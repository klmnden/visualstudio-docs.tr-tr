---
title: Başlatmadan sonra Başlangıç olaylarını gönderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], startup events
ms.assetid: 306ea0b4-6d9e-4871-8d8d-a4032d422940
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: caf36e6713e49bb1470cd720ba2d04f689abba43
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63436672"
---
# <a name="sending-startup-events-after-a-launch"></a>Başlatmadan Sonra Başlangıç Olaylarını Gönderme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Programın hata ayıklama altyapısı (DE) bağlandıktan sonra hata ayıklama oturumu başlatma olay serisi olarak gönderir.  
  
 Hata ayıklama oturumu gönderildi başlangıç olayları aşağıdakileri içerir:  
  
- Bir altyapı oluşturma olayı.  
  
- Bir program oluşturma olayı.  
  
- Oluşturma ve modül yükleme olayları iş parçacığı.  
  
- Kod yüklenmiş ve çalıştırılmaya hazır olduğunda, ancak herhangi bir kod yürütülmeden önce gönderilen bir yük tamamlama olayı  
  
  > [!NOTE]
  > Bu olay devam ettirildiğinde, genel değişkenler başlatılır ve başlangıç yordamları çalıştırın.  
  
- Diğer olası iş parçacığı oluşturma ve modül yükleme olayları.  
  
- Program, ana girdi noktası gibi ulaştı sinyalleri bir giriş noktası olayı **ana** veya `WinMain`. Zaten çalışan bir programa DE bağlanıyorsa bu olay genellikle gönderilmez.  
  
  Programlı olarak DE oturum hata ayıklama Yöneticisi (SDM) ilk kez gönderir bir [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) bir altyapı oluşturma olayı temsil eder, arabirim, arkasından bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) , bir program oluşturma olayı temsil eder.  
  
  Bu genellikle bir veya daha fazla takip [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) iş parçacığı oluşturma olayları ve [IDebugModuleLoadEvent2](../../extensibility/debugger/reference/idebugmoduleloadevent2.md) Modül yükleme olayları.  
  
  Yüklenmiş ve çalıştırılmaya hazır kodudur, ancak herhangi bir kod yürütülmeden önce DE SDM gönderir. bir [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) yük tamamlama olayı. Son olarak, program zaten çalışmıyorsa DE gönderdiği bir [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) program, ana girdi noktası sınırına ulaştı ve hata ayıklama için hazır olarak giriş noktası olayı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Yürütme denetimi](../../extensibility/debugger/control-of-execution.md)   
 [Hata Ayıklama Görevleri](../../extensibility/debugger/debugging-tasks.md)
