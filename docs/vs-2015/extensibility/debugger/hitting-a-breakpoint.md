---
title: Kesme noktasına ulaşma | Microsoft Docs
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
- debugging [Debugging SDK], hitting breakpoints
- breakpoints, hitting
ms.assetid: a77816e3-b15b-46a0-90cd-be7242e4d6c9
caps.latest.revision: 8
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: a4b5805621d1fd58f6c5d39c779e6b87719edac6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49214987"
---
# <a name="hitting-a-breakpoint"></a>Kesme Noktasına Ulaşma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklama altyapısı (DE) bir kesme noktası çalıştıran veya Adımlama ulaştığında aşağıdaki işlem açıklanmaktadır:  
  
## <a name="troubleshooting-a-hit-breakpoint"></a>Kesme noktası isabet sorunlarını giderme  
  
1.  DE gönderen bir [IDebugBreakpointEvent2](../../extensibility/debugger/reference/idebugbreakpointevent2.md) olarak arabirim bir **EVENT_SYNC_STOP**.  
  
2.  Oturum hata ayıklama Yöneticisi (SDM) çağıran [IDebugBreakpointEvent2:::EnumBreakpoints](../../extensibility/debugger/reference/idebugbreakpointevent2-enumbreakpoints.md) kesme noktası isabet aldığından alınamıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)

