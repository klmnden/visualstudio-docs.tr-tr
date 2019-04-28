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
ms.openlocfilehash: c3ec96c5ba806e6eff735edc8093868b19ebaf5b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62913841"
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

## <a name="members"></a>Üyeler
 Hiçbir modül MODULE_FLAG_NONE belirtir.

 Bir sistem modülünün MODULE_FLAG_SYSTEM belirtir.

 Sembol modülü MODULE_FLAG_SYMBOLS belirtir.

 Bir 64-bit modül MODULE_FLAG_64BIT belirtir.

 İyileştirilmiş modülü MODULE_FLAG_OPTIMIZED belirtir. Bu durumu yansıtılır **modülleri** penceresi.

 Modül getirilmemiş MODULE_FLAG_UNOPTIMIZED belirtir. Bu durumu yansıtılır **modülleri** penceresi. Varsayılan durum budur.

## <a name="remarks"></a>Açıklamalar
 İçin kullanılan `m_dwModuleFlags` üyesi [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md) yapısı.

 Bu bayrak bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [MODULE_INFO](../../../extensibility/debugger/reference/module-info.md)