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
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 729d37c36782cd1786124c94796f610931473f0c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62912755"
---
# <a name="terminating-a-program"></a>Program sonlandırma
Aşağıdaki bölümde, bir iş parçacığı ile tek bir programın sonlandırılması açıklanmaktadır.

## <a name="termination-process"></a>Sonlandırma işlemi

1. DE gönderen bir [IDebugThreadDestroyEvent2](../../extensibility/debugger/reference/idebugthreaddestroyevent2.md) ile geçerli bir [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md).

2. DE gönderen bir [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) ile geçerli bir [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md).

   IDE tasarım moduna geçer. Hata ayıklama altyapısı veya çalışma zamanı ortamı çağrıları [IDebugPortNotify2::RemoveProgramNode](../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md) bağlantı noktasından programı kaldırın.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)