---
title: 'Nasıl Yapılır: Bir kod analizi iade ilkesi ile Bakımı yapılabilir kodu zorlama'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
helpviewer_keywords:
- code analysis, check-in policies
ms.assetid: d1b3b04f-4dd9-40e6-b2d4-b414d33fb647
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 060ca6482249e9b1e538b25977a1bdf5dfb97276
ms.sourcegitcommit: 159ed9d4f56cdc1dff2fd19d9dffafe77e46cd4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/21/2018
ms.locfileid: "53739388"
---
# <a name="how-to-enforce-maintainable-code-with-a-code-analysis-check-in-policy"></a>Nasıl Yapılır: Bir kod analizi iade ilkesi ile Bakımı yapılabilir kodu zorlama

Geliştiriciler, karmaşıklığı ve bakımı kodlarını ölçmek için kod ölçümleri araç kullanabilirsiniz, ancak iade ilkesinin parçası olarak kod ölçümleri çağrılamaz. Ancak kodunuzun kod ölçümleri standartlarıyla uyumluluğu doğrulamak Kod Analizi kuralları etkinleştirin ve iade etme ilkeleri aracılığıyla kurallar uygular. Kod ölçümleri hakkında daha fazla bilgi için bkz: [kod ölçüm değerleri](../code-quality/code-metrics-values.md).

Derinlik, devralma, eşlenmesiyle sınıfı, bakım dizini ve karmaşıklık kurallarını bir kod çözümleme iade ilkesi ile Bakımı yapılabilir kodu zorlama etkinleştirebilirsiniz. Dört bu kurallar, Kod Analizi İlkesi Düzenleyicisi'nde "Bakım kuralları" kategorisi altında bulunur.

Sürüm denetimi için Team Foundation Yöneticileri, iade ilkesi gereksinimleri için Kod Analizi bakım kuralları ekleyebilirsiniz. Bu ilkeleri geliştiriciler kod iade başlatmadan önce bu kuralı değişikliklere dayalı analizi çalıştırmak gerekli iade.

## <a name="to-open-the-code-analysis-policy-editor"></a>Kod Analizi İlkesi Düzenleyicisi'ni açmak için

1. İçinde **Takım Gezgini**, projeye sağ tıklayın, **proje ayarları**ve ardından **kaynak denetimi**.

     **Kaynak denetimi** iletişim kutusu görüntülenir.

2. Üzerinde **iade ilkesi** sekmesine ve tıklayın **Ekle**.

     **İade İlkesi Ekle** iletişim kutusu görüntülenir.

3. İçinde **iade ilkesi** listesinden **Kod Analizi** onay kutusunu işaretleyin ve ardından **Tamam**.

     **Kod Analizi İlke Düzenleyicisi** iletişim kutusu görüntülenir.

## <a name="to-enable-code-analysis-maintainability-rules"></a>Kod Analizi bakım kuralları etkinleştirmek için

1. İçinde **Kod Analizi İlke Düzenleyicisi** iletişim kutusunun **kural ayarları**, genişletme **bakım kuralları** düğümü.

2. Aşağıdaki kurallar için onay kutularını seçin:

   - Devralma derinliği: **CA1501 AvoidExcessiveInheritance** -eşiği: Fazla 5 düzey derinliğinde uyarı

   - Karmaşıklığı: **CA1502 AvoidExcessiveComplexity** -eşiği: 25'ten fazla uyarı

   - Bakım dizini: **CA1505 AvoidUnmaintainableCode** -eşiği: 20'den daha az uyarı

   - Sınıf bağlantısı: **CA1506 AvoidExcessiveClassCoupling** -eşiği: Bir sınıf için 80'den fazla ve 30 bir yöntem için birden fazla uyarı

     Ayrıca, başarılı bir derleme önlemek için bir kuralı ihlali istiyorsanız seçin **uyarı bir hata olarak değerlendir** kural açıklaması yanındaki onay kutusunu.

3. **Tamam**'ı tıklatın. Yeni iade ilkesi artık, gelecekteki iade etme işlemleri için de geçerlidir.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod ölçüm değerleri](../code-quality/code-metrics-values.md)
- [Oluşturma ve kod çözümleme iade ilkelerini kullanma](../code-quality/how-to-create-or-update-standard-code-analysis-check-in-policies.md)