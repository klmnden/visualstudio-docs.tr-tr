---
title: Kesme noktasına ulaşma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- debugging [Debugging SDK], hitting breakpoints
- breakpoints, hitting
ms.assetid: a77816e3-b15b-46a0-90cd-be7242e4d6c9
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6d95abd66f248ca994d7712f1bf51519022de9d7
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66344041"
---
# <a name="hit-a-breakpoint"></a>Bir kesme noktası isabet
Aşağıdaki bölümde, çalışıyor veya atlama hata ayıklama altyapısı (DE) bir kesme noktasına ulaştığında işlemi açıklanmaktadır:

## <a name="troubleshoot-a-hit-breakpoint"></a>Kesme noktası isabet sorunlarını giderme

1. DE gönderen bir [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md) olarak arabirim bir **EVENT_SYNC_STOP**.

2. Oturum hata ayıklama Yöneticisi (SDM) çağıran [IDebugBreakpointEvent2:::EnumBreakpoints](../../extensibility/debugger/reference/idebugbreakpointevent2-enumbreakpoints.md) kesme noktası isabet aldığından alınamıyor.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcı olayları çağırma](../../extensibility/debugger/calling-debugger-events.md)