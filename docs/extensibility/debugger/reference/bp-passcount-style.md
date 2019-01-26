---
title: BP_PASSCOUNT_STYLE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_PASSCOUNT_STYLE
helpviewer_keywords:
- BP_PASSCOUNT_STYLE structure
ms.assetid: 0a647047-e2d5-4724-a0b8-68108425ecad
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5df5adacb34c151c1347a9fe2b375b371c72e6d1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55025585"
---
# <a name="bppasscountstyle"></a>BP_PASSCOUNT_STYLE
Kesme noktası ateşlenmesine neden kesme noktası geçişi sayısı ile ilişkilendirilmiş olan koşul belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_BP_PASSCOUNT_STYLE {   
   BP_PASSCOUNT_NONE             = 0x0000,  
   BP_PASSCOUNT_EQUAL            = 0x0001,  
   BP_PASSCOUNT_EQUAL_OR_GREATER = 0x0002,  
   BP_PASSCOUNT_MOD              = 0x0003  
};  
typedef DWORD BP_PASSCOUNT_STYLE;  
```  
  
```csharp  
public enum enum_BP_PASSCOUNT_STYLE {   
   BP_PASSCOUNT_NONE             = 0x0000,  
   BP_PASSCOUNT_EQUAL            = 0x0001,  
   BP_PASSCOUNT_EQUAL_OR_GREATER = 0x0002,  
   BP_PASSCOUNT_MOD              = 0x0003  
};  
```  
  
## <a name="members"></a>Üyeler  
 BP_PASSCOUNT_NONE  
 Hiçbir kesme noktası geçişi sayısı stilini belirtir.  
  
 BP_PASSCOUNT_EQUAL  
 Eşit olacak şekilde kesme noktası geçişi sayısı stilini ayarlar. Kesme noktası geçişi sayısı kesme noktasına isabet sayısı eşit olduğunda tetiklenir.  
  
 BP_PASSCOUNT_EQUAL_OR_GREATER  
 Eşit veya daha fazla kesme noktası geçişi sayısı stilini ayarlar. Kesme noktasına, kesme noktası isabet sayısını geçişi sayısından büyük veya eşit olduğunda tetiklenir.  
  
 BP_PASSCOUNT_MOD  
 Belirtir bir modül geçiş sayısı. Örneğin, geçiş sayısı türü ise `BP_PASSCOUNT_MOD` ve geçişi sayısı değeri 4, isabet sayısı 4'ün katı her zaman kesme noktası ateşlenir.  
  
## <a name="remarks"></a>Açıklamalar  
 İçin kullanılan `stylePassCount` üyesi [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md) sırayla üyesi yapısı [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) ve [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md) yapıları.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)   
 [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)   
 [BP_REQUEST_INFO2](../../../extensibility/debugger/reference/bp-request-info2.md)