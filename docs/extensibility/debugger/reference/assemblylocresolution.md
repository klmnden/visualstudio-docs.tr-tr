---
title: ASSEMBLYLOCRESOLUTION | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- ASSEMBLYLOCRESOLUTION
helpviewer_keywords:
- ASSEMBLYLOCRESOLUTION enumeration
ms.assetid: 0bcfe85c-5f37-4a9d-bf2b-141acd96ad67
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: c7a15c4f29cc4f7a9224634dc88755582429d581
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54972423"
---
# <a name="assemblylocresolution"></a>ASSEMBLYLOCRESOLUTION
Bir derlemeyi nerede olduğunu belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_ASSEMBLYLOCRESOLUTION {  
   ALR_NAME      = 0x0,  
   ALR_USERDIR   = 0x1,  
   ALR_SHAREDDIR = 0x2,  
   ALR_REMOTEDIR = 0x4,  
};  
typedef DWORD ASSEMBLYLOCRESOLUTION;  
```  
  
```csharp  
public enum enum_ASSEMBLYLOCRESOLUTION {  
   ALR_NAME      = 0x0,  
   ALR_USERDIR   = 0x1,  
   ALR_SHAREDDIR = 0x2,  
   ALR_REMOTEDIR = 0x4,  
};  
```  
  
## <a name="members"></a>Üyeler  
 ALR_NAME  
 Derleme geçerli bir ad alanında bulunur.  
  
 ALR_USERDIR  
 Derleme kullanıcı dizininde bulunur.  
  
 ALR_SHAREDDIR  
 Derleme, paylaşılan dizininde bulunur.  
  
 ALR_REMOTEDIR  
 Derleme, uzak bir dizinde bulunur.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerler tarafından döndürülen [ResolveAssemblyRef](../../../extensibility/debugger/reference/ipropertyproxyeeside-resolveassemblyref.md) ve [GetManagedViewerCreationData](../../../extensibility/debugger/reference/ipropertyproxyeeside-getmanagedviewercreationdata.md) yöntemleri.  
  
 Bu değerler ile birleştirilmiş `OR` işlemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [ResolveAssemblyRef](../../../extensibility/debugger/reference/ipropertyproxyeeside-resolveassemblyref.md)   
 [GetManagedViewerCreationData](../../../extensibility/debugger/reference/ipropertyproxyeeside-getmanagedviewercreationdata.md)