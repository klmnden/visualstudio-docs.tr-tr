---
title: Gerekli olayları gönderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], required events
ms.assetid: 08319157-43fb-44a9-9a63-50b919fe1377
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 45a65259c88eb9e8e946aa226eecc7cffa053552
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63415611"
---
# <a name="send-the-required-events"></a>Gerekli olayları gönderme
Gerekli olayları göndermek için bu yordamı kullanın.

## <a name="process-for-sending-required-events"></a>Gerekli olayları gönderme işlemi
 Aşağıdaki olaylar, bu sıralamayı oluşturmak bir hata ayıklama altyapısı, (DE) ve programa ekleme gereklidir:

1. Gönderme bir [IDebugEngineCreateEvent2](../../extensibility/debugger/reference/idebugenginecreateevent2.md) oturum hata ayıklama Yöneticisi (SDM) DE bir işlem bir veya daha fazla programlarında hata ayıklama başlatıldığında olay nesnesiyle.

2. Ayıklanacak programın bağlı olduğu zaman Gönder bir [IDebugProgramCreateEvent2](../../extensibility/debugger/reference/idebugprogramcreateevent2.md) SDM olay nesnesiyle. Bu olay altyapısı tasarımınızın bağlı olarak bir durdurma olay olabilir.

3. Program ekli ise işlem başlatıldığında Gönder bir [IDebugThreadCreateEvent2](../../extensibility/debugger/reference/idebugthreadcreateevent2.md) SDM yeni iş parçacığının IDE bildirmek üzere Olay nesnesiyle. Bu olay altyapısı tasarımınızın bağlı olarak bir durdurma olay olabilir.

4. Gönderme bir [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) ayıklanan programa tamamlanan yükleme veya programa ekleme tamamlandığında olduğunda SDM olay nesnesiyle. Bu olay bir durdurma olay olmalıdır.

5. Ayıklanacak uygulama başlatılmışsa, gönderme bir [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) çalıştırılmak üzere çalışma zamanı mimarisi kod ilk yönerge olduğunda SDM olay nesnesiyle. Bu olay her zaman bir durdurma olayıdır. Hata ayıklama oturumu Adımlama, IDE üzerinde bu olaya durdurur.

> [!NOTE]
> Birçok dil kodlarını başında genel başlatıcıların veya harici, önceden derlenmiş işlevleri (CRT kitaplığı veya _ana) kullanın. Programın hata ayıklamasını yaptığınız dilinin ilk giriş noktasından önce öğelerin bu türlerinden birini içeriyorsa, bu kodu çalıştırmak ve giriş noktası olayı gönderilir, kullanıcı giriş noktanız, gibi **ana** veya `WinMain`, olan ulaşıldı.

## <a name="see-also"></a>Ayrıca bkz.
- [Bir program görüntüde hata ayıklamayı etkinleştirme](../../extensibility/debugger/enabling-a-program-to-be-debugged.md)