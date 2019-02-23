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
ms.openlocfilehash: 7f0aafc5b41d9020c80cd2b86c9048db1d333bfd
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56708530"
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

## <a name="members"></a>Üyeler
 OBJECT_TYPE_BOOLEAN bir Boole değeri bir nesne olduğunu gösterir.

 OBJECT_TYPE_CHAR nesne bir karakter olduğunu gösterir.

 OBJECT_TYPE_I1 nesnesi bir bayt imzalı bir tamsayı olduğunu gösterir.

 OBJECT_TYPE_U1 nesne bir tane bayt işaretsiz tamsayı olduğunu gösterir.

 OBJECT_TYPE_I2 nesne iki baytlık bir işaretli tamsayı olduğunu gösterir.

 OBJECT_TYPE_U2 nesne bir iki bayt işaretsiz tamsayı olduğunu gösterir.

 OBJECT_TYPE_I4 nesne dört baytlık bir işaretli tamsayı olduğunu gösterir.

 OBJECT_TYPE_U4 nesne dört bayt işaretsiz tamsayı olduğunu gösterir.

 OBJECT_TYPE_I8 nesne sekiz bayt imzalı tamsayı olduğunu gösterir.

 OBJECT_TYPE_U8 nesne sekiz bayt işaretsiz tamsayı olduğunu gösterir.

 OBJECT_TYPE_R4 nesne dört baytlık bir kayan noktalı sayı olduğunu gösterir.

 OBJECT_TYPE_R8 nesne sekiz bayt kayan noktalı sayı olduğunu gösterir.

 OBJECT_TYPE_OBJECT nesne bir nesne olduğunu gösterir.

 OBJECT_TYPE_NULL nesnesi NULL olduğunu gösterir.

 OBJECT_TYPE_CLASS nesne bir sınıf olduğunu gösterir.

## <a name="remarks"></a>Açıklamalar
 Bağımsız değişken olarak geçirilen [CreatePrimitiveObject](../../../extensibility/debugger/reference/idebugfunctionobject-createprimitiveobject.md) ve [CreateArrayObject](../../../extensibility/debugger/reference/idebugfunctionobject-createarrayobject.md) yöntemleri.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: ee.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [CreatePrimitiveObject](../../../extensibility/debugger/reference/idebugfunctionobject-createprimitiveobject.md)
- [CreateArrayObject](../../../extensibility/debugger/reference/idebugfunctionobject-createarrayobject.md)