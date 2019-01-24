---
title: BP_RES_DATA_FLAGS | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- BP_RES_DATA_FLAGS
helpviewer_keywords:
- BP_RES_DATA_FLAGS enumeration
ms.assetid: d97611e2-def6-45a9-ad7d-eedf2ad4c82b
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 68d1c0705ae7d27bf281f5d65e9385228cd36bc4
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54786413"
---
# <a name="bpresdataflags"></a>BP_RES_DATA_FLAGS
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Veri kesme noktası olup olmadığını Öykünülen veya uygulanan donanımı belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_BP_RES_DATA_FLAGS {   
   BP_RES_DATA_EMULATED = 0x0001  
};  
typedef DWORD BP_RES_DATA_FLAGS;  
```  
  
```csharp  
public enum enum_BP_RES_DATA_FLAGS {   
   BP_RES_DATA_EMULATED = 0x0001  
};  
```  
  
## <a name="members"></a>Üyeler  
 BP_RES_DATA_EMULATED  
 Veri kesme noktası benzetilip benzetilmediğini olduğunu belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 İçin kullanılan `dwFlags` üyesi [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md) yapısı.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_RESOLUTION_DATA](../../../extensibility/debugger/reference/bp-resolution-data.md)
