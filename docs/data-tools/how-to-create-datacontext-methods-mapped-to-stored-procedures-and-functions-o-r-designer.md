---
title: Sprocs ve işlevlere (O R Designer) Map DataContext yöntemi
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e7ca32f1-50b3-48af-ad92-ceafd749296a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 3051820be7972af93419833cc62617f6d7e524da
ms.sourcegitcommit: 117ece52507e86c957a5fd4f28d48a0057e1f581
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2019
ms.locfileid: "66260490"
---
# <a name="how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-or-designer"></a>Nasıl yapılır: Saklı yordamlara eşlenen DataContext metotları oluşturma (O/R Tasarımcısı)

Saklı yordamları ve işlevleri için ekleyebileceğiniz **O/R Tasarımcısı** olarak <xref:System.Data.Linq.DataContext> yöntemleri. Yöntemini çağırarak ve gerekli parametrelerin geçirme veritabanında saklı yordamı veya işlevi çalıştırır ve verileri dönüş türünü döndüren <xref:System.Data.Linq.DataContext> yöntemi. İlgili ayrıntılı bilgi için <xref:System.Data.Linq.DataContext> yöntemleri bkz [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md).

> [!NOTE]
> Varsayılan geçersiz kılmak için saklı yordamları kullanabilirsiniz [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] ekleme, güncelleştirme gerçekleştiren ve bir veritabanına varlık sınıflardan değişiklikler kaydedildiğinde siler çalışma zamanı davranışı. Daha fazla bilgi için [nasıl yapılır: Güncelleştirme, ekleme ve silme (O/R Tasarımcısı) gerçekleştirmek için saklı yordamlar atama](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md).

## <a name="create-datacontext-methods"></a>DataContext-metotları oluşturma

Oluşturabileceğiniz <xref:System.Data.Linq.DataContext> sürükleyerek yöntemler depolanan yordamları veya işlevlerden <strong>Sunucu Gezgini veya ** veritabanı Gezgini</strong> üzerine **O/R Tasarımcısı**.

> [!NOTE]
> Dönüş türü oluşturulan <xref:System.Data.Linq.DataContext> yöntemi farklı bağlı olarak burada saklı yordamı bırakın veya işlevini **O/R Tasarımcısı**. Öğeleri doğrudan mevcut bir varlık sınıfı üzerine bırakarak oluşturur bir <xref:System.Data.Linq.DataContext> yöntemi varlık sınıfı dönüş türüne sahip. Öğeleri boş bir alanının bırakarak **O/R Tasarımcısı** oluşturur bir <xref:System.Data.Linq.DataContext> otomatik olarak oluşturulan bir tür döndüren yöntem. Dönüş türünü değiştirebilirsiniz bir <xref:System.Data.Linq.DataContext> eklemeden sonra yöntemi **yöntemleri** bölmesi. İnceleme veya dönüş türünü değiştirmek için bir <xref:System.Data.Linq.DataContext> yöntemi seçin ve İnceleme **dönüş türü** özelliğinde **özellikleri** penceresi. Daha fazla bilgi için [nasıl yapılır: (O/R Tasarımcısı) bir DataContext yöntemin dönüş türünü değiştirmek](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md).

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-create-datacontext-methods-that-return-automatically-generated-types"></a>DataContext oluşturmak için otomatik olarak döndüren yöntemler türü oluşturuldu

1. İçinde **Sunucu Gezgini** veya **veritabanı Gezgini**, genişletme **saklı yordamlar** birlikte çalıştığınız veritabanı düğümü.

2. İstenen saklı yordamı bulun ve boş bir alanı sürükleyin **O/R Tasarımcısı**.

     <xref:System.Data.Linq.DataContext> Yöntemi otomatik olarak oluşturulan bir dönüş türü ile oluşturulur ve görünür **yöntemleri** bölmesi.

### <a name="to-create-datacontext-methods-that-have-the-return-type-of-an-entity-class"></a>Bir varlık sınıfı dönüş türüne sahip bir DataContext yöntemi oluşturmak için

1. İçinde **Sunucu Gezgini** veya **veritabanı Gezgini**, genişletme **saklı yordamlar** birlikte çalıştığınız veritabanı düğümü.

2. İstenen saklı yordamı bulun ve varolan bir varlık sınıfı sürükleyin **O/R Tasarımcısı**.

     <xref:System.Data.Linq.DataContext> Yöntemi seçili varlık sınıfı, dönüş türü ile oluşturulur ve görünür **yöntemleri** bölmesi.

> [!NOTE]
> Var olan dönüş türünü değiştirme hakkında bilgi için <xref:System.Data.Linq.DataContext> yöntemleri bkz [nasıl yapılır: (O/R Tasarımcısı) bir DataContext yöntemin dönüş türünü değiştirmek](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md)
- [İzlenecek yol: SQL sınıflarına LINQ oluşturma](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [Visual Basic'de LINQ'e giriş](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)
- [C# üzerinde LINQ](/dotnet/csharp/linq/linq-in-csharp)
