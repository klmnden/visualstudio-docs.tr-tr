---
title: Hata ayıklama Adımlama seçenekleri (eski) | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
helpviewer_keywords:
- branch stepping
- stepping, options in workflow debugging
- debugging, stepping options
- debugging workflows, stepping options
- instance stepping
ms.assetid: 3e9e3041-68c7-4f16-9bd6-da5e5144744b
caps.latest.revision: 5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: b1f0761ba750146ce7f8cc52e6992dae689f7779
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754855"
---
# <a name="debug-stepping-options-legacy"></a>Hata Ayıklama Adımlama Seçenekleri (Eski)
Bu konu, hata ayıklamak açıklar [!INCLUDE[wf](../includes/wf-md.md)] eşzamanlı etkinliğin eski uygulamaları [!INCLUDE[wfd1](../includes/wfd1-md.md)]. Eski kullanın [!INCLUDE[wfd2](../includes/wfd2-md.md)] hedeflemek gerektiğinde [!INCLUDE[netfx35_long](../includes/netfx35-long-md.md)] veya [!INCLUDE[vstecwinfx](../includes/vstecwinfx-md.md)].  
  
 Ne zaman hata ayıklamasını yaptığınız gibi eş zamanlı yürütme olan eski etkinlikler **ParallelActivity** veya **ConditionedActivityGroup**, kodunuzda adım adım ilerleyin için aşağıdaki iki seçenekten birini kullanabilirsiniz .  
  
- **Adımlama dal.** Adım adım ve belirli bir dala bileşik bir etkinlik gibi hata ayıklama Adımlama bu modu sağlar **ParallelActivity** veya **ConditionalActivityGroup** etkinlik. Hata ayıklamak için bu seçeneği kullandığınızda, denetiminde bir değişikliği eş zamanlı yürütme iş akışındaki diğer etkinliklerin nedeniyle oluştuğunu olduğunu fark etmez. Hata ayıklayıcı tek adımlarında size etkinlikler, diğer etkinlikler iş akışı ile eşzamanlı olarak yürütülmesi sırasında şu anda seçili dal. Örneğin, varsayılan olarak, en soldaki dalda bir **ParallelActivity** etkinliği ve ilk alt etkinliğini bir **ConditionedActivityGroup** etkinliği atlamak için kullanılır. Kullanıcı diğer dal ya da alt etkinlik hata ayıklama ilgileniyor, açık bir kesme noktası, dal ya da alt etkinlik yerleştirilmelidir. Adımlama, kesme noktası tetiklendiğinde dalında Gerçekleştirdiğim eder.  
  
- **Adımlama örneği.** Bu mod, Adımlama, adım adım ilerleyin ve etkinliklerini iş akışı içinde eşzamanlı olarak yürütülmesi hata ayıklama olanak tanır. Bu seçenek ile bir değişiklik denetimi etkinlikleri iş akışı içinde çalıştırmak aynı anda çalıştırılırken oluştuğunu fark edeceksiniz.  
  
  Varsayılan olarak, dal Adımlama seçeneğini seçtiyseniz ve kullanıcılar eski iş akışı hata ayıklama sırasında iki seçenek arasında geçiş yapabilir.  
  
  Eski durum makine iş akışları hata ayıklama sırasında seçeneği Adımlama örneği seçmeniz gerekir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Eski iş akışlarında hata ayıklama](../workflow-designer/debugging-legacy-workflows.md)   
 [Nasıl yapılır: Hata ayıklama Adımlama seçeneğini (eski) değiştirme](../workflow-designer/how-to-change-the-debug-stepping-option-legacy.md)