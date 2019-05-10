---
title: MODULE_FLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MODULE_FLAGS
helpviewer_keywords:
- MODULE_FLAGS enumeration
ms.assetid: 0e555b42-b846-4dbb-812e-8e3d11c85b2d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b090fecf532ef862660b26432e930830cdb1d12b
ms.sourcegitcommit: 50f0c3f2763a05de8482b3579026d9c76c0e226c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65460955"
---
# <a name="moduleflags"></a>MODULE_FLAGS
Bir modülü tanımlamak için kullanılır.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_MODULE_FLAGS { 
   MODULE_FLAG_NONE        = 0x0000,
   MODULE_FLAG_SYSTEM      = 0x0001,
   MODULE_FLAG_SYMBOLS     = 0x0002,
   MODULE_FLAG_64BIT       = 0x0004,
   MODULE_FLAG_OPTIMIZED   = 0x0008,
   MODULE_FLAG_UNOPTIMIZED = 0x0010
};
typedef DWORD MODULE_FLAGS;
```

```csharp
public enum enum_MODULE_FLAGS { 
   MODULE_FLAG_NONE        = 0x0000,
   MODULE_FLAG_SYSTEM      = 0x0001,
   MODULE_FLAG_SYMBOLS     = 0x0002,
   MODULE_FLAG_64BIT       = 0x0004,
   MODULE_FLAG_OPTIMIZED   = 0x0008,
   MODULE_FLAG_UNOPTIMIZED = 0x0010
};
```

## <a name="fields"></a>Alanlar
 `MODULE_FLAG_NONE`\
 Hiçbir modül belirtir.

 `MODULE_FLAG_SYSTEM`\
 Bir sistem modülünün belirtir.

 `MODULE_FLAG_SYMBOLS`\
 Sembol Modülü belirtir.

 `MODULE_FLAG_64BIT`\
 Bir 64-bit Modülü belirtir.

 `MODULE_FLAG_OPTIMIZED`\
 İyileştirilmiş Modülü belirtir. Bu durumu yansıtılır **modülleri** penceresi.

 `MODULE_FLAG_UNOPTIMIZED`\
 Modül getirilmemiş belirtir. Bu durumu yansıtılır **modülleri** penceresi. Varsayılan durum budur.

## <a name="remarks"></a>Açıklamalar
 İçin kullanılan `m_dwModuleFlags` üyesi [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) yapısı.

 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)