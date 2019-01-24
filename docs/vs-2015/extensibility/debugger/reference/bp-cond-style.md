---
title: BP_COND_STYLE | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- BP_COND_STYLE
helpviewer_keywords:
- BP_COND_STYLE enumeration
ms.assetid: a93b1412-f447-48a1-af9d-38f3dbb3092f
caps.latest.revision: 11
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: fbb2674381992bd86f0144af103615f0a3922fcf
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54779594"
---
# <a name="bpcondstyle"></a>BP_COND_STYLE
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bekleyen kesme noktası koşulu stili için belirtir ve bağlı kesme noktaları.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
enum enum_BP_COND_STYLE {   
   BP_COND_NONE         = 0x0000,  
   BP_COND_WHEN_TRUE    = 0x0001,  
   BP_COND_WHEN_CHANGED = 0x0002  
};  
typedef DWORD BP_COND_STYLE;  
```  
  
```csharp  
public enum enum_BP_COND_STYLE {   
   BP_COND_NONE         = 0x0000,  
   BP_COND_WHEN_TRUE    = 0x0001,  
   BP_COND_WHEN_CHANGED = 0x0002  
};  
```  
  
## <a name="members"></a>Üyeler  
 BP_COND_NONE  
 Kesme noktasına, Kesme noktasının konuma ulaşıldığında tetikler. Belirtilen hiçbir kesme noktası koşulu.  
  
 BP_COND_WHEN_TRUE  
 Veren, koşullu ifade kesme noktasıyla ilişkili yalnızca bir kesme noktası harekete `true`.  
  
 BP_COND_WHEN_CHANGED  
 Yalnızca koşullu ifadenin değerini kesme noktası ile ilişkili olduğunda kesme noktası, önceki değerlendirmesinden gelen değişti ateşlenir.  
  
## <a name="remarks"></a>Açıklamalar  
 İçin kullanılan `styleCondition` üyesi [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) yapısı.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)
