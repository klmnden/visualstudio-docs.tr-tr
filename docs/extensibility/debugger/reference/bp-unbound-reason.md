---
title: BP_UNBOUND_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BP_UNBOUND_REASON
helpviewer_keywords:
- BP_UNBOUND_REASON enumeration
ms.assetid: 939b6f9c-113b-471d-9f30-b03871af6285
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4d8dfc8e032eecc854a0572c8a7bd14b0c551df7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55028648"
---
# <a name="bpunboundreason"></a>BP_UNBOUND_REASON
Bir kesme noktası ilişkisiz nedeni sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_BP_UNBOUND_REASON {   
   BPUR_UNKNOWN           = 0x0000,  
   BPUR_CODE_UNLOADED     = 0x0002,  
   BPUR_BREAKPOINT_REBIND = 0x0003,  
   BPUR_BREAKPOINT_ERROR  = 0x0004  
};  
typedef DWORD BP_UNBOUND_REASON;  
```  
  
```csharp  
public enum enum_BP_UNBOUND_REASON {   
   BPUR_UNKNOWN           = 0x0000,  
   BPUR_CODE_UNLOADED     = 0x0002,  
   BPUR_BREAKPOINT_REBIND = 0x0003,  
   BPUR_BREAKPOINT_ERROR  = 0x0004  
};  
```  
  
## <a name="members"></a>Üyeler  
 BPUR_UNKNOWN  
 Bunun nedeni bilinmiyor.  
  
 BPUR_CODE_UNLOADED  
 Kesme noktasını içeren kod kaldırıldı.  
  
 BPUR_BREAKPOINT_REBIND  
 Farklı bir konuma kesme noktası yansıdı. Bu düzenlemeden sonra gerçekleşir ve kesme noktası hareket ettiğinde veya artık geçerli olmayan bir yola sahip bir dosya kesme noktasına bağlandığında işlemler devam edebilirsiniz.  
  
 BPUR_ BREAKPOINT_ERROR  
 Kesme noktasına bağlı sonra hata olarak değerlendirilir. Bu, koşullar artık geçerli olmayan yönetilen kesme noktaları için gerçekleşir.  
  
## <a name="remarks"></a>Açıklamalar  
 Tarafından döndürülen [GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md)