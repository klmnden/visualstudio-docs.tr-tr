---
title: DEBUG_REFERENCE_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DEBUG_REFERENCE_INFO
helpviewer_keywords:
- DEBUG_REFERENCE_INFO structure
ms.assetid: 24b83d00-d756-42a1-8083-730f998761dc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3167deaa7e088ed75584f9fdc0777a608f11a47e
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56413481"
---
# <a name="debugreferenceinfo"></a>DEBUG_REFERENCE_INFO
Bir başvuru açıklar.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct tagDEBUG_REFERENCE_INFO {
    DEBUGREF_INFO_FLAGS dwFields;
    BSTR                bstrName;
    BSTR                bstrType;
    BSTR                bstrValue;
    DBG_ATTRIB_FLAGS    dwAttrib;
    REFERENCE_TYPE.     dwRefType;
    IDebugReference2*   m_pReference;
} DEBUG_REFERENCE_INFO;
```

```csharp
public struct DEBUG_REFERENCE_INFO {
    public uint             dwFields;
    public string           bstrName;
    public string           bstrType;
    public string           bstrValue;
    public ulong            dwAttrib;
    public uint.            dwRefType;
    public IDebugReference2 m_pReference;
};
```

## <a name="members"></a>Üyeler
dwFields  
Bayraklarının bir birleşimi [DEBUGREF_INFO_FLAGS](../../../extensibility/debugger/reference/debugref-info-flags.md) hangi alanların doldurulmuş belirten sabit listesi.

bstrName  
Kullanıcı tarafından belirtilen adı [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) nesne.

bstrType  
Başvuru türü olarak biçimlendirilmiş bir dize.

bstrValue  
Başvuru değeri olarak biçimlendirilmiş bir dize

dwAttrib  
Bayraklarının bir birleşimi [DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md) bayrakları için hata ayıklama özellik öznitelikleri belirten sabit listesi.

dwRefType  
Bir değer [REFERENCE_TYPE](../../../extensibility/debugger/reference/reference-type.md) güçlü veya zayıf başvuru türü olup olmadığını belirten sabit listesi.

m_pReference  
Bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) başvuru bilgileri belirten bir nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı bir çağrısına geçirilen [GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md) doldurulması için yöntemi. Bu yapı ayrıca bir listeden bir parçası olarak döndürülen [IEnumDebugReferenceInfo2](../../../extensibility/debugger/reference/ienumdebugreferenceinfo2.md) hangi sırayla çağrısından döndürülen arabirimi [EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)  
[DEBUGREF_INFO_FLAGS](../../../extensibility/debugger/reference/debugref-info-flags.md)  
[DBG_ATTRIB_FLAGS](../../../extensibility/debugger/reference/dbg-attrib-flags.md)  
[REFERENCE_TYPE](../../../extensibility/debugger/reference/reference-type.md)  
[GetReferenceInfo](../../../extensibility/debugger/reference/idebugreference2-getreferenceinfo.md)  
[EnumChildren](../../../extensibility/debugger/reference/idebugreference2-enumchildren.md)  
[IEnumDebugReferenceInfo2](../../../extensibility/debugger/reference/ienumdebugreferenceinfo2.md)
