---
title: BUILT_TYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BUILT_TYPE
helpviewer_keywords:
- BUILT_TYPE structure
ms.assetid: cc02c32c-0f65-4210-ad25-a9b1899066e8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 692391379c3f2581e535a9e5c885f776565fb93d
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315499"
---
# <a name="builttype"></a>BUILT_TYPE
Bu yapı meta verilerinden harcanan alan türü hakkında bilgileri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _tagTYPE_BUILT {
    ULONG32      ulAppDomainID;
    GUID         guidModule;
    IDebugField* pUnderlyingField;
} BUILT_TYPE;
```

```csharp
public struct BUILT_TYPE {
    public uint        ulAppDomainID;
    public Guid        guidModule;
    public IDebugField pUnderlyingField;
};
```

#### <a name="parameters"></a>Parametreler
ulAppDomainID  
Simgenin içinden gelen uygulama kimliği. Bu, uygulamanın bir örneğini benzersiz şekilde tanımlamak için kullanılır.

guidModule  
Bu alan içeren modül GUID.

pUnderlyingField  
Bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) yerleşik bu alanla ilişkilendirilmiş temel alan tanımlayan nesne.

## <a name="remarks"></a>Açıklamalar
Bu yapı birleşimde bir parçası olarak görünür [TYPE_INFO](../../../extensibility/debugger/reference/type-info.md) ne zaman yapısı `dwKind` alanını `TYPE_INFO` yapısı ayarlandığında `TYPE_KIND_BUILT` (arasında bir değer [dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md) sabit listesi).

## <a name="requirements"></a>Gereksinimler
Üstbilgi: sh.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)  
[TYPE_INFO](../../../extensibility/debugger/reference/type-info.md)  
[dwTYPE_KIND](../../../extensibility/debugger/reference/dwtype-kind.md)  
[IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
