---
title: Kural kümeleri kullanma Kod Analizi kurallarını gruplandırmak için | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.rulesets.learnmore
helpviewer_keywords:
- code analysis, rule sets
ms.assetid: ed0f3a2a-1516-42e2-92de-b8986dc75d42
caps.latest.revision: 38
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1da32bd3626af60de56c0a8544753f95988773e9
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54759205"
---
# <a name="using-rule-sets-to-group-code-analysis-rules"></a>Kod Çözümleme Kurallarını Gruplandırmak için Kural Kümeleri Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kod Analizi yapılandırdığınızda [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], veya [!INCLUDE[vsPro](../includes/vspro-md.md)], Microsoft yerleşik bir listeden seçebilirsiniz *kural kümeleri*. Bir kural kümesi, hedeflenen sorunları ve belirli koşullar belirleyen kod analizi kuralları mantıksal bir gruplandırmasıdır. Örneğin, kod genel kullanıma açık API'leri taramak için tasarlanmış bir kural kümesi uygulayabilirsiniz veya içeren yalnızca en az önerilen kurallar kural kümesi uygulayabilirsiniz. İçeren tüm kurallar kural kümesi de uygulayabilirsiniz.  
  
 Bir kural ekleme veya silme kuralları veya kuralları değiştirerek görünmesini kümesini özelleştirebilirsiniz **hata listesi** uyarıları veya hataları olarak penceresi. Özel kural kümeleri belirli geliştirme ortamınızı gereksinimini karşılayabilir. Kural kümesi sayfası, bir kural kümesi özelleştirdiğinizde, arama ve filtreleme süreçte yardımcı olacak araçlar sağlar.  
  
## <a name="common-tasks"></a>Ortak Görevler  
  
|Görev|İlgili içerik|  
|----------|---------------------|  
|**Uygulamalı alıştırma alın:** Basit bir .NET Framework uygulama sorunlarını bulmak ve özel bir kural belirtmek için kod çözümleme araçları kullanın.|-   [İzlenecek yol: Yapılandırma ve bir özel kural kullanarak ayarlayın](../code-quality/walkthrough-configuring-and-using-a-custom-rule-set.md)|  
|**Bir proje için Kod Analizi yapılandırın:** Bir proje, Web sitesi veya çözüm için ayarlanmış mevcut bir kuralı seçin.|-   [Nasıl Yapılır: Yönetilen kod projesi için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-a-managed-code-project.md)<br />-   [Çalıştırılacak C++ kurallarını belirtmek için kural kümeleri kullanma](../code-quality/using-rule-sets-to-specify-the-cpp-rules-to-run.md)<br />-   [Nasıl Yapılır: Bir ASP.NET Web uygulaması için kod çözümlemesini yapılandırma](../code-quality/how-to-configure-code-analysis-for-an-aspnet-web-application.md)<br />-   [Nasıl Yapılır: Bir çözümde birden çok proje için kural kümesi belirtme](../code-quality/how-to-specify-managed-code-rule-sets-for-multiple-projects-in-a-solution.md)|  
|**Bir kural kümesi Özelleştir:** Projenize uygulanacak kuralları belirtin.|-   [Özel kural kümeleri oluşturma](../code-quality/creating-custom-code-analysis-rule-sets.md)|  
|**Yerleşik kural kümelerini anlayın:** Yerleşik kural kümelerini oluşturan kod analizi kuralları görüntüleyin.|-   [Kod çözümleme kural kümesi başvurusu](../code-quality/code-analysis-rule-set-reference.md)|  
|**Kod Analizi Team Foundation Server ile tümleştirin:** [!INCLUDE[esprtfs](../includes/esprtfs-md.md)] ilkelerini etkinleştirmek, tüm kod iadesi Kod Analizi standartları ortak bir dizi karşıladığından emin olmak geliştirme ekipleri iade.|-   [Nasıl Yapılır: İade takım projesi ilkesiyle kod proje kural kümelerini eşitleme](../code-quality/how-to-synchronize-code-project-rule-sets-with-team-project-check-in-policy.md)|
