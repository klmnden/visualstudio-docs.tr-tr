---
title: NESNE_TÜRÜ | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- OBJECT_TYPE
helpviewer_keywords:
- OBJECT_TYPE enumeration
ms.assetid: c4d246f9-8a98-44ec-b2bb-ff5c684f668e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 08d50e3d3ddda55a7ff0f3fea333c5408b02878a
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65461040"
---
# <a name="objecttype"></a>OBJECT_TYPE
İfade değerlendirici nesneden türünü belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_OBJECT_TYPE { 
   OBJECT_TYPE_BOOLEAN = 0x0,
   OBJECT_TYPE_CHAR    = 0x1,
   OBJECT_TYPE_I1      = 0x2,
   OBJECT_TYPE_U1      = 0x3,
   OBJECT_TYPE_I2      = 0x4,
   OBJECT_TYPE_U2      = 0x5,
   OBJECT_TYPE_I4      = 0x6,
   OBJECT_TYPE_U4      = 0x7,
   OBJECT_TYPE_I8      = 0x8,
   OBJECT_TYPE_U8      = 0x9,
   OBJECT_TYPE_R4      = 0xa,
   OBJECT_TYPE_R8      = 0xb,
   OBJECT_TYPE_OBJECT  = 0xc,
   OBJECT_TYPE_NULL    = 0xd,
   OBJECT_TYPE_CLASS   = 0xe
};
typedef DWORD OBJECT_TYPE;
```

```csharp
public enum enum_OBJECT_TYPE { 
   OBJECT_TYPE_BOOLEAN = 0x0,
   OBJECT_TYPE_CHAR    = 0x1,
   OBJECT_TYPE_I1      = 0x2,
   OBJECT_TYPE_U1      = 0x3,
   OBJECT_TYPE_I2      = 0x4,
   OBJECT_TYPE_U2      = 0x5,
   OBJECT_TYPE_I4      = 0x6,
   OBJECT_TYPE_U4      = 0x7,
   OBJECT_TYPE_I8      = 0x8,
   OBJECT_TYPE_U8      = 0x9,
   OBJECT_TYPE_R4      = 0xa,
   OBJECT_TYPE_R8      = 0xb,
   OBJECT_TYPE_OBJECT  = 0xc,
   OBJECT_TYPE_NULL    = 0xd,
   OBJECT_TYPE_CLASS   = 0xe
};
```

## <a name="fields"></a>Alanlar
 `OBJECT_TYPE_BOOLEAN`\
 Bir Boole değeri bir nesne olduğunu gösterir.

 `OBJECT_TYPE_CHAR`\
 Bir nesne bir karakter olduğunu gösterir.

 `OBJECT_TYPE_I1`\
 Nesnesi bir bayt imzalı bir tamsayı olduğu anlamına gelir.

 `OBJECT_TYPE_U1`\
 Bir nesne için bir tane bayt işaretsiz tamsayı olduğunu gösterir.

 `OBJECT_TYPE_I2`\
 Nesne iki baytlık bir işaretli tamsayı olduğunu gösterir.

 `OBJECT_TYPE_U2`\
 Bir nesne bir iki bayt işaretsiz tamsayı olduğunu gösterir.

 `OBJECT_TYPE_I4`\
 Nesne dört baytlık bir işaretli tamsayı olduğunu gösterir.

 `OBJECT_TYPE_U4`\
 Dört bayt işaretsiz tamsayı bir nesne olduğunu gösterir.

 `OBJECT_TYPE_I8`\
 Nesne bir sekiz bayt imzalı tamsayı olduğunu gösterir.

 `OBJECT_TYPE_U8`\
 Bir nesne bir sekiz bayt işaretsiz tamsayı olduğunu gösterir.

 `OBJECT_TYPE_R4`\
 Nesne dört baytlık bir kayan noktalı sayı olduğunu gösterir.

 `OBJECT_TYPE_R8`\
 Bir nesne bir sekiz bayt kayan noktalı sayı olduğunu gösterir.

 `OBJECT_TYPE_OBJECT`\
 Bir nesne bir nesne olduğunu gösterir.

 `OBJECT_TYPE_NULL`\
 Nesne NULL olduğunu gösterir.

 `OBJECT_TYPE_CLASS`\
 Bir nesne bir sınıf olduğunu belirtir.

## <a name="remarks"></a>Açıklamalar
 Bağımsız değişken olarak geçirilen [CreatePrimitiveObject](../../../extensibility/debugger/reference/idebugfunctionobject-createprimitiveobject.md) ve [CreateArrayObject](../../../extensibility/debugger/reference/idebugfunctionobject-createarrayobject.md) yöntemleri.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [CreatePrimitiveObject](../../../extensibility/debugger/reference/idebugfunctionobject-createprimitiveobject.md)
- [CreateArrayObject](../../../extensibility/debugger/reference/idebugfunctionobject-createarrayobject.md)