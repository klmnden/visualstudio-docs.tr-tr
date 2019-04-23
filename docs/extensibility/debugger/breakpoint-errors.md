---
title: Kesme noktası hataları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, errors
- debugging [Debugging SDK], breakpoint errors
- errors [Debugging SDK]
ms.assetid: 79221c6b-a924-4c8e-a778-e312e4e0c0c8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a539894b0564d8c89461886558eb35c04c8af83c
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60074589"
---
# <a name="breakpoint-errors"></a>Kesme noktası hataları
Aşağıdaki koda bağlamak bir kesme noktası girişiminde bulunduğunda işlemini açıklar ancak başarısız olur.

## <a name="troubleshoot-a-breakpoint-error"></a>Bir kesme noktası hatası sorunlarını giderme

1. Hata ayıklama altyapısı (DE) gönderen bir [IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md) oturum hata ayıklama Yöneticisi (SDM).

2. SDM çağrıları [IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md) (IDebugErrorBreakpoint2 ** `ppErrorBP`) hata kesme noktası alınamıyor.

3. SDM çağrıları [IDebugErrorBreakpoint2::GetPendingBreakpoint](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md) hata kesme noktası kaynaklandığı bekleyen kesme noktasının alınamıyor.

4. SDM çağrıları [IDebugErrorBreakpoint2::GetBreakpointResolution](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md) bağlamak için hata kesme noktası başarısız olmasının nedeni alınamıyor.

## <a name="see-also"></a>Ayrıca bkz.
- [Hata ayıklayıcısı olaylarını çağırma](../../extensibility/debugger/calling-debugger-events.md)