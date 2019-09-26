---
title: LINQ to SQL sınıfları tablolarda/görünümlerde eşleme (O-R Designer)
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 0fb78bbc-7a78-4ab4-b32f-85ece912e660
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 2b34212ddad2bc5d69778f973d5975655431a829
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253006"
---
# <a name="how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-or-designer"></a>Nasıl yapılır: Tablolar ve görünümler ile eşlenen LINQ to SQL sınıfları oluşturma (O/R Tasarımcısı)

[!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)]veritabanı tablolarıyla ve görünümleriyle eşlenmiş sınıflar *varlık sınıfları*olarak adlandırılır. Varlık sınıfı bir kayıtla eşlenir, ancak bir varlık sınıfının bireysel özellikleri bir kaydı oluşturan ayrı sütunlara eşlenir. **Sunucu Gezgini** veya **veritabanı Gezgini** tabloları veya görünümleri [Visual Studio 'daki LINQ to SQL araçlarına](../data-tools/linq-to-sql-tools-in-visual-studio2.md)sürükleyerek veritabanı tablolarını veya görünümlerini temel alan varlık sınıfları oluşturun. **O/R Tasarımcısı** sınıfları oluşturur ve işlevleri etkinleştirmek [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] için belirli öznitelikleri uygular (öğesinin <xref:System.Data.Linq.DataContext>veri iletişimi ve düzenlenme özellikleri). Sınıflar hakkında [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] ayrıntılı bilgi için bkz. [LINQ to SQL nesne modeli](/dotnet/framework/data/adonet/sql/linq/the-linq-to-sql-object-model).

> [!NOTE]
> **O/R Tasarımcısı** yalnızca 1:1 eşleme ilişkileri desteklediğinden, bir Basit Nesne İlişkisel eşleyicisidir. Diğer bir deyişle, bir varlık sınıfı yalnızca 1:1 eşleme ilişkisi olan bir veritabanı tablosu veya görünümü olabilir. Bir varlık sınıfını birden çok tabloya eşleme gibi karmaşık eşleme desteklenmez. Ancak, bir varlık sınıfını birden çok ilişkili tabloyu birleştiren bir görünümle eşleyebilirsiniz.

## <a name="create-linq-to-sql-classes-that-are-mapped-to-database-tables-or-views"></a>Veritabanı tabloları veya görünümleriyle eşlenmiş LINQ to SQL sınıfları oluşturma

**Sunucu Gezgini** veya **veritabanı Gezgini** içindeki tabloları ya da görünümleri **O/R tasarımcısına** sürüklemek, güncelleştirme gerçekleştirmek için kullanılan <xref:System.Data.Linq.DataContext> yöntemlerin yanı sıra varlık sınıfları oluşturur.

Varsayılan olarak, [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] çalışma zamanı güncelleştirilebilir bir varlık sınıfından değişiklikleri veritabanına geri kaydetmek için mantık oluşturur. Bu mantık, tablonun şemasını temel alır (sütun tanımları ve birincil anahtar bilgileri). Bu davranışı istemiyorsanız, varsayılan [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] çalışma zamanı davranışını kullanmak yerine ekleme, güncelleştirme ve silme işlemleri gerçekleştirmek için saklı yordamları kullanmak üzere bir varlık sınıfı yapılandırabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Güncelleştirme, ekleme ve silme işlemleri gerçekleştirmek için saklı yordamlar atayın (O/R Designer)](../data-tools/how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-o-r-designer.md).

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-create-linq-to-sql-classes-that-are-mapped-to-database-tables-or-views"></a>Veritabanı tabloları veya görünümleriyle eşlenmiş LINQ to SQL sınıfları oluşturmak için

1. **Sunucu** veya **veritabanı Gezgini**' de, **Tablolar** veya **Görünümler** ' i genişletin ve uygulamanızda kullanmak istediğiniz veritabanı tablosu veya görünümünü bulun.

2. Tabloyu veya görünümü **O/R tasarımcısına**sürükleyin.

     Bir varlık sınıfı oluşturulur ve tasarım yüzeyinde görüntülenir. Varlık sınıfı, seçili tablodaki veya görünümdeki sütunlarla eşlenen özelliklere sahiptir.

## <a name="create-an-object-data-source-and-display-the-data-on-a-form"></a>Bir nesne veri kaynağı oluşturma ve verileri bir formda görüntüleme

**O/R tasarımcısını**kullanarak varlık sınıfları oluşturduktan sonra, bir nesne veri kaynağı oluşturabilir ve [veri kaynakları penceresini](add-new-data-sources.md#data-sources-window) varlık sınıflarıyla doldurabilirsiniz.

### <a name="to-create-an-object-data-source-based-on-linq-to-sql-entity-classes"></a>LINQ to SQL varlık sınıflarına dayalı bir nesne veri kaynağı oluşturmak için

1. Projeyi derlemek için **Oluştur** menüsünde **çözüm oluştur** ' a tıklayın.

2. Veri **kaynakları** penceresini açmak Için, **veri** menüsünde **veri kaynaklarını göster**' e tıklayın.

3. **Veri kaynakları** penceresinde **Yeni veri kaynağı Ekle**' ye tıklayın.

4. **Veri kaynağı türü seçin** sayfasında **nesne** ' ye tıklayın ve ardından **İleri**' ye tıklayın.

5. Düğümleri genişletin ve sınıfınızı bulun ve seçin.

    > [!NOTE]
    > **Müşteri** sınıfı kullanılabilir değilse, Sihirbazı iptal edin, projeyi derleyin ve Sihirbazı yeniden çalıştırın.

6. Veri kaynağını oluşturmak ve **veri kaynakları** penceresine **Müşteri** varlık sınıfını eklemek için **son** ' a tıklayın.

7. Öğeleri **veri kaynakları** penceresinden bir form üzerine sürükleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio 'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [İzlenecek yol: LINQ to SQL sınıfları oluşturma (O-R Designer)](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [DataContext yöntemleri (O/R Designer)](../data-tools/datacontext-methods-o-r-designer.md)
- [Nasıl yapılır: Saklı yordamlara eşlenen DataContext metotları oluşturma (O/R Tasarımcısı)](../data-tools/how-to-create-datacontext-methods-mapped-to-stored-procedures-and-functions-o-r-designer.md)
- [LINQ to SQL nesne modeli](/dotnet/framework/data/adonet/sql/linq/the-linq-to-sql-object-model)
- [İzlenecek yol: Varlık sınıflarının ekleme, güncelleştirme ve silme davranışını özelleştirme](../data-tools/walkthrough-customizing-the-insert-update-and-delete-behavior-of-entity-classes.md)
- [Nasıl yapılır: LINQ to SQL sınıfları arasında ilişkilendirme (ilişki) oluşturma (O/R Tasarımcısı)](../data-tools/how-to-create-an-association-relationship-between-linq-to-sql-classes-o-r-designer.md)
