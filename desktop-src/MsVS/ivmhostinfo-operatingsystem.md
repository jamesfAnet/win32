---
title: IVMHostInfo OperatingSystem property
description: The OperatingSystem property contains the name of the operating system currently running on the host machine.
ms.assetid: 3f0cc93e-d279-416a-8e7c-9d7618d93b56
keywords:
- OperatingSystem property Virtual Server
- OperatingSystem property Virtual Server , IVMHostInfo interface
- IVMHostInfo interface Virtual Server , OperatingSystem property
- OperatingSystem property Virtual Server , VMHostInfo interface
- VMHostInfo interface Virtual Server , OperatingSystem property
topic_type:
- apiref
api_name:
- IVMHostInfo.OperatingSystem
- IVMHostInfo.get_OperatingSystem
- VMHostInfo.OperatingSystem
api_location:
- VsComInterfaces.h
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IVMHostInfo::OperatingSystem property

The **OperatingSystem** property contains the name of the operating system currently running on the host machine.

This property is read-only.

## Syntax


```C++
HRESULT get_OperatingSystem(
  [out] BSTR *operatingSystem 
);
```

<span codelanguage="VisualBasic"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>VB</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>VMHostInfo.OperatingSystem( _
  ByRef operatingSystem  _
)</code></pre></td>
</tr>
</tbody>
</table>



## Property value

The name of the operating system currently running on the host machine.

This property value is read-only.

## Error codes



| Name                                                                                          | Meaning                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt> S\_OK</dt> </dl>             | The operation was successful.<br/>       |
| <dl> <dt>E\_POINTER</dt> </dl>         | The outgoing parameter is **NULL**.<br/> |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> </dl> | An unexpected error occurred.<br/>       |



## Requirements



|                     |                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------|
| Product<br/>  | Microsoft Virtual Server 2005 onWindows Server 2003<br/>                                    |
| Download<br/> | Microsoft Virtual Server 2005 R2 SP1 Update onWindows Server 2008orWindows Server 2003<br/> |
| Header<br/>   | <dl> <dt>VsComInterfaces.h</dt> </dl>      |



## See also

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

 




