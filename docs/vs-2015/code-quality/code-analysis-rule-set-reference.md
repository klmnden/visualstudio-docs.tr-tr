---
title: Kod çözümleme kural kümesi başvurusu | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
helpviewer_keywords:
- code analysis, rule sets
ms.assetid: 5874e854-e298-4d2e-bbe4-95e899d22587
caps.latest.revision: 45
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a1f91b352da5a41ec2ef81fb6067976073c787ef
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62576760"
---
# <a name="code-analysis-rule-set-reference"></a>Kod analizi kural kümesi başvurusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yönetilen kod projeleri için Kod Analizi yapılandırdığınızda [!INCLUDE[vsPreLong](../includes/vsprelong-md.md)], [!INCLUDE[vsUltLong](../includes/vsultlong-md.md)], veya [!INCLUDE[vsPro](../includes/vspro-md.md)]yerleşik bir listesi sunulur *kural kümeleri*. Ya da standar kural kümelerinden birini kullanabilir veya bir kural kümesini proje gereksinimlerinizi karşılayacak şekilde özelleştirebilirsiniz.  
  
## <a name="available-rule-sets"></a>Kullanılabilir kural kümeleri  
 Aşağıdaki tabloda, varsayılan kural kümelerini listeler:  
  
|||  
|-|-|  
|[Tüm Kurallar kural kümesi](../code-quality/all-rules-rule-set.md)|Bu kural kümesi, tüm kurallar içerir. Bu kural kümesi çalıştıran çok sayıda rapor uyarılarına neden olabilir. Bu kural kümesini kodunuzda tüm sorunların kapsamlı bir resim almak için kullanın. Bu, hangisinin daha odaklı kural kümeleri projelerinizi çalıştırmak için daha uygun olduğuna karar vermenize yardımcı olabilir.|  
|[Yönetilen kod için Temel Doğruluk Kuralları kural kümesi](../code-quality/basic-correctness-rules-rule-set-for-managed-code.md)|Bu kurallar mantık hataları ve Framework API kullanımı yapılan yaygın hataları odaklanır. En az önerilen kurallar tarafından bildirilen uyarılar listesini genişletmek için bu kural içerir.|  
|[Yönetilen kod için Temel Tasarım Yönerge Kuralları kural kümesi](../code-quality/basic-design-guideline-rules-rule-set-for-managed-code.md)|Bu kurallar kodunuzu anlamayı ve kullanmayı daha kolay hale getirmek için en iyi yöntemler üzerinde odaklanır. Bu kural projeniz Kütüphane kodu içeriyorsa, ya da kolayca rahat kod için en iyi yöntemler zorlamak istiyorsanız kümesini içerir.|  
|[Yönetilen kod için Genişletilmiş Doğruluk Kuralları kural kümesi](../code-quality/extended-correctness-rules-rule-set-for-managed-code.md)|Bu kuralların raporlanan mantığı ve framework kullanım hatalarını en üst düzeye çıkarmak için temel doğruluk kurallarını genişletin. Ekstra Vurgu COM birlikte çalışma ve mobil uygulamaları gibi spesifik senaryolarda yer alır. Bu kural Bu senaryolardan biri, projenize veya projenize ek sorunları bulmak için geçerliyse kümesi dahil etmeyi düşünün.|  
|[Yönetilen kod için Genişletilmiş Tasarım Yönerge Kuralları kural kümesi](../code-quality/extended-design-guidelines-rules-rule-set-for-managed-code.md)|Bu kurallar bildirilir ve yaşatılabilirlik en üst düzeye çıkarmak için temel tasarım yönerge kuralları'nı genişletin. Kuralları adlandırma üzerinde fazladan Vurgu yerleştirilir. Bu kural projeniz Kütüphane kodu içeriyorsa, ya da Bakımı yapılabilir kodu yazmak için en yüksek standartları zorlamak istiyorsanız kümesi dahil etmeyi düşünün.|  
|[Yönetilen kod için Genelleştirme Kuralları kural kümesi](../code-quality/globalization-rules-rule-set-for-managed-code.md)|Bu kurallar veri uygulamanızın farklı dil, yerel ayarlar ve kültürler kullanıldığında düzgün görüntülenmesini engelleyen sorunlara odaklanır. Bu kural, uygulama yerelleştirilmiş ya da Eğer kümesini içerir.|  
|[Yönetilen kod için Yönetilen Minimum Kurallar kural kümesi](../code-quality/managed-minimun-rules-rule-set-for-managed-code.md)|Bu kurallar kodunuzda kod analizinin en doğru olan en kritik sorunlara odaklanır.  Bu kurallar küçük ve bunlar yalnızca sınırlı bir Visual Studio sürümlerinde çalışması amaçlanmıştır.  Minimumrecommendedrules.ruleset'i diğer Visual Studio sürümleri ile kullanın.|  
|[Yönetilen kod için Yönetilen Önerilen Kurallar kural kümesi](../code-quality/managed-recommended-rules-rule-set-for-managed-code.md)|Bu kurallar potansiyel güvenlik boşluklarını, uygulama kilitlenmesi ve diğer önemli mantık ve tasarım hataları gibi kodunuzda en kritik sorunlara odaklanır. Projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesini içermelidir.|  
|[Karışık Minimum Kurallar kural kümesi](../code-quality/mixed-minimum-rules-rule-set.md)|Bu kurallar potansiyel güvenlik boşluklarını ve Uygulama Kilitlenmesi gibi Common Language Runtime destekleyen C++ projelerinizin en kritik sorunlara odaklanır. Common Language Runtime destekleyen C++ projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesini içermelidir.|  
|[Karışık Önerilen Kurallar kural kümesi](../code-quality/mixed-recommended-rules-rule-set.md)|Bu kurallar potansiyel güvenlik boşluklarını, uygulama kilitlenmesi ve diğer önemli mantık ve tasarım hataları gibi Common Language Runtime destekleyen C++ projeleriniz en yaygın ve kritik sorunlarına odaklanır. Common Language Runtime destekleyen C++ projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesini içermelidir.  Bu kural Seti Visual Studio Professional sürümü ve üzeri sürümlerin yapılandırılması için tasarlanmıştır.|  
|[Yerel Minimum Kurallar kural kümesi](../code-quality/native-minimum-rules-rule-set.md)|Bu kurallar potansiyel güvenlik boşluklarını ve Uygulama Kilitlenmesi gibi yerel, kodunuzda en kritik sorunlara odaklanır. Doğal projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesini içermelidir.|  
|[Yerel Önerilen Kurallar kural kümesi](../code-quality/native-recommended-rules-rule-set.md)|Bu kurallar potansiyel güvenlik boşluklarını ve Uygulama Kilitlenmesi gibi yerel kodda en önemli ve en yaygın sorunları odaklanır.  Doğal projeleriniz için oluşturduğunuz herhangi bir özel kural kümesi bu kural kümesini içermelidir.  Bu kural Seti Visual Studio Professional sürümü ve üzeri sürümlerde çalışmak üzere tasarlanmıştır.|  
|[Yönetilen kod için Güvenlik Kuralları kural kümesi](../code-quality/security-rules-rule-set-for-managed-code.md)|Bu kural kümesi, tüm Microsoft Güvenlik kuralları içerir. Bu kural raporlanan olası güvenlik sorunlarını sayısı en üst düzeye çıkarmak için kümesi içerir.|
