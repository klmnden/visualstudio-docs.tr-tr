---
title: Kod çözümleme sorunlarını giderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: troubleshooting
ms.assetid: 61c7e44d-2780-4df5-9bcb-49e40c1152fc
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 047866f958ebfe6de20d5f7760b72eaab4135ef1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62551480"
---
# <a name="troubleshooting-code-analysis-issues"></a>Kod Analizi Sorunlarını Giderme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu konu aşağıdaki Visual Studio Kod Analizi sorunlarına yönelik sorun giderme bilgileri içerir.  
  
- [Bir Visual Studio 2010 kural kümesi olan önceki Visual Studio sürümlerinde yansıtılan olmayan değişiklikler](#ChildRuleSetChangesInPreviousVersions)  
  
## <a name="ChildRuleSetChangesInPreviousVersions"></a> Bir Visual Studio 2010 kural kümesi olan önceki Visual Studio sürümlerinde yansıtılan olmayan değişiklikler  
 Bir kural kümesi oluşturduğunuzda [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)] bir alt kural kümesi içeren, bir değişiklik alt kural kümesi için Kod Analizi yürütmeleri Visual Studio'nun önceki bir sürümünü kullanan bilgisayarlarda uygulanmayabilir. Bu sorunu çözmek için bir yeniden yazma alt kural kümesini içeren kural kümesi olan üst kural kümesinin zorlaması gerekir.  
  
1. Açık üst kural kümesinde [!INCLUDE[vs_dev10_long](../includes/vs-dev10-long-md.md)].  
  
2. Ekleme veya bir kuralı kaldırma gibi bir değişiklik yapın ve sonra kural kümesi kaydedin.  
  
3. Kural kümesi yeniden, değişikliğini tersine çevirebilir ve kural kümesi yeniden kaydedin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Uygulama kalitesini analiz etme](../code-quality/analyzing-application-quality-by-using-code-analysis-tools.md)   
 [Yönetilen kod kalitesini analiz etme](../code-quality/analyzing-managed-code-quality-by-using-code-analysis.md)   
 [Kod Analizi Kurallarını Gruplandırmak için Kural Kümeleri Kullanma](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)
