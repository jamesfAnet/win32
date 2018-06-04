---
Description: Asynchronously uninstalls a server component from a VHD on a managed node.
audience: developer
ms.assetid: 641c13de-8c63-41a8-97d4-a21079cab82b
ms.prod: windows-server-dev
ms.technology: windows-management-instrumentation
ms.tgt_platform: multiple
title: RemoveServerComponentVhdAsync method of the MSFT\_ServerManagerDeploymentTasks class
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# RemoveServerComponentVhdAsync method of the MSFT\_ServerManagerDeploymentTasks class

Asynchronously uninstalls a server component from a VHD on a managed node.

## Syntax


```mof
uint32 RemoveServerComponentVhdAsync(
  [in]  MSFT_ServerManagerRequestGuid               RequestGuid,
  [in]  Boolean                                     DeleteComponents,
  [in]  MSFT_ServerManagerServerComponentDescriptor ServerComponentDescriptors[],
  [in]  String                                      VhdPath,
  [out] MSFT_ServerManagerRequestState              AlterationState
);
```



## Parameters

<dl> <dt>

*RequestGuid* \[in\]
</dt> <dd>

The **GUID** of this deployment request.

</dd> <dt>

*DeleteComponents* \[in\]
</dt> <dd>

Indicates whether to delete the server components. True to delete the components; otherwise false.

</dd> <dt>

*ServerComponentDescriptors* \[in\]
</dt> <dd>

An array that contains the identities of the server components to uninstall.

</dd> <dt>

*VhdPath* \[in\]
</dt> <dd>

The path to the VHD that contains the server components.

</dd> <dt>

*AlterationState* \[out\]
</dt> <dd>

A string that receives the state of this deployment request.

</dd> </dl>

## Requirements



|                                     |                                                                                                                 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                                       |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                                                  |
| Namespace<br/>                | Root\\StandardCimv2<br/>                                                                                  |
| MOF<br/>                      | <dl> <dt>ServerManager.DeploymentProvider.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>ServerManager.DeploymentProvider.dll</dt> </dl> |



## See also

<dl> <dt>

[**MSFT\_ServerManagerDeploymentTasks**](msft-servermanagerdeploymenttasks.md)
</dt> </dl>

 

 



