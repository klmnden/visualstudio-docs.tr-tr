---
title: Kesme noktasını silme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- breakpoints, deleting
- debugging [Debugging SDK], deleting breakpoints
ms.assetid: 75a046cc-d20a-4c79-ad2d-1f18426ac5d0
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 42cd353c216c21d14c4f6592da809c72acdba664
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63409405"
---
# <a name="deleting-a-breakpoint"></a>Kesme Noktasını Silme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Aşağıdaki bir bekleyen kesme noktasının silerken işlemi açıklanmaktadır:  
  
## <a name="deletion-process"></a>Silme işlemi  
 Oturum hata ayıklama Yöneticisi (SDM) çağıran [IDebugPendingBreakpoint2::Delete](../../extensibility/debugger/reference/idebugpendingbreakpoint2-delete.md) ondan bağlı bekleyen kesme noktasının ve ilişkili tüm kesme noktalarını kaldırmak için yöntemi.  
  
> [!NOTE]
> Tek bir bağlı Kesme noktasının bir çağrı tarafından da silinebilir [IDebugBoundBreakpoint2::Delete](../../extensibility/debugger/reference/idebugboundbreakpoint2-delete.md).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)
