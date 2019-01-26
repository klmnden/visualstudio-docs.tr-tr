---
title: Başlatma tabanlı ek | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, launching
- debug engines, attaching to programs
ms.assetid: 362f00ac-1909-4a3a-bacb-c0ceb5549816
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fa0f03c37b92366e9872cbd170605a385aabdd1a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54975861"
---
# <a name="launch-based-attachment"></a>Başlatma tabanlı ek
Başlatma tabanlı ek bir program için otomatik olarak gerçekleşir. SDM tarafından program barındırma işlemi başlatıldığında, başlatma tabanlı ek el ile ek yöntemi için benzer bir yolu izler. Bilgi için [programa ekleme](../../extensibility/debugger/attaching-to-the-program.md).  
  
## <a name="the-attaching-process"></a>Düğmelere işlemi  
 İkisi arasındaki temel fark aşağıdaki olaylar dizisi olan **Ekle** gibi çağırın:  
  
1.  Gönderme bir **IDebugEngineCreateEvent2** SDM olay nesnesiyle. Ayrıntılar için bkz [olayları göndermek](../../extensibility/debugger/sending-events.md).  
  
2.  Çağrı `IDebugProgram2::GetProgramId` metodunda **IDebugProgram2** arabirimi geçirilen **iliştirme** yöntemi.  
  
3.  Gönder bir **IDebugProgramCreateEvent2** SDM bildirmek üzere olay nesnesi, yerel **IDebugProgram2** nesne program için DE göstermek için oluşturuldu.  
  
4.  Gönderme bir [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) SDM başlatılan işlem için yeni bir iş parçacığı oluşturulduğunu bildirmek üzere olay nesnesi.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Gerekli olayları gönderme](../../extensibility/debugger/sending-the-required-events.md)   
 [Bir program görüntüde hata ayıklamayı etkinleştir](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)