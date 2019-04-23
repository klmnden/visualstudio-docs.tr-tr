---
title: İş parçacıkları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], threads
- threading [Debugging SDK]
ms.assetid: 2243d24a-c3d2-41d1-abbb-6db21a2db9ee
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 028ad25495ba01d9763c8bec3bbb9c4480d72ff8
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60054592"
---
# <a name="threads"></a>İş Parçacıkları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **iş parçacığı**:  
  
- Temel hesaplama birimidir. Bir iş parçacığı bağlamı içinde kendi yönergeler tek bir kod bağlamdan sonraki taşıma, bir tek bir çağrı yığınının sıralı olarak yürütür.  
  
- Kendisi ve bunu, çalıştığı adlı, askıya ve sürdürüldü program tanımlayabilirsiniz. Bir iş parçacığı, ayrıca kendi ilişkili yığın çerçevelerini numaralandırabilirsiniz ve bazı koşullar altında başka bir yığın çerçevesine taşınabilir. Bir yığın çerçevesi bağlamında göz önünde bulundurulduğunda, bir iş parçacığı, ilişkili mantıksal iş parçacığı varsa döndürebilir. Bir iş parçacığı IDE iş parçacıkları penceresinde görüntülenen bir askıya alma sayımı gibi özellikleri vardır.  
  
- Tarafından temsil edilen bir [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir programı yürütme söz konusu kümelerdeki sanal makine tarafından oluşturuldu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Programlar](../../extensibility/debugger/programs.md)   
 [Yığın çerçeveleri](../../extensibility/debugger/stack-frames.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Oturum Hata Ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md)
