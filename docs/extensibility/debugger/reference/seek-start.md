---
title: SEEK_START | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- SEEK_START
helpviewer_keywords:
- SEEK_START enumeration
ms.assetid: 55bd8901-626e-428b-a263-23b14417f4c6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e003b74faeb7c6ed165c43380a7c4c6b0520ea0c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62864827"
---
# <a name="seekstart"></a>SEEK_START
Ayrıştırılmış kodu stream'de arama başlatılacağı konumu belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_SEEK_START { 
   SEEK_START_BEGIN       = 0x0001,
   SEEK_START_END         = 0x0002,
   SEEK_START_CURRENT     = 0x0003,
   SEEK_START_CODECONTEXT = 0x0004,
   SEEK_START_CODELOCID   = 0x0005
};
typedef DWORD SEEK_START;
```

```csharp
public enum enum_SEEK_START { 
   SEEK_START_BEGIN       = 0x0001,
   SEEK_START_END         = 0x0002,
   SEEK_START_CURRENT     = 0x0003,
   SEEK_START_CODECONTEXT = 0x0004,
   SEEK_START_CODELOCID   = 0x0005
};
```

## <a name="members"></a>Üyeler
 Geçerli belgenin başlangıcında arayan SEEK_START_BEGIN başlatır.

 Geçerli belgenin sonunda arayan SEEK_START_END başlatır.

 Geçerli belge geçerli konumda arama SEEK_START_CURRENT başlatır.

 Geçerli belgenin verilen kod bağlamı arayan SEEK_START_CODECONTEXT başlatır.

 SEEK_START_CODELOCID belirli kod konum tanımlayıcısı aramayı başlatır. Kod konumu tanımlayıcılarını elde edilen çağırarak [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md).

## <a name="remarks"></a>Açıklamalar
 Bağımsız değişken olarak geçirilen [arama](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
 Üstbilgi: msdbg.h

 Ad alanı: Microsoft.VisualStudio.Debugger.Interop

 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [Seek](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)
- [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)