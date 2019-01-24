---
title: Sonlandırma ve ayırma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- programs, termination events
- debug engines, detaching from programs
ms.assetid: 268c1e51-6363-45d1-964c-1ab99bdfa4f9
caps.latest.revision: 8
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d92fe88826baf19ba66b200990aee7797e91f87b
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54793907"
---
# <a name="termination-and-detaching"></a>Sonlandırma ve Ayırma
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Aşağıdaki normal sonlandırması açıklar.  
  
## <a name="discussion"></a>Tartışma  
 Sonra [IDebugLoadCompleteEvent2](../../extensibility/debugger/reference/idebugloadcompleteevent2.md) veya [IDebugEntryPointEvent2](../../extensibility/debugger/reference/idebugentrypointevent2.md) arabirimi devam eder, hiçbir kesme noktaları, özel durumlar, çalışma zamanı hataları veya uygulamada hata ayıklaması için sonsuz döngüler varsa hata ayıklanan programa tamamlanana kadar çalışır. Normal sonlandırması budur.  
  
 Göndermeniz gerekir bir [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) normal sonlandırması uygulamak için. Bu uygulama gerektirir [IDebugProgramDestroyEvent2::GetExitCode](../../extensibility/debugger/reference/idebugprogramdestroyevent2-getexitcode.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Özel Hata Ayıklama Altyapısı Oluşturma](../../extensibility/debugger/creating-a-custom-debug-engine.md)
