---
title: Kod Analizi için yönetilen kod genel bakış | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: overview
f1_keywords:
- vs.projectpropertypages.codeanalysis
helpviewer_keywords:
- code analysis, managed code
- managed code, code analysis
ms.assetid: 12ec0dab-46a4-43d8-984a-440730ef37a9
caps.latest.revision: 37
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: a38909eb0917b3ad5b02d5e953c17c950c7c819e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62539198"
---
# <a name="code-analysis-for-managed-code-overview"></a>Yönetilen Kod için Kod Analizine Genel Bakış
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yönetilen kod için kod analizi, yönetilen derlemeleri çözümler ve derlemeler, programlama ve Microsoft .NET Framework tasarım yönergeleri ile ortaya konan Tasarım Kuralları ihlalleri gibi bilgileri raporlar.  
  
 Analiz aracı uyarı iletileri bir Çözümleme sırasında gerçekleştirdiği denetimleri temsil eder. Uyarı iletileri ilgili programlama ve tasarım sorunlarını belirleyin ve mümkünse sorunu gidermek nasıl bilgi olduğunda.  
  
## <a name="ide-integrated-development-environment-integration"></a>IDE (tümleşik geliştirme ortamı) Tümleştirmesi  
 Bir geliştirici olarak projenizde kod analizi otomatik olarak çalıştırabilir veya el ile çalıştırabilirsiniz.  
  
 Bir projeyi derleme yaptığınızda Kod Analizi çalıştırmak için seçtiğiniz **etkinleştir (code_analysıs sabitini tanımlar) derlemede kod analizini** projenin özellik sayfasında. Daha fazla bilgi için [nasıl yapılır: Enable ve Disable otomatik kod çözümlemesini](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md).  
  
 Kod analizini el ile bir proje üzerinde çalışma **Çözümle** menüsünde tıklatın **kod çözümlemeyi Çalıştır**_ProjectName_. Daha fazla bilgi için [nasıl yapılır: Enable ve Disable otomatik kod çözümlemesini](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md).  
  
## <a name="rule-sets"></a>Kural Kümeleri  
 Yönetilen kod için Kod Analizi kuralları halinde gruplanır *kural kümeleri*. Microsoft Standart kural kümelerinden birini kullanabilir veya belirli bir gereksinimi karşılamak için özel bir kural oluşturabilirsiniz. Daha fazla bilgi için [Kod Analizi kurallarını gruplandırmak için kural kümeleri kullanma](../code-quality/using-rule-sets-to-group-code-analysis-rules.md).  
  
## <a name="in-source-suppression"></a>Kaynak sıkıştırmasında  
 Genellikle, geçerli olmayan bir uyarı olduğunu belirtmek kullanışlıdır. Bu geliştiriciye ve kodu daha sonra gözden geçirecek diğer kişilere bir uyarı araştırılması ve sonra da gizlenen veya yoksayıldı olduğunu bildirir.  
  
 Uyarıların kaynak sıkıştırması özel öznitelikler ile gerçekleştirilir. Bir uyarıyı bastırmak için öznitelik Ekle `SuppressMessage` aşağıdaki örnekte gösterildiği gibi kaynak koda:  
  
 ```csharp
 [System.Diagnostics.CodeAnalysis.SuppressMessage("Microsoft.Design", "CA1039:ListsAreStrongTyped")]
 Public class MyClass
 {
     // code
 }
 ```
  
 Daha fazla bilgi için [bastır uyarıları kullanarak SuppressMessage özniteliğini](../code-quality/suppress-warnings-by-using-the-suppressmessage-attribute.md).  
  
## <a name="run-code-analysis-as-part-of-check-in-policy"></a>İade ilkesinin parçası olarak kod analizini Çalıştır  
 Bir kuruluş olarak tüm iade etmelerin bazı ilkeleri karşılamasını zorunlu isteyebilirsiniz. Özellikle, aşağıdaki ilkeleri uyguladığınızdan emin olmanız gerekir:  
  
- Teslim edilen kodda derleme hataları vardı.  
  
- Kod Analizi en son derlemenin bir parçası çalıştırıldı.  
  
  Bu iade etme ilkeleri belirterek gerçekleştirebilirsiniz. Daha fazla bilgi için [takım projesi iade ilkeleriyle kod kalitesini geliştirme](../code-quality/enhancing-code-quality-with-team-project-check-in-policies.md).  
  
## <a name="team-build-integration"></a>Ekip Oluşturma entegrasyonu  
 Analiz aracı yapı işleminin bir parçası olarak çalıştırmak için derleme sisteminin tümleşik özelliklerini kullanabilirsiniz. Daha fazla bilgi için [uygulamayı derleyin](http://msdn.microsoft.com/library/a971b0f9-7c28-479d-a37b-8fd7e27ef692).  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kod Analizi kurallarını gruplandırmak için kural kullanarak ayarlar](../code-quality/using-rule-sets-to-group-code-analysis-rules.md)   
 [Nasıl yapılır: Etkinleştirme ve otomatik kod analizini devre dışı](../code-quality/how-to-enable-and-disable-automatic-code-analysis-for-managed-code.md)
