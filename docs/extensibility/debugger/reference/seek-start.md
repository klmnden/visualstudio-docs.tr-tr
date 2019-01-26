---
title: SEEK_START | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: 203371cd1ee2d1a9efe4c50f8d5a73f2fa7d7980
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54961886"
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
 SEEK_START_BEGIN  
 Geçerli belgenin başlangıcında aramayı başlatır.  
  
 SEEK_START_END  
 Geçerli belgenin sonunda aramayı başlatır.  
  
 SEEK_START_CURRENT  
 Geçerli belge geçerli konumuna aramayı başlatır.  
  
 SEEK_START_CODECONTEXT  
 Geçerli belgede belirli kod bağlamında aramayı başlatır.  
  
 SEEK_START_CODELOCID  
 Verilen kod konum tanımlayıcısı aramayı başlatır. Kod konumu tanımlayıcılarını elde edilen çağırarak [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md).  
  
## <a name="remarks"></a>Açıklamalar  
 Bağımsız değişken olarak geçirilen [arama](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [Arama](../../../extensibility/debugger/reference/idebugdisassemblystream2-seek.md)   
 [GetCurrentLocation](../../../extensibility/debugger/reference/idebugdisassemblystream2-getcurrentlocation.md)