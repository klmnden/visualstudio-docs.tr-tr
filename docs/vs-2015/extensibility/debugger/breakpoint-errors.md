---
title: Kesme noktası hataları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, errors
- debugging [Debugging SDK], breakpoint errors
- errors [Debugging SDK]
ms.assetid: 79221c6b-a924-4c8e-a778-e312e4e0c0c8
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: c9400e28e54476b027e6d57e97d7d0178511a10a
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755515"
---
# <a name="breakpoint-errors"></a>Kesme Noktası Hataları
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Aşağıdaki koda bağlamak bir kesme noktası girişiminde bulunduğunda işlemini açıklar ancak başarısız olur:  
  
## <a name="troubleshooting-a-breakpoint-error"></a>Bir kesme noktası hatası sorunlarını giderme  
  
1.  Hata ayıklama altyapısı (DE) gönderen bir [IDebugBreakpointErrorEvent2](../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md) oturum hata ayıklama Yöneticisi (SDM).  
  
2.  SDM çağrıları [IDebugBreakpointErrorEvent2::GetErrorBreakpoint](../../extensibility/debugger/reference/idebugbreakpointerrorevent2-geterrorbreakpoint.md) (IDebugErrorBreakpoint2 ** `ppErrorBP`) hata kesme noktası alınamıyor.  
  
3.  SDM çağrıları [IDebugErrorBreakpoint2::GetPendingBreakpoint](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getpendingbreakpoint.md) hata kesme noktası kaynaklandığı bekleyen kesme noktasının alınamıyor.  
  
4.  SDM çağrıları [IDebugErrorBreakpoint2::GetBreakpointResolution](../../extensibility/debugger/reference/idebugerrorbreakpoint2-getbreakpointresolution.md) bağlamak için hata kesme noktası başarısız olmasının nedeni alınamıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)
