---
title: Başlatma tabanlı ek | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debug engines, launching
- debug engines, attaching to programs
ms.assetid: 362f00ac-1909-4a3a-bacb-c0ceb5549816
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 09a6b39bef9ba6af098bf92d779a490e22492209
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60044869"
---
# <a name="launch-based-attachment"></a>Başlatma Tabanlı Ek
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Başlatma tabanlı ek bir program için otomatik olarak gerçekleşir. SDM tarafından program barındırma işlemi başlatıldığında, başlatma tabanlı ek el ile ek yöntemi için benzer bir yolu izler. Bilgi için [programa ekleme](../../extensibility/debugger/attaching-to-the-program.md).  
  
## <a name="the-attaching-process"></a>Düğmelere işlemi  
 İkisi arasındaki temel fark aşağıdaki olaylar dizisi olan **Ekle** gibi çağırın:  
  
1. Gönderme bir **IDebugEngineCreateEvent2** SDM olay nesnesiyle. Ayrıntılar için bkz [olayları gönderme](../../extensibility/debugger/sending-events.md).  
  
2. Çağrı `IDebugProgram2::GetProgramId` metodunda **IDebugProgram2** arabirimi geçirilen **iliştirme** yöntemi.  
  
3. Gönder bir **IDebugProgramCreateEvent2** SDM bildirmek üzere olay nesnesi, yerel **IDebugProgram2** nesne program için DE göstermek için oluşturuldu.  
  
4. Gönderme bir [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) SDM başlatılan işlem için yeni bir iş parçacığı oluşturulduğunu bildirmek üzere olay nesnesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Gerekli olayları gönderme](../../extensibility/debugger/sending-the-required-events.md)   
 [Bir Programı Hataları Ayıklanacak Şekilde Etkinleştirme](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)
