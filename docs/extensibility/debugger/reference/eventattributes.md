---
title: EVENTATTRIBUTES | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- EVENTATTRIBUTES
helpviewer_keywords:
- EVENTATTRIBUTES enumeration
ms.assetid: 04db10f7-df31-4464-98e8-b3777428179e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 60bd3296ed3c610b238abf00d90781b6e0067d72
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54953831"
---
# <a name="eventattributes"></a>EVENTATTRIBUTES
Olay öznitelikleri belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum enum_EVENTATTRIBUTES {   
   EVENT_ASYNCHRONOUS          = 0x0000,  
   EVENT_SYNCHRONOUS           = 0x0001,  
   EVENT_STOPPING              = 0x0002,  
   EVENT_ASYNC_STOP            = 0x0002,  
   EVENT_SYNC_STOP             = 0x0003,  
   EVENT_IMMEDIATE             = 0x0004,  
   EVENT_EXPRESSION_EVALUATION = 0x0008  
};  
typedef DWORD EVENTATTRIBUTES;  
```  
  
```csharp  
public enum enum_EVENTATTRIBUTES {   
   EVENT_ASYNCHRONOUS          = 0x0000,  
   EVENT_SYNCHRONOUS           = 0x0001,  
   EVENT_STOPPING              = 0x0002,  
   EVENT_ASYNC_STOP            = 0x0002,  
   EVENT_SYNC_STOP             = 0x0003,  
   EVENT_IMMEDIATE             = 0x0004,  
   EVENT_EXPRESSION_EVALUATION = 0x0008  
};  
```  
  
## <a name="members"></a>Üyeler  
 EVENT_ASYNCHRONOUS  
 Zaman uyumsuz bir olaydır ve olay yanıt gerekli olduğunu gösterir.  
  
 EVENT_SYNCHRONOUS  
 Olay zaman uyumlu olduğunu gösterir; yoluyla yanıt [ContinueFromSynchronousEvent](../../../extensibility/debugger/reference/idebugengine2-continuefromsynchronousevent.md).  
  
 EVENT_STOPPING  
 Durdurma olay olduğunu gösterir. İle birleştirilmelidir `EVENT_ASYNCHRONOUS` veya `EVENT_SYNCHRONOUS`.  
  
 EVENT_ASYNC_STOP  
 Zaman uyumsuz durdurma olay gösterir. Şu anda bu tür bir olay. Bu bayrağı yalnızca bir yer tutucudur.  
  
 EVENT_SYNC_STOP  
 Zaman uyumlu durdurma olay gösterir (bir birleşimini `EVENT_SYNCHRONOUS` ve `EVENT_STOPPING`). Durdurma olay gönderdiğinde, bu değer bir hata ayıklama altyapısı (DE) kullanılır. Yanıt için bir çağrı yoluyla yapılan [yürütme](../../../extensibility/debugger/reference/idebugprogram2-execute.md), [adım](../../../extensibility/debugger/reference/idebugprogram2-step.md), veya [devam](../../../extensibility/debugger/reference/idebugprogram2-continue.md).  
  
 EVENT_IMMEDIATE  
 IDE hemen ve eşzamanlı olarak gönderilen bir olay gösterir. Bu bayrak, gibi diğer bayraklar birlikte `EVENT_ASYNCHRONOUS`, `EVENT_SYNCHRONOUS`, veya `EVENT_SYNC_STOP` olay ve yanıt mekanizmasını (varsa) bilinir olgu türünü belirtmek için.  
  
 EVENT_EXPRESSION_EVALUATION  
 İfade değerlendirmesinin sonucu olayıdır.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu değerleri geçirilir `dwAttrib` parametresinin [olay](../../../extensibility/debugger/reference/idebugeventcallback2-event.md) yöntemi.  
  
 Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: msdbg.h  
  
 Ad alanı: Microsoft.VisualStudio.Debugger.Interop  
  
 Derleme: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)   
 [ContinueFromSynchronousEvent](../../../extensibility/debugger/reference/idebugengine2-continuefromsynchronousevent.md)   
 [Event](../../../extensibility/debugger/reference/idebugeventcallback2-event.md)