﻿---
Description: 'Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT). Applications typically do not use this attribute.'
ms.assetid: '96a99f35-f9db-407e-a4e3-7adc3caccb19'
title: 'MF\_ACTIVATE\_MFT\_LOCKED attribute'
---

# MF\_ACTIVATE\_MFT\_LOCKED attribute

Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT). Applications typically do not use this attribute.

## Data type

**UINT32**

Treat as a Boolean value.

## Remarks

If value of this attribute is nonzero, the topology loader will not change the media types on the MFT. The topology loader sets this attribute after it loads the topology.

The GUID constant for this attribute is exported from mfuuid.lib.

## Requirements



|                                     |                                                                                    |
|-------------------------------------|------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista \[desktop apps only\]<br/>                                     |
| Minimum supported server<br/> | Windows Server 2008 \[desktop apps only\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## See also

<dl> <dt>

[Alphabetical List of Media Foundation Attributes](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](imfattributes-getuint32.md)
</dt> <dt>

[**IMFAttributes::SetUINT32**](imfattributes-setuint32.md)
</dt> <dt>

[Transform Attributes](transform-attributes.md)
</dt> </dl>

 

 



