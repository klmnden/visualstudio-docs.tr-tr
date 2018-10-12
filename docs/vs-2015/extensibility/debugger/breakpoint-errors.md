---
title: Kesme noktası hataları | Microsoft Docs
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
- breakpoints, errors
- debugging [Debugging SDK], breakpoint errors
- errors [Debugging SDK]
ms.assetid: 79221c6b-a924-4c8e-a778-e312e4e0c0c8
caps.latest.revision: 9
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 136b371b6d024a93e2a4cb4cadd792928db49800
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49197972"
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

