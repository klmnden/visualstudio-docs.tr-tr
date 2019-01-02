---
title: Yük testi senaryoları
ms.date: 10/03/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, scenarios
- load tests, user activities
- load tests, modeling scenarios
ms.assetid: fec04f2e-bf38-4d44-b2ec-fa50f58fd0d9
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.openlocfilehash: 18acb181125bcc8bd2f68a93661658f8ba01c79c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53934024"
---
# <a name="edit-load-test-scenarios"></a>Yük testi senaryolarını düzenleme

Bir yük testi *senaryo* yük düzeni, test karışımını, tarayıcı karışımı ve ağ karışımını belirtir. Senaryoları, karmaşık, gerçekçi iş yükleri benzetimi yapmak için testleri yapılandırmanıza olanak tanırlar için önemlidir.

Örneğin, kullanılan bir Internet ön uç tarafından eş zamanlı müşterilerin gelen birçok bağlantı hızıyla ve farklı tarayıcılar kullanarak yüzlerce bir e-ticaret sitesini test. Aynı site, ürünleri güncelleştirmek ve istatistikleri görüntülemek için şirket içi çalışanlar tarafından kullanılan bir yönetim işlevi de olabilir. Bu dahili kullanıcılar genellikle aynı tarayıcı ve yüksek hızlı LAN bağlantısı kullanarak siteye erişir. Farklı senaryolarda kullanıcıların bu iki farklı grubunun özelliklerini saklamak isteyeceksiniz. Her senaryo, bir sanal kullanıcı türü içerebilir. Bu durumda, sanal müşterileri temsil edecek bir yük testi senaryosuna yapılabilir ve başka bir senaryo, bir Web sitesinin iç sanal kullanıcılarını temsil etmek için yapılabilir.

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

## <a name="scenario-components"></a>Senaryo Bileşenleri

Herhangi bir ilk yapılandırma seçenekleri ve bir yük testi oluşturduğunuzda, belirttiğiniz ayarlar daha sonra değiştirilebilir **Yük Testi Düzenleyicisi**. Bir yük testine yeni senaryolar ve çalıştırma ayarları sayaç kümeleri de ekleyebilirsiniz.

![Yük testi senaryoları](../test/media/loadtesteditinscenarios.png)

Senaryoları aşağıdaki bileşenleri içerir:

|Terim|Tanım|
|-|-|
|Tarayıcı karışımı|Sanal kullanıcıların çeşitli web tarayıcıları bir Web sitesine erişir benzetimini yapar.|
|Yük düzeni|Bir yük testi ve yeni kullanıcıların başlatılma oranını sırasında etkin olan sanal kullanıcı sayısını belirtir. Örneğin: adım, sabit ve hedef temelli.|
|Test karışımı modeli|Bir yük testi senaryosunda belirli bir testi çalıştıran sanal kullanıcının olasılığını belirtir. Örneğin: TestA ve % 80 fırsat TestB'yi çalıştırmak için çalıştırmak için % 20 fırsat. Test karışımı modeli her bir senaryo için testinizin hedefini yansıtmalıdır.|
|Test karışımı|Test karışımı seçimini senaryoyu oluşturan web başarım ve birim testleri ve bu testlerin dağıtımını ' dir.|
|Ağ karışımı|Sanal kullanıcıların çeşitli ağ bağlantıları bir Web sitesine erişir benzetimini yapar. Ağ karışımı LAN, kablolu modem ve diğer seçenekleri içeren seçenekler sunar.|

Kullanarak düzenleyebileceğiniz diğer bazı özellikleri senaryosunda **Yük Testi Düzenleyicisi**. Daha fazla bilgi için [yük testi senaryosu özellikleri](../test/load-test-scenario-properties.md).

## <a name="tasks"></a>Görevler

|Görevler|İlişkili Konular|
|-|-----------------------|
|**Senaryonuza yapay insan etkileşimi duraklamaları ekleyin:** Düşünme süreleri, insanların bir Web sitesiyle etkileşimleri ile arasında beklemesine neden olan insan davranışını benzetmekte kullanılır. Düşünme süreleri, bir web performans testindeki istekleri ve bir yük testi senaryosunda test tekrarları arasında oluşur. Bir yük testinde Düşünme süreleri kullanarak daha kesin yükleme benzetimleri oluşturmak yararlı olabilir.|-   [Web sitesi insan etkileşimi gecikmelerini benzetmek için Düşünme zamanlarını düzenleme](../test/edit-think-times-in-load-test-scenarios.md)|
|**Senaryonuz için sanal kullanıcı sayısını belirtin:** Yük deseni özellikleri benzetimli kullanıcı yükünün yük testi boyunca nasıl ayarlandığını belirlemek için yapılandırabilirsiniz. Üç yerleşik yükleme düzeni Al: Sabit, adım ve hedef temelli. Yük desenini seçin ve yük testi hedefleriniz için uygun düzeylere özellikleri ayarlayın.|-   [Model sanal kullanıcı etkinlikleri için yük desenlerini düzenleme](../test/edit-load-patterns-to-model-virtual-user-activities.md)|
|**Bu senaryoda bir testi çalıştıran sanal kullanıcı olasılığını yapılandırın:** Bir yük testi senaryosunda belirli bir testi çalıştıran sanal kullanıcı olasılığını belirleyen test karışımını kullanabilirsiniz. Bu, yükü daha gerçekçi bir benzetimini sağlar. Uygulamalarınız boyunca yalnızca bir iş akışı sahip olmak yerine, son kullanıcıların uygulamalarınızla nasıl etkileşmeleri hakkında daha yakın bir benzetim olan birkaç iş olabilir.|-   [Metin karışımı modellerini düzenleme](../test/edit-test-mix-models-to-specify-the-probability-of-a-virtual-user-running-a-test.md)|
|**Ekleme veya bir Web performans veya birim testi bir yük testi senaryosu kaldırabilirsiniz:** Ekleyebilir veya bir yük testi senaryosunda web performans veya birim testi kaldırın. Bir yük testi, her biri bir veya daha fazla web performans testleri içeren bir veya daha fazla senaryo içerir.|-   [Test karışımını düzenleyin](../test/edit-the-test-mix-to-specify-which-web-browsers-types-in-a-load-test-scenario.md)|
|**Senaryonuz için istenilen ağ karışımını yapılandırın:** Ağ karışımını kullanarak, bir yük testi senaryosunda daha gerçekçi bir biçimde Ağ Yükü benzetimi. Yükleme, tek tek ağ türü yerine farklı yapıda ağ türlerinin karışımı kullanılarak oluşturulur. Son kullanıcıların uygulamalarınızla nasıl etkileşmeleri hakkında daha yakın bir benzetim oluşturursunuz. Ağ karışımı modeli senaryonun hedeflerini yansıtmalıdır.|-   [Sanal ağ türlerini belirtme](../test/specify-virtual-network-types-in-a-load-test-scenario.md)|
|**Senaryonuz için uygun Web tarayıcı karışımını seçin:** Tarayıcı karışımını kullanarak, bir yük testi senaryosunda daha gerçekçi web yükü benzetimi. Yükleme tek tarayıcı yerine türdeş olmayan bir karışımını kullanarak oluşturulur. Uygulamalarınızla kullanılacak tarayıcıların daha yakın bir yaklaşığını oluşturursunuz.|-   [Web tarayıcısı türlerini belirtme](../test/edit-the-test-mix-to-specify-which-web-browsers-types-in-a-load-test-scenario.md)|
|**Senaryonuz için test yineleme ayarlarını yapılandırın:** Yükleme testi düzenleyiciyi ve Özellikler penceresini kullanarak test yineleme ayarlarını yapılandırmak için bir yük testi senaryosu düzenleyebilirsiniz. Varsayılan olarak, bir senaryo yok en yüksek test yinelemeleri ile ayarlanır. İsteğe bağlı olarak senaryo ve bunlar arasında beklenecek süreyi en yüksek yineleme sayısı da yapılandırabilirsiniz.|-   [Senaryolar için test yinelemelerini yapılandırma](../test/configure-test-iterations-in-a-load-test-scenario.md)|
|**Senaryonuz için gecikme ayarlarını yapılandırın:** Kullanarak **Yük Testi Düzenleyicisi** ve **özellikleri** penceresinde, bir yük testinde bir senaryoyu başlatmadan önce bir gecikme belirleyebilirsiniz. Bir örneği olduğunda kullanmak isteyebilirsiniz **başlama zamanını ertele** özelliği olan başka bir senaryonun tükettiği öğeleri oluşturmaya başlamak için bir senaryoya ihtiyaç duyduğunuzda. Üretim senaryosunun bazı verileri doldurmasına etkinleştirmek için tüketim senaryosunu geciktirebilirsiniz.|-   [Configureng senaryo başlatma gecikmelerini](../test/configure-scenario-start-delays.md)|
|**Bir yük testi senaryosunda kullanılacak uzak makineleri belirtin:** Bir yük testi oluşturduktan sonra hangi test aracılarını dahil etmek istediğiniz belirtmek için yük testi senaryonuzun özelliklerini düzenleyebilirsiniz. Daha fazla bilgi için [Test denetleyicileri ve test aracılarını](configure-test-agents-and-controllers-for-load-tests.md).|-   [Nasıl Yapılır: Kullanılacak test aracıları belirtme](../test/how-to-specify-test-agents-to-use-in-load-test-scenarios.md)|

## <a name="see-also"></a>Ayrıca bkz.

- [Yük testlerini düzenleme](../test/edit-load-tests.md)
- [Yük testi senaryosu özellikleri](../test/load-test-scenario-properties.md)