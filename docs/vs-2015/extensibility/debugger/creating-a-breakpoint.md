---
title: Bir kesme noktası oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, creating
- debugging [Debugging SDK], creating breakpoints
ms.assetid: 6f9f87bb-192e-45e0-9a7a-ffe729e87f7d
caps.latest.revision: 9
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 078b0a46662930f2a8624c1b0d10510728a811d6
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54799474"
---
# <a name="creating-a-breakpoint"></a>Kesme Noktası Oluşturma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir kesme noktası oluşturma işlemi açıklanmaktadır.  
  
## <a name="methods-in-breakpoint-creation"></a>Kesme noktası oluşturma yöntemleri  
 Bir kesme noktası bağlanması gereken bir modül yüklendiğinde oturum hata ayıklama Yöneticisi (SDM) aşağıdaki yöntemleri çağırır:  
  
1.  [IDebugPendingBreakpoint2::Enable](../../extensibility/debugger/reference/idebugpendingbreakpoint2-enable.md)  
  
2.  [IDebugPendingBreakpoint2::Virtualize](../../extensibility/debugger/reference/idebugpendingbreakpoint2-virtualize.md)  
  
3.  [IDebugPendingBreakpoint2::CanBind](../../extensibility/debugger/reference/idebugpendingbreakpoint2-canbind.md)  
  
    > [!NOTE]
    >  **CanBind** yalnızca bir kullanıcı kesme noktaları penceresinde kesme noktası yaptığında çağrılır.  
  
4.  [IDebugPendingBreakpoint2::Bind](../../extensibility/debugger/reference/idebugpendingbreakpoint2-bind.md)  
  
5.  [IDebugPendingBreakpoint2::EnumBoundBreakpoints](../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)
