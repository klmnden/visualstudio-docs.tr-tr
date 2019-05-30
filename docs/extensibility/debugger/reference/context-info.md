---
title: CONTEXT_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CONTEXT_INFO
helpviewer_keywords:
- CONTEXT_INFO structure
ms.assetid: 6b513f4e-e7b0-4969-adf0-2205ccc1e09b
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 6c50d5ea930f05d22b68416978909cceca17727d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66346463"
---
# <a name="contextinfo"></a>CONTEXT_INFO
Bu yapı, bellek bağlamı veya kod bağlamı açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagCONTEXT_INFO {
    CONTEXT_INFO_FIELDS dwFields;
    BSTR                bstrModuleUrl;
    BSTR                bstrFunction;
    TEXT_POSITION       posFunctionOffset;
    BSTR                bstrAddress;
    BSTR                bstrAddressOffset;
    BSTR                bstrAddressAbsolute;
} CONTEXT_INFO;
```

```csharp
public struct CONTEXT_INFO {
    public uint          dwFields;
    public string        bstrModuleUrl;
    public string        bstrFunction;
    public TEXT_POSITION posFunctionOffset;
    public string        bstrAddress;
    public string        bstrAddressOffset;
    public string        bstrAddressAbsolute;
};
```

## <a name="members"></a>Üyeler
`dwFields`\
He bayraklarının bir birleşimi [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md) hangi alanların doldurulmuş belirten numaralandırma<strong>.</strong>

`bstrModuleUrl`\
Bağlam bulunduğu modülünün adı.

`bstrFunction`\
Bağlam bulunduğu işlevi adı.

`posFunctionOffset`\
A [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md) kod bağlamı ile ilişkili işlevi satır ve sütun uzaklığı tanımlayan yapısı.

`bstrAddress`\
Belirtilen bağlamda bulunduğu kod adresi.

`bstrAddressOffset`\
Belirtilen bağlamda bulunduğu kod adres uzaklığı.

`bstrAddressAbsolute`\
Belirtilen bağlamda bulunduğu bellek mutlak bir adres.

## <a name="remarks"></a>Açıklamalar
Bu yapı çağrısından döndürülen [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md) yöntemi.

Bu yapı için genel kullanım support biri olan bir **bellek** hata ayıklama penceresine.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md)
- [CONTEXT_INFO_FIELDS](../../../extensibility/debugger/reference/context-info-fields.md)
- [TEXT_POSITION](../../../extensibility/debugger/reference/text-position.md)
