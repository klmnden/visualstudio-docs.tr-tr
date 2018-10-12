---
title: Program sonlandırma | Microsoft Docs
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
- programs, termination events
- debugging [Debugging SDK], terminating a program
ms.assetid: eedda0a3-5e05-44fe-841d-a2f4866ac72d
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: cf972e6bb38d9dcd2995814e885ceb0b071abe29
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49294690"
---
# <a name="terminating-a-program"></a>Program Sonlandırma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir iş parçacığı ile tek bir programın sonlandırılması bir açıklaması verilmiştir.  
  
## <a name="termination-process"></a>Sonlandırma işlemi  
  
1.  DE gönderen bir [IDebugThreadDestroyEvent2](../../extensibility/debugger/reference/idebugthreaddestroyevent2.md) ile geçerli bir [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md).  
  
2.  DE gönderen bir [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) ile geçerli bir [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md).  
  
 IDE tasarım moduna geçer. Hata ayıklama altyapısı veya çalışma zamanı ortamı çağrıları [IDebugPortNotify2::RemoveProgramNode](../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md) bağlantı noktasından programı kaldırın.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)

