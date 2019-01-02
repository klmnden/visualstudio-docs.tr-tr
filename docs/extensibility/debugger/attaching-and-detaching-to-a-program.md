---
title: Ekleme ve programdan ayırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, attaching to programs
- debug engines, detaching from programs
ms.assetid: 79dcbb9b-c7f8-40fc-8a00-f37fe1934f51
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7576b3c80ff80ec0c26234cf43682aca19a96a7b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53841605"
---
# <a name="attaching-and-detaching-to-a-program"></a>Ekleme ve programdan ayırma
Hata ayıklayıcısı ekleniyor, yöntemlerini ve olaylarını uygun özniteliklerle doğru sırasını gönderilmesi gerekir.  
  
## <a name="sequence-of-methods-and-events"></a>Dizi yöntemler ve olaylar  
  
1. Oturum hata ayıklama Yöneticisi (SDM) çağıran [OnAttach](../../extensibility/debugger/reference/idebugprogramnodeattach2-onattach.md) yöntemi.  
  
    Hata ayıklama altyapısı (DE) işlem modelini temel alan `IDebugProgramNodeAttach2::OnAttach` yöntemi ne olacağını belirler aşağıdaki yöntemlerden birini döndürür.  
  
    Varsa `S_FALSE` döndürülür, hata ayıklama altyapısı başarıyla bağlı program. Aksi takdirde, [iliştirme](../../extensibility/debugger/reference/idebugengine2-attach.md) yöntemi ekleme işlemi tamamlamak için çağrılır.  
  
    Varsa `S_OK` döndürülür, DE aynı işlemde SDM olarak yüklenecek. SDM aşağıdaki görevleri gerçekleştirir:  
  
   1.  Çağrıları [GetEngineInfo](../../extensibility/debugger/reference/idebugprogramnode2-getengineinfo.md) altyapısı DE almak için.  
  
   2.  Birlikte DE oluşturur.  
  
   3.  Çağrıları [ekleme](../../extensibility/debugger/reference/idebugengine2-attach.md).  
  
2. DE gönderen bir [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği.  
  
3. DE gönderen bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) ile SDM için bir `EVENT_SYNC` özniteliği. 
  
4. DE gönderen bir [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) ile SDM için bir `EVENT_SYNC_STOP` özniteliği.  
  
   Bir programdan ayırma basit, iki adımlı işlem aşağıdaki gibidir:  
  
5. SDM çağrıları [ayırma](../../extensibility/debugger/reference/idebugprogram2-detach.md).  
  
6. DE gönderen bir [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)