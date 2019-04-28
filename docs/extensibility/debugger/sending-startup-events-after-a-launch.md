---
title: Başlatmadan sonra Başlangıç olaylarını gönderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], startup events
ms.assetid: 306ea0b4-6d9e-4871-8d8d-a4032d422940
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2f82ab0b28c1052a0d6a4cb0b2db7e6bbaaba8cc
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63420592"
---
# <a name="send-startup-events-after-a-launch"></a>Başlatmadan sonra Başlangıç olaylarını gönderme
Programın hata ayıklama altyapısı (DE) bağlandıktan sonra hata ayıklama oturumu başlatma olay serisi olarak gönderir.

 Hata ayıklama oturumu gönderildi başlangıç olayları şunlardır:

- Bir altyapı oluşturma olayı.

- Bir program oluşturma olayı.

- Oluşturma ve modül yükleme olayları iş parçacığı.

- Kod yüklenmiş ve çalıştırılmaya hazır olduğunda, ancak herhangi bir kod yürütülmeden önce gönderilen yük gibi tam bir olay.

  > [!NOTE]
  > Bu olay devam ettirildiğinde, genel değişkenler başlatılır ve başlangıç yordamları çalıştırın.

- Diğer olası iş parçacığı oluşturma ve modül yükleme olayları.

- Program, ana girdi noktası gibi ulaştı sinyalleri bir giriş noktası olayı **ana** veya `WinMain`. Zaten çalışan bir programa DE bağlanıyorsa bu olay genellikle gönderilen değil.

  Programlı olarak DE oturum hata ayıklama Yöneticisi (SDM) ilk kez gönderir bir [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) bir altyapı oluşturma olayı temsil eder, arabirim, arkasından bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) , bir program oluşturma olayı temsil eder.

  Bu olaylar, genellikle bir veya daha fazla izlendiğini [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) iş parçacığı oluşturma olayları ve [IDebugModuleLoadEvent2](../../extensibility/debugger/reference/idebugmoduleloadevent2.md) Modül yükleme olayları.

  Yüklenmiş ve çalıştırılmaya hazır kodudur, ancak herhangi bir kod yürütülmeden önce DE SDM gönderir. bir [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) yük tamamlama olayı. Son olarak, program zaten çalışmıyorsa DE gönderdiği bir [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) program, ana girdi noktası sınırına ulaştı ve hata ayıklama için hazır olarak giriş noktası olayı.

## <a name="see-also"></a>Ayrıca bkz.
- [Yürütme denetimi](../../extensibility/debugger/control-of-execution.md)
- [Hata ayıklama görevleri](../../extensibility/debugger/debugging-tasks.md)