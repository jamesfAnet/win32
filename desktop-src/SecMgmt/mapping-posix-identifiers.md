---
Description: The Posix subsystem must be able to translate any security identifier (SID) it encounters into a 32-bit value, called a Posix ID.
ms.assetid: cd6c89ef-c3f1-47fe-8183-320b5d24b0dd
title: Mapping Posix Identifiers
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Mapping Posix Identifiers

The Posix subsystem must be able to translate any [*security identifier*](https://msdn.microsoft.com/library/windows/desktop/ms721625#-security-security-identifier-gly) (SID) it encounters into a 32-bit value, called a *Posix ID*. Furthermore, it must be able to categorize the ID as either a user ID or a group ID. To understand how this mapping is accomplished, let's first look at the SIDs that must be mapped.

SIDs have two components, the SID of the domain and the relative ID of the account in the domain. For example, in the SID S-1-518364-21-43-8, the last number, 8, is the account's relative ID (RID) and S-1-518364-21-43 is the SID of the domain.

Domain information is stored in [**TrustedDomain**](trusteddomain-object.md) objects. Part of the information stored in a **TrustedDomain** object is a Posix ID offset to be used for SIDs within that domain. For example, assume that a **TrustedDomain** is defined as follows:

``` syntax
    Name:    NtPgm
    Sid:    S-1-518364-21-43
    Posix Offset:    0x130000
```

Posix IDs for accounts in this domain would be generated by adding 0x130000 to the relative ID of the account. So, the Posix ID corresponding to the SID S-1-518364-21-43-8 would be 0x130008.

Not all Posix ID translations make use of a [**TrustedDomain**](trusteddomain-object.md) object. The following table shows SIDs that are mapped using well-known offset values.



| Source                                              | Posix ID offset |
|-----------------------------------------------------|-----------------|
| SIDs from the built-in domain                       | 0x20000         |
| SIDs from the account domain                        | 0x30000         |
| SIDs from the primary domain (on Workstations only) | 0x40000         |



 

And finally, one other set of SIDs, logon SIDs, requires special processing. These values are assigned by the Windows logon process for each logon session and have the form S-1-5-5-X-Y, where X and Y are treated as a single LARGE\_INTEGER that is incremented for each logon session. These SIDs are mapped to the constant Posix ID 0xFFF. To map the Posix ID 0xFFF, you may translate whatever [*logon identifier*](https://msdn.microsoft.com/library/windows/desktop/ms721592#-security-logon-identifier-gly) best suits the situation, or you may use S-1-5-5-0-0 by default. (For example, if a posix user applies protection to an object and specifies FFFx, it is better to substitute that user's logon identifier than just assigning S-1-5-5-0-0.)

 

 


