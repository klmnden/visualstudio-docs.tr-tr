---
title: Kesme noktasına ulaşma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], hitting breakpoints
- breakpoints, hitting
ms.assetid: a77816e3-b15b-46a0-90cd-be7242e4d6c9
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 728258dc363f906e005c654909cb86fd782824a9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53935638"
---
# <a name="hit-a-breakpoint"></a>Bir kesme noktası isabet
Aşağıdaki bölümde, çalışıyor veya atlama hata ayıklama altyapısı (DE) bir kesme noktasına ulaştığında işlemi açıklanmaktadır:  
  
## <a name="troubleshoot-a-hit-breakpoint"></a>Kesme noktası isabet sorunlarını giderme  
  
1.  DE gönderen bir [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md) olarak arabirim bir **EVENT_SYNC_STOP**.  
  
2.  Oturum hata ayıklama Yöneticisi (SDM) çağıran [IDebugBreakpointEvent2:::EnumBreakpoints](../../extensibility/debugger/reference/idebugbreakpointevent2-enumbreakpoints.md) kesme noktası isabet aldığından alınamıyor.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Hata ayıklayıcı olayları çağırma](../../extensibility/debugger/calling-debugger-events.md)