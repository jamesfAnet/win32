---
Description: MaxMergeInterval
ms.assetid: d93ae152-eace-45bb-af64-6541a0f9f5a2
title: MaxMergeInterval
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MaxMergeInterval

> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](https://msdn.microsoft.com/windows/desktop/6da601c6-3742-40ad-99f2-8817f7f642b3) for client side search and [Microsoft Search Server Express]( http://go.microsoft.com/fwlink/p/?linkid=258445) for server side search.

 

The **MaxMergeInterval** entry is the time interval to wait between merges.

### Summary



|          |                |
|----------|----------------|
| Type:    | **REG\_DWORD** |
| Units:   | Minutes        |
| Default: | 10             |
| Range:   | 1 - 60         |



 

### Remarks

After an interval equal to the value of the **MaxMergeInterval** entry, Indexing Service determines whether a merge is necessary. When necessary, Indexing Service usually performs an annealing merge, but it may be a shadow merge or master merge.

## Related topics

<dl> <dt>

[Catalog, Property, and Scope Registry Entries](catalog--property--and-scope-registry-entries.md)
</dt> <dt>

[Main Registry Entries](main-registry-entries.md)
</dt> </dl>

 

 


