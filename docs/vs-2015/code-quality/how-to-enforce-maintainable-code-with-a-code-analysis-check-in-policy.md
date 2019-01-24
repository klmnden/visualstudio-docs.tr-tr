---
title: 'Nasıl yapılır: Bir kod analizi iade ilkesi ile Bakımı yapılabilir kodu zorlama | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- code analysis, check-in policies
ms.assetid: d1b3b04f-4dd9-40e6-b2d4-b414d33fb647
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 5676bfaabb20ebf6dabea7bae66527d17891b362
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753021"
---
# <a name="how-to-enforce-maintainable-code-with-a-code-analysis-check-in-policy"></a>Nasıl yapılır: Bir Kod Analizi İade İlkesi ile Bakımı Yapılabilir Kodu Zorlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Geliştiriciler, karmaşıklığı ve bakımı kodlarını ölçmek için kod ölçümleri araç kullanabilirsiniz, ancak iade ilkesinin parçası olarak kod ölçümleri çağrılamaz. Ancak, bir takım, kodun kod ölçümleri standartlarıyla uyumluluğu doğrulamak ve iade etme ilkeleri aracılığıyla kuralları zorunlu Kod Analizi kuralları etkinleştirebilirsiniz. Kod ölçümleri hakkında daha fazla bilgi için bkz: [kod ölçüm değerleri](../code-quality/code-metrics-values.md).  
  
 Geliştiriciler, derinliği, devralma, eşlenmesiyle sınıfı, bakım dizini ve karmaşıklık kurallarını Kod Analizi iade ilkeleri ile Bakımı yapılabilir kodu zorlama etkinleştirebilirsiniz. Dört bu kurallar, Kod Analizi İlkesi Düzenleyicisi'nde "Bakım kuralları" kategorisi altında bulunur.  
  
 Yöneticiler sürümü denetlemek için [!INCLUDE[esprfound](../includes/esprfound-md.md)] iade ilkesi gereksinimleri için Kod Analizi bakım kuralları ekleyebilirsiniz. Bu ilkeleri geliştiriciler kod iade başlatmadan önce bu kuralı değişikliklere dayalı analizi çalıştırmak gerekli iade.  
  
### <a name="to-open-the-code-analysis-policy-editor"></a>Kod Analizi İlkesi Düzenleyicisi'ni açmak için  
  
1.  İçinde **Takım Gezgini**, takım projesine sağ tıklayın, **takım projesi ayarları**ve ardından **kaynak denetimi**.  
  
     **Kaynak denetimi** iletişim kutusu görüntülenir.  
  
2.  Üzerinde **iade ilkesi** sekmesine ve tıklayın **Ekle**.  
  
     **İade İlkesi Ekle** iletişim kutusu görüntülenir.  
  
3.  İçinde **iade ilkesi** listesinden **Kod Analizi** onay kutusunu işaretleyin ve ardından **Tamam**.  
  
     **Kod Analizi İlke Düzenleyicisi** iletişim kutusu görüntülenir.  
  
### <a name="to-enable-code-analysis-maintainability-rules"></a>Kod Analizi bakım kuralları etkinleştirmek için  
  
1.  İçinde **Kod Analizi İlke Düzenleyicisi** iletişim kutusunun **kural ayarları**, genişletme **bakım kuralları** düğümü.  
  
2.  Aşağıdaki kurallar için onay kutularını seçin:  
  
    -   Devralma derinliği: **CA1501 AvoidExcessiveInheritance** -eşiği: Fazla 5 düzey derinliğinde uyarı  
  
    -   Karmaşıklığı: **CA1502 AvoidExcessiveComplexity** -eşiği: 25'ten fazla uyarı  
  
    -   Bakım dizini: **CA1505 AvoidUnmaintainableCode** -eşiği: 20'den daha az uyarı  
  
    -   Sınıf bağlantısı: **CA1506 AvoidExcessiveClassCoupling** -eşiği: Bir sınıf için 80'den fazla ve 30 bir yöntem için birden fazla uyarı  
  
    -   Ayrıca, bir derleme önlemek için bir kuralı ihlali istiyorsanız seçin **uyarı bir hata olarak değerlendir** kural açıklaması yanındaki onay kutusunu.  
  
3.  **Tamam**'ı tıklatın. Yeni iade ilkesi artık, gelecekteki iade etme işlemleri için de geçerlidir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Kod ölçüm değerleri](../code-quality/code-metrics-values.md)   
 [Kod Çözümleme İade İlkeleri Oluşturma ve Kullanma](../code-quality/creating-and-using-code-analysis-check-in-policies.md)
