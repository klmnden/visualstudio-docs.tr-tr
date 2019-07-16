---
title: Yönetilen kod uyarıları için Kod Analizi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vc.project.vcfxcoptool.enablefxcop
helpviewer_keywords:
- managed code analyis, warnings
- warnings, managed code analysis
- managed code analysis warnings
- code analysis,managed code
ms.assetid: 3c2741ff-0d3a-42e6-acd5-d42310bd03c4
caps.latest.revision: 22
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 237091c4304b6d6fef90197d503f84fe86c12b9e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68142337"
---
# <a name="code-analysis-for-managed-code-warnings"></a>Yönetilen Kod için Kod Analizi Uyarıları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yönetilen kod analizi aracı, yönetilen kod kitaplıkları kuralı ihlallerini göstermek uyarılar sağlar. Uyarılar, tasarım, yerelleştirme, performans ve güvenlik gibi kural alanları halinde düzenlenir. Her uyarı, yönetilen kod analizi kural ihlalini gösterir. Bu bölümde, her yönetilen kod analizi uyarısı için derinlemesine tartışmalar ve örnekler sağlar.  
  
 Aşağıdaki tabloda, her uyarı için sağlanan bilgi türünü gösterir.  
  
|Öğe|Açıklama|  
|----------|-----------------|  
|Tür|Kuralın tür adı.|  
|CheckId|Kuralı için benzersiz tanımlayıcı. Checkıd ve kategori kaynak uyarı gizleme için kullanılır.|  
|Kategori|Uyarı kategorisi.|  
|Yeni Değişiklik|Bu kural ihlalini düzeltmesini bir değişiklik olup olmadığı. İhlaline neden hedefte bağımlılığı bir derleme yeni derlemeniz değil değişiklik anlamına gelir bozucu sürüm sabit veya çalışma zamanında değişiklik nedeniyle başarısız olabilir. Birden çok düzeltmesi mevcuttur ve en az bir düzeltme bölünmesi farklıdır ve bir düzeltme değil, hem 'Yeni' ve 'Bozucu olmayan' belirtilir.|  
|Sebep|Kural bir uyarı oluşturmak neden olan belirli yönetilen kod.|  
|Açıklama|Uyarı arkasında sorunları açıklar.|  
|İhlaller Nasıl Düzeltilir?|Kural karşılar ve bir uyarı oluşturmasını önlemek için kaynak kodunu değiştirmek açıklanmaktadır.|  
|Uyarılar Bastırıldığında|Kuraldan bir uyarıyı bastırmak güvenli olduğunda açıklar.|  
|Örnek kod|Kuralı ihlal ediyor ve kural karşılayan örnekler düzeltti örnekler.|  
|İlgili uyarılar|İlgili uyarıları.|  
  
## <a name="in-this-section"></a>Bu Bölümde  
  
|||  
|-|-|  
|[CheckId Uyarıları](../code-quality/code-analysis-warnings-for-managed-code-by-checkid.md)|Checkıd tüm uyarıları listeler|  
|[Şifreleme Uyarıları](../code-quality/cryptography-warnings.md)|Daha güvenli kütüphaneleri ve uygulamaları doğru kullanımı aracılığıyla şifreleme desteği uyarılar.|  
|[Tasarım Uyarıları](../code-quality/design-warnings.md)|Tarafından belirtilen doğru kitaplık tasarım desteği uyarıları [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] tasarım yönergeleri.|  
|[Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)|Dünya çapında kullanılmaya hazır kitaplıkları ve uygulamaları desteklemek uyarılar.|  
|[Birlikte Çalışabilirlik Uyarıları](../code-quality/interoperability-warnings.md)|COM istemcileri ile etkileşimi destekleyen uyarılar.|  
|[Bakım Uyarıları](../code-quality/maintainability-warnings.md)|Kitaplık ve Uygulama Bakımı destekleyen uyarılar.|  
|[Hareketlilik Uyarıları](../code-quality/mobility-warnings.md)|Uyarılar verimli güç kullanımını destekler.|  
|[Adlandırma Uyarıları](../code-quality/naming-warnings.md)|Adlandırma kurallarını kıldığı destekleyen uyarıları [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)] tasarım yönergeleri.|  
|[Performans Uyarıları](../code-quality/performance-warnings.md)|Yüksek performanslı kitaplıkları ve uygulamaları desteklemek uyarılar.|  
|[Taşınabilirlik Uyarıları](../code-quality/portability-warnings.md)|Farklı platformlar arasında taşınabilirlik destekleyen uyarılar.|  
|[Güvenilirlik Uyarıları](../code-quality/reliability-warnings.md)|Doğru bellek ve iş parçacığı kullanımı gibi kitaplık ve uygulama güvenilirliğini destekleyen uyarılar.|  
|[Güvenlik Uyarıları](../code-quality/security-warnings.md)|Bu uyarılar daha güvenli kütüphaneleri ve uygulamaları destekler.|  
|[Kullanım Uyarıları](../code-quality/usage-warnings.md)|Uygun kullanımını desteklemek uyarıları [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)].|  
|[Kod Çözümleme İlkesi Hataları](../code-quality/code-analysis-policy-errors.md)|Kod Analizi İlkesi iade aşamasında karşılanmıyor, oluşan hataları.|
