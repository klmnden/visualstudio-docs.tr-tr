---
title: DUMPTYPE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DUMPTYPE
helpviewer_keywords:
- DUMPTYPE enumeration
ms.assetid: ea8160db-8732-4056-a1d7-892ef72da71e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ab7d66ecae911faf8cc42a840ac853d585fc80bb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55012588"
---
# <a name="dumptype"></a>DUMPTYPE
Döküm için ne kadar bir programın durumu ' (örneğin, çalışan iş parçacıkları, yığın çerçeveleri ve geçerli yönerge adresi) belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_DUMPTYPE {   
   DUMP_MINIDUMP = 0,  
   DUMP_FULLDUMP = 1  
};  
typedef DWORD DUMPTYPE;  
```  
  
```csharp  
public enum enum_DUMPTYPE {   
   DUMP_MINIDUMP = 0,  
   DUMP_FULLDUMP = 1  
};  
```  
  
## <a name="members"></a>Üyeler  
 DUMP_MINIDUMP  
 Küçük, küçük bir döküm belirtir.  
  
 DUMP_FULLDUMP  
 Büyük, eksiksiz bir döküm belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bağımsız değişken olarak geçirilen [WriteDump](../../../extensibility/debugger/reference/idebugprogram2-writedump.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [WriteDump](../../../extensibility/debugger/reference/idebugprogram2-writedump.md)