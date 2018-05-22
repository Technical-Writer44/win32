﻿---
Description: 'Creates an instance of the capture engine.'
ms.assetid: '4B0C9DD6-135D-4412-A585-7E98A84101B5'
title: MFCreateCaptureEngine function
---

# MFCreateCaptureEngine function

\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future. \]

Creates an instance of the capture engine.

## Syntax


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## Parameters

<dl> <dt>

*ppCaptureEngine* \[out\]
</dt> <dd>

Receives a pointer to the [**IMFCaptureEngine**](imfcaptureengine.md) interface. The caller must release the interface.

</dd> </dl>

## Return value

If the function succeeds, it returns S\_OK. Otherwise, it returns an **HRESULT** error code.

## Remarks

This function has no associated import library and is not declared in a public header file. You must use the [**LoadLibrary**](base.loadlibrary) and [**GetProcAddress**](base.getprocaddress) functions to dynamically link to MFCaptureEngine.dll.

## Requirements



|                                     |                                                                                                |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8 \[desktop apps only\]<br/>                                                     |
| Minimum supported server<br/> | Windows Server 2012 R2 \[desktop apps only\]<br/>                                        |
| DLL<br/>                      | <dl> <dt>MFCaptureEngine.dll</dt> </dl> |



## See also

<dl> <dt>

[Media Foundation Functions](media-foundation-functions.md)
</dt> </dl>

 

 



