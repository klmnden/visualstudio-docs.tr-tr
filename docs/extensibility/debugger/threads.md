---
title: İş parçacıkları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], threads
- threading [Debugging SDK]
ms.assetid: 2243d24a-c3d2-41d1-abbb-6db21a2db9ee
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b15928e10d77a10d9ae8b2b684af02e3b370ce87
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56716018"
---
# <a name="threads"></a>İş Parçacıkları
Hata ayıklayıcı mimarisinde bir *iş parçacığı*:

-   Temel hesaplama birimidir. Bir iş parçacığı bağlamı içinde kendi yönergeler tek bir kod bağlamdan sonraki taşıma, bir tek bir çağrı yığınının sıralı olarak yürütür.

-   Kendisi ve, çalışan bir program tanımlayabilirsiniz. İş parçacıkları adlı askıya sürdürüldü ve. Bir iş parçacığı, ayrıca kendi ilişkili yığın çerçevelerini numaralandırabilirsiniz ve bazı koşullar altında başka bir yığın çerçevesine taşınabilir. Bir yığın çerçevesi bağlamında göz önünde bulundurulduğunda, bir iş parçacığı, ilişkili mantıksal iş parçacığı varsa döndürebilir. Bir iş parçacığı içinde görüntülenen bir askıya alma sayımı gibi özelliklere sahip **iş parçacıkları** IDE bir pencerenin.

-   Tarafından temsil edilen bir [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir programı yürütme söz konusu kümelerdeki sanal makine tarafından oluşturuldu.

## <a name="see-also"></a>Ayrıca bkz.
- [Programlar](../../extensibility/debugger/programs.md)
- [Yığın çerçeveleri](../../extensibility/debugger/stack-frames.md)
- [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)
- [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)
- [Oturum hata ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md)