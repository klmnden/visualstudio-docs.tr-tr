---
title: Kesme modunda Adımlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- break mode, stepping
- stepping, in break mode
- debugging [Debugging SDK], stepping in break mode
ms.assetid: b08dc8ee-6c63-4462-a097-6f525cfbb35a
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 482d7131692c1e22483c80f4b4bb22e07a6caf1a
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60065928"
---
# <a name="stepping-in-break-mode"></a>Kesme Modunda Adımlama
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Hata ayıklayıcı kesme modundayken ve kodunuz içinde adım adım gerekir oluşan süreci açıklanmaktadır:  
  
## <a name="stepping-process"></a>İşlem Adımlama  
  
1. Çağrı [IDebugProgram2::Step](../../extensibility/debugger/reference/idebugprogram2-step.md) ile [STEPKIND](../../extensibility/debugger/reference/stepkind.md) ve [STEPUNIT](../../extensibility/debugger/reference/stepunit.md) bir adımı yürütmeye yönelik bağımsız değişkenleri.  
  
2. Bu adım tamamlandığında, gönderme bir [IDebugStepCompleteEvent2](../../extensibility/debugger/reference/idebugstepcompleteevent2.md) durdurma olay olarak.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Hata Ayıklayıcısı Olaylarını Çağırma](../../extensibility/debugger/calling-debugger-events.md)
