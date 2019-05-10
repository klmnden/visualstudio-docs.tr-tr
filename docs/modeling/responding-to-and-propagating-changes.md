---
title: Değişikliklere Yanıt Verme ve Değişiklikleri Yayma
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Domain-Specific Language, events
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a1d58ede1370976147b33cf1246f8b582adb3c5b
ms.sourcegitcommit: 6a19c5ece38a70731496a38f2ef20676ff18f8a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/09/2019
ms.locfileid: "65476609"
---
# <a name="respond-to-and-propagate-changes"></a>Değişiklikleri için yanıtlama ve yayma

Bir öğe oluşturulduğunda, silinmiş veya güncelleştirildiğinde, değişiklik modelinin diğer bölümleri veya dosyaları, veritabanları veya diğer bileşenleri gibi dış kaynaklara yayan kod yazabilirsiniz.

## <a name="reference"></a>Başvuru

Bir kılavuz olarak aşağıdaki sırayla bu teknikler göz önünde bulundurun:

|Yöntemi|Senaryolar|Daha fazla bilgi için|
|-|-|-|
|Hesaplanan alan özelliği tanımlar.|Değeri, modeldeki diğer özelliklerinden hesaplanan bir alan özelliği. Örneğin, ilgili öğelerin fiyatlar toplamını olan fiyat.|[Hesaplanan ve Özel Depolama Özellikleri](../modeling/calculated-and-custom-storage-properties.md)|
|Bir depolama özel etki alanı özelliği tanımlayın.|Diğer bölümlerinde modelinin veya harici olarak depolanan bir alan özelliği. Örneğin, bir ağaç modelinde içine bir ifade dizeyi ayrıştırmak.|[Hesaplanan ve Özel Depolama Özellikleri](../modeling/calculated-and-custom-storage-properties.md)|
|Geçersiz kılma OnValueChanging ve OnDeleting gibi değişiklik işleyicileri|Farklı öğeler eşitlenmiş halde tutun ve dış değerleri modeli ile eşitlenmiş halde tutun.<br /><br /> Tanımlı aralıkları için değerler kısıtlar.<br /><br /> Hemen önce ve sonra özellik değerini ve diğer değişiklikler çağrılır. Bir özel durum tarafından değişiklik sonlandırabilirsiniz.|[Etki Alanı Özellik Değeri Değişiklik İşleyicileri](../modeling/domain-property-value-change-handlers.md)|
|Kurallar|Yalnızca bir işlem içinde bir değişiklik oldu bitmeden önce yürütme için sıraya alınan kuralları tanımlayabilirsiniz. Bunlar, geri alma veya yineleme üzerinde yürütülmez. Deponun bir bölümünü başka ile eşitlenmiş tutmak için bunları kullanın.|[Değişiklikleri Modelin İçinde Yayan Kurallar](../modeling/rules-propagate-changes-within-the-model.md)|
|Store olayları|Model Deposu ekleme veya bir öğe veya bağlantı siliniyor veya bir özelliğin değerinin değiştirilmesi gibi olayların bildirimleri sağlar. Olayı, Geri Al ve Yinele da yürütülür. Depoda olmayan değerleri güncelleştirmek için deposu olayları kullanın.|[Değişiklikleri Modelin Dışına Yayan Olay İşleyicileri](../modeling/event-handlers-propagate-changes-outside-the-model.md)|
|.NET olayları|Fare tıklama ve diğer hareketlerini yanıt olay işleyicileri şekilleri bulunur. Bu olayların her nesne için kaydolması gerekir. Kayıt, genellikle InitializeInstanceResources bir geçersiz kılma gerçekleştirilir ve her öğe için yapılması gerekir.<br /><br /> Bu olaylar, genellikle bir işlemin dışında oluşur.|[Nasıl yapılır: Şekil veya Dekoratörde bir Tıklama için Araya Girme](../modeling/how-to-intercept-a-click-on-a-shape-or-decorator.md)|
|Sınır kuralları|Sınırları kural, özellikle bir şeklin sınırları sınırlamak için kullanılır.|[BoundsRules Şekil Konumunu ve Boyutunu Kısıtlamama](/visualstudio/modeling/boundsrules-constrain-shape-location-and-size?view=vs-2015)|
|Seçim kuralları|Seçimi kurallarını, özellikle kullanıcının seçim yapabileceği kısıtlar.|[Nasıl yapılır: Geçerli Seçime Erişme ve Seçimi Kısıtlama](../modeling/how-to-access-and-constrain-the-current-selection.md)|
|OnAssocatedPropertyChanged|Şekilleri ve bağlayıcıları gibi gölge, ok ucu, renk, çizgi genişliği ve stil özelliklerini kullanarak model öğelerini durumları gösterir.|[Modeli Yansıtacak Şekilleri ve Bağlayıcıları Güncelleştirme](../modeling/updating-shapes-and-connectors-to-reflect-the-model.md)|

## <a name="compare-rules-and-store-events"></a>Kuralları karşılaştırın ve olayları depolamak

Bir modelde değişiklikler olduğunda, değişiklik notifiers, kuralları ve olayları çalıştırılır.

Kuralları genellikle değişikliği oluştu son işlem sırasında uygulanır ve olayları, bir işlemde değişiklikler gönderildikten sonra uygulanır.

Deposu olayları Store ve kuralları Store içinde tutarlılık sağlamak için dışında kalan nesneler ile modeli eşitlemek için kullanın.

- **Özel kurallar oluşturarak** soyut bir kuraldan türetilmiş bir sınıf olarak özel bir kural oluşturun. Ayrıca, özel kural hakkındaki framework bildirmeniz gerekir. Daha fazla bilgi için [kuralları yaymak değişiklikleri içinde modeli](../modeling/rules-propagate-changes-within-the-model.md).

- **Olaylara abone olma** bir olaya abone önce bir olay işleyicisi ve temsilci oluşturma. Ardından <xref:Microsoft.VisualStudio.Modeling.Store.EventManagerDirectory%2A>özelliği olaya abone olun. Daha fazla bilgi için [olay işleyicileri yaymak değişiklikleri dışında modeli](../modeling/event-handlers-propagate-changes-outside-the-model.md).

- **Değişiklikler geri alınıyor** bir işlemin geri, olayları oluştuğunda, ancak kuralları uygulanmaz. Bir kural değeri değiştirir ve bu değişikliği geri alın, değer özgün değerine geri alma işlemi sırasında sıfırlanır. Bir olay oluştuğunda, özgün değerine değeri el ile değiştirmeniz gerekir. İşlemler ve geri alma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Modeli güncelleştirmek için işlemleri kullanma](../modeling/how-to-use-transactions-to-update-the-model.md).

- **Kuralları ve olayları için olay bağımsız değişkenleri geçirme** hem olayları ve kuralları geçirilir bir `EventArgs` modeli hakkında bilgi olan parametresi değiştirildi.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Şekil veya Dekoratörde bir Tıklama için Araya Girme](../modeling/how-to-intercept-a-click-on-a-shape-or-decorator.md)
- [Bir etki alanına özgü dili özelleştirmek için kod yazma](../modeling/writing-code-to-customise-a-domain-specific-language.md)
