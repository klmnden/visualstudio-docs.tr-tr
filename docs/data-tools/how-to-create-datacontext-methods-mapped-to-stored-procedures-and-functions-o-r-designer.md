---
title: DataContext metotlarını sprocs ve işlevlerle eşleyin (O-R Designer)
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e7ca32f1-50b3-48af-ad92-ceafd749296a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 4c3769634bfbeb98fcc31e5c074177d950248292
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71252903"
---
# <a name="how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-or-designer"></a>Nasıl yapılır: Saklı yordamlara eşlenen DataContext metotları oluşturma (O/R Tasarımcısı)

Saklı yordamları ve işlevleri Yöntem olarak <xref:System.Data.Linq.DataContext> **O/R tasarımcısına** ekleyebilirsiniz. Yöntemi çağırmak ve gerekli parametreleri geçirmek, veritabanında saklı yordamı veya işlevi çalıştırır ve <xref:System.Data.Linq.DataContext> yöntemin dönüş türündeki verileri döndürür. Yöntemler hakkında <xref:System.Data.Linq.DataContext> ayrıntılı bilgi için bkz. [DataContext yöntemleri (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md).

> [!NOTE]
> Ayrıca, değişiklikler varlık sınıflarından veritabanına kaydedildiğinde ekleme, güncelleştirme [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] ve silme işlemleri gerçekleştiren varsayılan çalışma zamanı davranışını geçersiz kılmak için saklı yordamları kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Güncelleştirme, ekleme ve silme işlemleri gerçekleştirmek için saklı yordamlar atayın (O/R Designer)](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md).

## <a name="create-datacontext-methods"></a>DataContext yöntemleri oluşturma

Saklı yordamları veya <xref:System.Data.Linq.DataContext> işlevleri <strong>Sunucu Gezgini veya * * veritabanı Gezgini</strong> ' dan **O/R tasarımcısına**sürükleyerek Yöntemler oluşturabilirsiniz.

> [!NOTE]
> Oluşturulan <xref:System.Data.Linq.DataContext> metodun dönüş türü, saklı yordamı veya işlevi **O/R tasarımcısında**nerede bıraktığınızda olduğuna bağlı olarak farklılık gösterir. Öğelerin doğrudan mevcut bir varlık sınıfına düşürülme, varlık <xref:System.Data.Linq.DataContext> sınıfının dönüş türüyle bir yöntem oluşturur. **O/R tasarımcısının** boş bir alanına öğe bırakma, otomatik olarak oluşturulan bir <xref:System.Data.Linq.DataContext> tür döndüren bir yöntem oluşturur. Bir <xref:System.Data.Linq.DataContext> yöntemin dönüş türünü, **Yöntemler** bölmesine eklendikten sonra değiştirebilirsiniz. Bir <xref:System.Data.Linq.DataContext> yöntemin dönüş türünü incelemek veya değiştirmek için, bunu seçin ve **Özellikler** penceresinde **dönüş türü** özelliğini inceleyin. Daha fazla bilgi için [nasıl yapılır: Bir DataContext yönteminin (O/R Designer)](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md)dönüş türünü değiştirin.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-create-datacontext-methods-that-return-automatically-generated-types"></a>Otomatik olarak oluşturulan türleri döndüren DataContext yöntemleri oluşturmak için

1. **Sunucu Gezgini** veya **veritabanı Gezgini**' de, çalışmakta olduğunuz veritabanının **saklı yordamlar** düğümünü genişletin.

2. İstenen saklı yordamı bulun ve **u/R tasarımcısının**boş bir alanına sürükleyin.

     Yöntemi otomatik olarak oluşturulan bir dönüş türüyle oluşturulur ve Yöntemler bölmesinde görünür. <xref:System.Data.Linq.DataContext>

### <a name="to-create-datacontext-methods-that-have-the-return-type-of-an-entity-class"></a>Bir varlık sınıfının dönüş türüne sahip DataContext yöntemleri oluşturmak için

1. **Sunucu Gezgini** veya **veritabanı Gezgini**' de, çalışmakta olduğunuz veritabanının **saklı yordamlar** düğümünü genişletin.

2. İstenen saklı yordamı bulun ve **o/R tasarımcısında**mevcut bir varlık sınıfının üzerine sürükleyin.

     Yöntemi, seçilen varlık sınıfının dönüş türüyle oluşturulur ve Yöntemler bölmesinde görünür. <xref:System.Data.Linq.DataContext>

> [!NOTE]
> Mevcut <xref:System.Data.Linq.DataContext> yöntemlerin dönüş türünü değiştirme hakkında daha fazla bilgi için bkz [. nasıl yapılır: Bir DataContext yönteminin (O/R Designer)](../data-tools/how-to-change-the-return-type-of-a-datacontext-method-o-r-designer.md)dönüş türünü değiştirin.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [DataContext yöntemleri (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md)
- [İzlenecek yol: LINQ to SQL sınıfları oluşturma](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [Visual Basic LINQ 'e giriş](/dotnet/visual-basic/programming-guide/language-features/linq/introduction-to-linq)
- [C# üzerinde LINQ](/dotnet/csharp/linq/linq-in-csharp)
