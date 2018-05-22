﻿---
Description: 'Computes the final hash of the data entered by the MD5Update function.'
ms.assetid: 'A0457D26-F4E3-4ED4-B374-0AFCB6F661FB'
title: 'A\_SHAFinal function'
---

# A\_SHAFinal function

Computes the final hash of the data entered by the MD5Update function.

## Syntax


```C++
VOID RSA32API A_SHAFinal(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR Result
);
```



## Parameters

<dl> <dt>

*Context* \[in, out\]
</dt> <dd>

The SHA context.

</dd> <dt>

*Result* \[out\]
</dt> <dd>

The resulting hash table.

</dd> </dl>

## Return value

This function does not return a value.

## Remarks

This function is very similar to SHAFinal, but is called directly from the library, rather than being routed through the cryptography infrastructure. For more information, see [Windows NTCryptographic Providers](https://msdn.microsoft.com/en-us/library/cc723484.aspx).

## Requirements



|                    |                                                                                      |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Sha.h</dt> </dl>     |
| Library<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |
| DLL<br/>     | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 



