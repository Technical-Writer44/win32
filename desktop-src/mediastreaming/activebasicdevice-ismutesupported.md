---
title: ActiveBasicDevice IsMuteSupported property
description: Gets a value that indicates if the device supports muting the audio.
ms.assetid: 'FF4B533F-B416-4DBE-BF86-FA34E785FFA2'
keywords: ["IsMuteSupported property Media Streaming API", "IsMuteSupported property Media Streaming API , ActiveBasicDevice interface", "ActiveBasicDevice interface Media Streaming API , IsMuteSupported property"]
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
---

# ActiveBasicDevice::IsMuteSupported property

Gets a value that indicates if the device supports muting the audio.

This property is read-only.

## Syntax


```C++
HRESULT get_IsMuteSupported(
  [out]�boolean *value
);
```



## Property value

A pointer to a **boolean** that indicates if the device supports muting the audio.

**true** if the device supports muting the audio; otherwise, **false**.

## Requirements



|                                     |                                                                                             |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�8.1 \[desktop apps only\]<br/>                                                |
| Minimum supported server<br/> | Windows Server�2012�R2 \[desktop apps only\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## See also

<dl> <dt>

[**ActiveBasicDevice**](activebasicdevice.md)
</dt> </dl>

�

�




