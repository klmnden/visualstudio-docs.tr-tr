---
title: (O R Designer) DataContext metodunun dönüş türünü değiştir
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c5b66bff-6dbb-43c0-bffa-317133ca5b9e
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 18e54938248dd52ee331e4df7bd2388105522657
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66260569"
---
# <a name="how-to-change-the-return-type-of-a-datacontext-method-or-designer"></a>Nasıl yapılır: DataContext metodunun dönüş türünü değiştirme (O/R Tasarımcısı)
Dönüş türü bir <xref:System.Data.Linq.DataContext> yöntemi (bir saklı yordamı veya işlevi temel alarak oluşturduğunuz) farklı bağlı olarak burada bırak saklı yordamı veya işlevi **O/R Tasarımcısı**. Bir öğeyi doğrudan mevcut bir varlık sınıfı üzerine sürükleyip bıraktığınızda bir <xref:System.Data.Linq.DataContext> varlık sınıfı için dönüş türüne sahip yöntemi (saklı yordamı veya işlevi tarafından döndürülen veri şeması varlık sınıfı şeklini eşleşiyorsa) oluşturulur. Boş bir alanının bir öğeyi bırak varsa **O/R Tasarımcısı**, <xref:System.Data.Linq.DataContext> otomatik olarak oluşturulan bir tür döndüren yöntem oluşturulur. Dönüş türünü değiştirebilirsiniz bir <xref:System.Data.Linq.DataContext> yöntemleri bölmesine ekledikten sonra yöntemi. İnceleme veya dönüş türünü değiştirmek için bir <xref:System.Data.Linq.DataContext> yöntemi seçin ve **dönüş türü** özelliğinde **özellikleri** penceresi.

> [!NOTE]
> Geri alınamaz <xref:System.Data.Linq.DataContext> kullanarak otomatik olarak oluşturulan türü döndürmek için bir varlık sınıfı için ayarlanmış bir dönüş türüne sahip yöntemleri **özellikleri** penceresi. Geri almak için bir <xref:System.Data.Linq.DataContext> bir otomatik olarak üretilen tür döndürülecek yöntemi özgün veritabanı nesnesi üzerine sürükleyin gerekir **O/R Tasarımcısı** yeniden.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

## <a name="to-change-the-return-type-of-a-datacontext-method-from-the-auto-generated-type-to-an-entity-class"></a>Bir DataContext yöntemin dönüş türü bir varlık sınıfı için otomatik olarak oluşturulan türü değiştirmek için

1. Seçin <xref:System.Data.Linq.DataContext> yöntemleri bölmesinde yöntemi.

2. Seçin **dönüş türü** içinde **özellikleri** penceresi ve ardından kullanılabilir varlık sınıfı içinde **dönüş türü** listesi. İstenen varlık sınıfı listesinde değilse, ekleyin veya oluşturun **O/R Tasarımcısı** listesine eklenecek.

3. Kaydet *.dbml* dosya.

## <a name="to-change-the-return-type-of-a-datacontext-method-from-an-entity-class-back-to-the-auto-generated-type"></a>Bir DataContext yöntemin dönüş türü bir varlık sınıfından otomatik olarak üretilen türe geri değiştirmek için

1. Seçin <xref:System.Data.Linq.DataContext> yönteminde **yöntemleri** bölmesi ve silin.

2. Veritabanı nesneyi sürükleyin **Sunucu Gezgini** veya **veritabanı Gezgini** boş bir alanı üzerine **O/R Tasarımcısı**.

3. Kaydet *.dbml* dosya.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md)
- [Nasıl yapılır: Saklı yordamlara eşlenen DataContext metotları oluşturma (O/R Tasarımcısı)](../data-tools/how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-o-r-designer.md)