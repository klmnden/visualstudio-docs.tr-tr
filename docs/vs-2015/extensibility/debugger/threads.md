---
title: İş parçacıkları | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- debugging [Debugging SDK], threads
- threading [Debugging SDK]
ms.assetid: 2243d24a-c3d2-41d1-abbb-6db21a2db9ee
caps.latest.revision: 14
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: bda2bc0c79f766b4c6322850a22d2a830499ff58
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49188280"
---
# <a name="threads"></a>İş Parçacıkları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı mimarisi bakımından bir **iş parçacığı**:  
  
-   Temel hesaplama birimidir. Bir iş parçacığı bağlamı içinde kendi yönergeler tek bir kod bağlamdan sonraki taşıma, bir tek bir çağrı yığınının sıralı olarak yürütür.  
  
-   Kendisi ve bunu, çalıştığı adlı, askıya ve sürdürüldü program tanımlayabilirsiniz. Bir iş parçacığı, ayrıca kendi ilişkili yığın çerçevelerini numaralandırabilirsiniz ve bazı koşullar altında başka bir yığın çerçevesine taşınabilir. Bir yığın çerçevesi bağlamında göz önünde bulundurulduğunda, bir iş parçacığı, ilişkili mantıksal iş parçacığı varsa döndürebilir. Bir iş parçacığı IDE iş parçacıkları penceresinde görüntülenen bir askıya alma sayımı gibi özellikleri vardır.  
  
-   Tarafından temsil edilen bir [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md) arabirimi, genellikle bir hata ayıklama altyapısı (DE) veya bir programı yürütme söz konusu kümelerdeki sanal makine tarafından oluşturuldu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Programlar](../../extensibility/debugger/programs.md)   
 [Yığın çerçeveleri](../../extensibility/debugger/stack-frames.md)   
 [Hata ayıklama altyapısı](../../extensibility/debugger/debug-engine.md)   
 [Hata ayıklayıcı kavramları](../../extensibility/debugger/debugger-concepts.md)   
 [Oturum Hata Ayıklama Yöneticisi](../../extensibility/debugger/session-debug-manager.md)

