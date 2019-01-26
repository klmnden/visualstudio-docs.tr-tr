---
title: Veri sınıfı devralma (O R Tasarımcısı)
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: af32653c-f4e6-4217-8c5a-e32b322b4918
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: f0e95466baa4e16e4620ff387a11d4e723399a38
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54953399"
---
# <a name="data-class-inheritance-or-designer"></a>Veri sınıfı devralma (O/R Tasarımcısı)

Diğer nesneleri gibi LINQ to SQL sınıfları devralma kullanabilirsiniz ve diğer sınıflarından türetilmiş. Kod içinde bir sınıf diğerinden devralır bildirmek nesneler arasındaki devralma ilişkileri belirtebilirsiniz. Bir veritabanında kalıtım ilişkileri çeşitli yollarla oluşturulur. **Object Relational Designer** (**O/R Tasarımcısı**) ilişkisel sistemlerde sık uygulandığı şekilde tek tablolu devralma kavramını destekler.

Tek tablo Devralmada hem temel sınıfını hem türetilen sınıflarını sütunlarını içeren bir tek veritabanı tablosu yok. İlişkisel verilerle bir ayrıştırıcı sütunu verilen kaydın ait olduğu sınıfı belirleyen bir değer içerir. Örneğin, bir `Persons` herkesin şirket tarafından kullanılan içeren tablo. Bazı kişiler çalışanlar ve bazı kişiler yöneticileri. `Persons` Tablo adlı bir sütun içeren `Type` 1 değeri, yöneticileri ve 2 değerini çalışanlar için olan. `Type` Ayrıştırıcı sütunu bir sütundur. Bu senaryoda, çalışanların öğesinin oluşturabilir ve sınıf olan kayıtlar ile doldurmak bir `Type` değeri 2'dir.

Yapılandırdığınızda devralma varlık sınıfları kullanarak [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)], iki kez tasarımcıya devralma verileri içeren tek bir tabloyu sürükleyin: devralma hiyerarşisinde her sınıf için bir kez. Tasarımcıya tabloları ekledikten sonra bunları bir devralma öğesinden bağlanın **Object Relational Designer** araç ve kümesi dört devralma özelliklerinde **özellikleri** penceresi.

## <a name="inheritance-properties"></a>Devralma Özellikleri

Aşağıdaki tabloda, devralma özellikleri ve açıklamaları listelenmektedir:

|Özellik|Açıklama|
|--------------|-----------------|
|**Ayrıştırıcı özelliği**|Geçerli kayda ait olduğu olduğu sınıfı belirleyen (sütuna eşlenmiş) özelliği.|
|**Temel sınıf ayrıştırıcı değeri**|Değer (olarak tanımlanan sütunda **ayrıştırıcı özelliği**) bir kaydın temel sınıf olduğunu belirler.|
|**Türetilen sınıf ayrıştırıcı değeri**|Değer (olarak belirlenmiş özelliğinde **ayrıştırıcı özelliği**) bir kaydın türetilmiş sınıf olduğunu belirler.|
|**Devralma varsayılanı**|Özellik değeri olarak belirlenmiş doldurulur sınıfının **ayrıştırıcı özelliği** ya da eşleşmiyor **temel sınıf ayrıştırıcı değeri** veya **türetilen sınıfı Ayrıştırıcı değeri**.|

Devralma kullanan ve ilişkisel verilere karşılık gelen bir nesne modeli oluşturma biraz kafa karıştırıcı olabilir. Bu konu, temel kavramları ve devralma yapılandırmak için gerekli olan özellikler hakkında bilgi sağlar. Aşağıdaki konular, devralma ile nasıl yapılandıracağınızı öğrenmek için daha anlaşılır bir açıklama sağlar. **O/R Tasarımcısı**.

|Konu|Açıklama|
|-----------|-----------------|
|[Nasıl yapılır: O/R Tasarımcısı kullanarak devralmayı yapılandırma](../data-tools/how-to-configure-inheritance-by-using-the-o-r-designer.md)|Tek Tablo Devralma kullanarak varlık sınıflarını yapılandırmayı açıklar **O/R Tasarımcısı**.|
|[İzlenecek yol: Tek tablo devralma (O/R Tasarımcısı) kullanarak SQL sınıflarına LINQ oluşturma](../data-tools/walkthrough-creating-linq-to-sql-classes-by-using-single-table-inheritance-o-r-designer.md)|Tek Tablo Devralma kullanarak varlık sınıfları yapılandırma hakkında adım adım yönergeler sağlar **O/R Tasarımcısı**.|

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [İzlenecek yol: (O R Designer) SQL sınıflarına LINQ oluşturma](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [İzlenecek yol: Tek tablo devralma (O/R Tasarımcısı) kullanarak SQL sınıflarına LINQ oluşturma](../data-tools/walkthrough-creating-linq-to-sql-classes-by-using-single-table-inheritance-o-r-designer.md)
- [Başlarken](/dotnet/framework/data/adonet/sql/linq/getting-started)