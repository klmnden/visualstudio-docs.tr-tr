---
title: FIELD_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- FIELD_INFO
helpviewer_keywords:
- FIELD_INFO structure
ms.assetid: bfafef6d-0c83-43d7-a779-1f0d24b166a1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 83cdacae192ad1286203139432a0eacd632b8511
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62877771"
---
# <a name="fieldinfo"></a>FIELD_INFO
Bu yapı, yerel bir değişken, parametre veya diğer alanlar açıklanır.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagFieldInfo {
    FIELD_INFO_FIELDS dwFields;
    BSTR              bstrFullName;
    BSTR              bstrName;
    BSTR              bstrType;
    FIELD_MODIFIERS   dwModifiers;
} FIELD_INFO;
```

```csharp
public struct FIELD_INFO {
    public uint   dwFields;
    public string bstrFullName;
    public string bstrName;
    public string bstrType;
    public uint   dwModifiers;
};
```

## <a name="members"></a>Üyeler
bayrakları birleşimi dwFields A [FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md) hangi üyelerin doldurulur belirten sabit listesi.

bstrFullName alanının tam adı.

kısa ad alanının bstrName.

bstrType alanının türü.

bayrakları birleşimi dwModifiers A [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md) alanı açıklayan sabit listesi.

## <a name="remarks"></a>Açıklamalar
Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md) yöntemi burada da doldurulur.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md)
- [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)
