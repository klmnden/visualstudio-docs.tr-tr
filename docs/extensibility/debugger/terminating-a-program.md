---
title: Program sonlandırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- programs, termination events
- debugging [Debugging SDK], terminating a program
ms.assetid: eedda0a3-5e05-44fe-841d-a2f4866ac72d
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 28be8f34602a3a175c40d630463686f0ca99c919
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53958858"
---
# <a name="terminating-a-program"></a>Program sonlandırma
Aşağıdaki bölümde, bir iş parçacığı ile tek bir programın sonlandırılması açıklanmaktadır.  
  
## <a name="termination-process"></a>Sonlandırma işlemi  
  
1. DE gönderen bir [IDebugThreadDestroyEvent2](../../extensibility/debugger/reference/idebugthreaddestroyevent2.md) ile geçerli bir [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md).  
  
2. DE gönderen bir [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) ile geçerli bir [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md).  
  
   IDE tasarım moduna geçer. Hata ayıklama altyapısı veya çalışma zamanı ortamı çağrıları [IDebugPortNotify2::RemoveProgramNode](../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md) bağlantı noktasından programı kaldırın.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)