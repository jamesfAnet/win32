---
title: SetGroupPresharedKey\_IN structure
description: The SetGroupPresharedKey\_IN structure holds the input data for the SetGroupPresharedKey method.
ms.assetid: fe5e1f75-ebd0-4856-bb77-14efb52fbce0
keywords:
- SetGroupPresharedKey_IN structure Storage Devices
- PSetGroupPresharedKey_IN structure pointer Storage Devices
topic_type:
- apiref
api_name:
- SetGroupPresharedKey_IN
api_location:
- iscsiop.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: structure
ms.date: 05/31/2018
---

# SetGroupPresharedKey\_IN structure

The SetGroupPresharedKey\_IN structure holds the input data for the [SetGroupPresharedKey](https://msdn.microsoft.com/library/windows/hardware/ff565693) method.

## Syntax


```C++
typedef struct _SetGroupPresharedKey_IN {
  ULONG KeySize;
  UCHAR Key[1];
} SetGroupPresharedKey_IN, *PSetGroupPresharedKey_IN;
```



## Members

<dl> <dt>

**KeySize**
</dt> <dd>

The size, in bytes, of the key in **Key***.*

</dd> <dt>

**Key**
</dt> <dd>

The preshared group key*.*

</dd> </dl>

## Remarks

You must implement this method.

## Requirements



|                   |                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Iscsiop.h (include Iscsiop.h)</dt> </dl> |



## See also

<dl> <dt>

[SetGroupPresharedKey](https://msdn.microsoft.com/library/windows/hardware/ff565693)
</dt> <dt>

[**SetGroupPresharedKey\_OUT**](setgrouppresharedkey-out.md)
</dt> </dl>

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bstorage\storage%5D:%20SetGroupPresharedKey_IN%20structure%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





