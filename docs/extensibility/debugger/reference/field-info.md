---
title: FIELD_INFO | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: b34624672b64d88ca9b080094c5d661494c089cf
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315904"
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
dwFields  
Bayraklarının bir birleşimi [FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md) hangi üyelerin doldurulur belirten sabit listesi.

bstrFullName  
Alanının tam adı.

bstrName  
Kısa ad alanı.

bstrType  
Alan türü.

dwModifiers  
Bayraklarının bir birleşimi [FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md) alanı açıklayan sabit listesi.

## <a name="remarks"></a>Açıklamalar
Bu yapı geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md) yöntemi burada da doldurulur.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[FIELD_INFO_FIELDS](../../../extensibility/debugger/reference/field-info-fields.md)  
[FIELD_MODIFIERS](../../../extensibility/debugger/reference/field-modifiers.md)  
[GetInfo](../../../extensibility/debugger/reference/idebugfield-getinfo.md)
