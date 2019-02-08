---
title: Yazılan ve yazılmayan veri kümelerinin karşılaştırması
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
ms.assetid: c83ba0bb-5425-4d47-8891-6b4dbf937701
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: d6a16b8f0752ca2ab063f8bbbaa966836856eb4f
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55927730"
---
# <a name="typed-vs-untyped-datasets"></a>Yazılan ve yazılmayan veri kümelerinin karşılaştırması
Yazılan veri kümesi temel ilk türetilmiş bir veri kümesidir <xref:System.Data.DataSet> sınıfı ve ardından bilgilerinden **veri kümesi Tasarımcısı**, depolandığı .xsd dosyasına yeni, oluşturmak için bir veri kümesi sınıfı türü kesin belirlenmiş. (Tablolar, sütunlar ve benzeri) şema bilgileri oluşturulur ve bu yeni veri kümesi sınıfına birinci sınıf nesneleri ve özellikleri kümesi olarak derlenir. Yazılan veri kümesi temel devraldığından <xref:System.Data.DataSet> sınıfı, belirlenmiş bir sınıf tüm işlevlerini varsayar <xref:System.Data.DataSet> sınıfı ve bir örneği ele yöntemleriyle kullanılabilir bir <xref:System.Data.DataSet> bir parametre olarak sınıf.

 Yazılmamış bir veri kümesi, buna karşılık, karşılık gelen hiçbir yerleşik şeması vardır. Türü belirtilmiş veri kümesi olduğu gibi tabloları, sütunları ve benzeri yazılmamış bir veri kümesi içerir; ancak bunlar yalnızca koleksiyon olarak sunulur. (El ile tabloları ve diğer veri öğelerini yazılmamış bir veri kümesini oluşturduktan sonra ancak, veri kümesinin yapısı bir şema dataset kullanarak dışa aktarabilirsiniz <xref:System.Data.DataSet.WriteXmlSchema%2A> yöntemi.)

## <a name="contrast-data-access-in-typed-and-untyped-datasets"></a>Yazılan ve yazılmayan veri kümeleri Karşıtlık veri erişimi
 Yazılan veri kümesi için sınıfın özelliklerini tabloları ve sütunları gerçek adları almakta nesne modeli vardır. Örneğin, bir türü belirtilmiş veri kümesi ile çalışıyorsanız, aşağıdaki gibi bir kod kullanarak bir sütun başvurabilirsiniz:

 [!code-csharp[VbRaddataDatasets#4](../data-tools/codesnippet/CSharp/typed-vs-untyped-datasets_1.cs)]
 [!code-vb[VbRaddataDatasets#4](../data-tools/codesnippet/VisualBasic/typed-vs-untyped-datasets_1.vb)]

 Buna karşılık, yazılmamış bir veri kümesi ile çalışıyorsanız, eşdeğer kod şöyledir:

 [!code-csharp[VbRaddataDatasets#5](../data-tools/codesnippet/CSharp/typed-vs-untyped-datasets_2.cs)]
 [!code-vb[VbRaddataDatasets#5](../data-tools/codesnippet/VisualBasic/typed-vs-untyped-datasets_2.vb)]

 Türü belirlenmiş erişim değil yalnızca daha kolay okunmasını, ancak aynı zamanda tam olarak desteklenen Visual Studio IntelliSense tarafından **Kod Düzenleyicisi**. Yazılmış veri kümesi için söz dizimi ile çalışmak daha kolay olmasının yanı sıra veri kümesi üyeleri için değerler atama hataları olasılığını önemli ölçüde azaltan derleme zamanında tür sağlar. Bir sütunun adını değiştirirseniz, <xref:System.Data.DataSet> sınıfı ve ardından uygulamanızı derleyin, bir derleme hatası alırsınız. Derleme hataya çift tıklayarak **görev listesi**, doğrudan satır veya eski sütun adı başvuru kod satırlarını gidebilirsiniz. Erişim tablolar ve sütunlar bir türü belirtilmiş veri kümesi olduğundan da çalışma zamanında biraz daha hızlı erişim zamanında koleksiyonlar üzerinden değil, derleme zamanında belirlenir.

 Türü belirtilmiş datasets birçok avantaj olsa bile yazılmamış bir veri kümesi çeşitli durumlarda yararlı olur. Şema veri kümesi için kullanılabilir olduğunda en belirgin senaryodur. Uygulamanız bir veri kümesi döndüren bir bileşeni ile etkileşim kurma Bu, örneğin, meydana gelebilir ancak önceden yapısını ne olduğunu bildiğiniz değil. Benzer şekilde, ne zaman bir statik, öngörülebilir yapısına sahip değil verilerle çalışma zamanları vardır. Türü belirtilmiş veri kümesi sınıfı her değişikliği veri yapısı ile yeniden oluşturmanız gerekirdi bu durumda, türü belirlenmiş bir veri kümesini kullanmak için pratik olmasıdır.

 Daha genel olarak kullanılabilir bir şema zorunda kalmadan bir veri kümesini dinamik olarak oluşturabilir, birden çok kez vardır. Bu durumda, verileri ilişkisel bir biçimde temsil edilebilir olduğu sürece veri kümesi yalnızca bilgileri saklamak uygun bir yapı ' dir. Aynı anda bilgileri başka bir işleme geçirmek veya bir XML dosyasına yazmak için seri hale getirme olanağı gibi veri kümesinin özelliklerinden yararlanabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [Veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md)