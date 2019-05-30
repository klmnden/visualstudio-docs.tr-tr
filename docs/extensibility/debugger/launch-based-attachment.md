---
title: Başlatma tabanlı ek | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debug engines, launching
- debug engines, attaching to programs
ms.assetid: 362f00ac-1909-4a3a-bacb-c0ceb5549816
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 638eaea19b4f21e749fbd3db845f18eb573420f2
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66344155"
---
# <a name="launch-based-attachment"></a>Başlatma tabanlı ek
Başlatma tabanlı ek bir program için otomatik olarak gerçekleşir. SDM tarafından program barındırma işlemi başlatıldığında, başlatma tabanlı ek el ile ek yöntemi için benzer bir yolu izler. Bilgi için [programa ekleme](../../extensibility/debugger/attaching-to-the-program.md).

## <a name="the-attaching-process"></a>Düğmelere işlemi
 İkisi arasındaki temel fark aşağıdaki olaylar dizisi olan **Ekle** gibi çağırın:

1. Gönderme bir **IDebugEngineCreateEvent2** SDM olay nesnesiyle. Ayrıntılar için bkz [olayları göndermek](../../extensibility/debugger/sending-events.md).

2. Çağrı `IDebugProgram2::GetProgramId` metodunda **IDebugProgram2** arabirimi geçirilen **iliştirme** yöntemi.

3. Gönder bir **IDebugProgramCreateEvent2** SDM bildirmek üzere olay nesnesi, yerel **IDebugProgram2** nesne program için DE göstermek için oluşturuldu.

4. Gönderme bir [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) SDM başlatılan işlem için yeni bir iş parçacığı oluşturulduğunu bildirmek üzere olay nesnesi.

## <a name="see-also"></a>Ayrıca bkz.
- [Gerekli olayları gönderme](../../extensibility/debugger/sending-the-required-events.md)
- [Bir program görüntüde hata ayıklamayı etkinleştir](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)