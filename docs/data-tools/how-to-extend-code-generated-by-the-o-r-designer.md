---
title: 'Nasıl Yapılır: O R tasarımcısı tarafından oluşturulan kodu genişletme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d6d1122e-2f55-4607-8d8b-48c3c22600fb
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 41704ad1f43dadee1efd16102281173215bad4e0
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53933790"
---
# <a name="how-to-extend-code-generated-by-the-or-designer"></a>Nasıl Yapılır: O/R tasarımcısı tarafından oluşturulan kodu genişletme
Tarafından oluşturulan kodu **O/R Tasarımcısı** varlık sınıfları ve diğer nesneler üzerinde Tasarımcı yüzeyine değişiklik yapıldığında yeniden oluşturulur. Tasarımcı, kod yeniden oluşturur, bu kod oluşturma işlemi nedeniyle, oluşturulan kod için eklediğiniz herhangi bir kod genellikle üzerine yazılır. **O/R Tasarımcısı** yazılmaz kod içine ekleyebileceğiniz kısmi sınıf dosyaları oluşturmak olanağı sağlar. Bir örneği tarafından oluşturulan kodu kendi kodunuzu ekleme **O/R Tasarımcısı** veri doğrulama (varlık) SQL sınıflarına LINQ to eklemektir. Daha fazla bilgi için [nasıl yapılır: Varlık sınıflarına doğrulama ekleme](../data-tools/how-to-add-validation-to-entity-classes.md).

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

## <a name="add-code-to-an-entity-class"></a>Bir varlık sınıfı için kod ekleyin

### <a name="to-create-a-partial-class-and-add-code-to-an-entity-class"></a>Kısmi bir sınıf oluşturun ve bir varlık sınıfı için kod ekleyin

1.  Yeni bir LINQ to SQL sınıfları dosyası oluşturun veya açın (**.dbml** dosya) içinde **O/R Tasarımcısı**. (Çift **.dbml** dosyası **Çözüm Gezgini** veya **veritabanı Gezgini**.)

2.  İçinde **O/R Tasarımcısı**, doğrulama ekleyin ve ardından istediğiniz sınıfı sağ **kodu görüntüle**.

     Seçilen varlık sınıfı için bir parçalı sınıf Kod Düzenleyicisi açılır.

3.  Kısmi sınıf bildiriminde varlık sınıfı için kodunuzu ekleyin.

## <a name="add-code-to-a-datacontext"></a>Bir DataContext için kod ekleyin

### <a name="to-create-a-partial-class-and-add-code-to-a-datacontext"></a>Kısmi bir sınıf oluşturun ve bir DataContext için kod ekleyin

1.  Yeni bir LINQ to SQL sınıfları dosyası oluşturun veya açın (**.dbml** dosya) içinde **O/R Tasarımcısı**. (Çift **.dbml** dosyası **Çözüm Gezgini** veya **veritabanı Gezgini**.)

2.  İçinde **O/R Tasarımcısı**, Tasarımcı üzerinde boş bir alana sağ tıklayın ve ardından **kodu görüntüle**.

     Kod Düzenleyicisi ile kısmi bir sınıf için DataContext açılır.

3.  Kısmi sınıf bildiriminde DataContext için kodunuzu ekleyin.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [İzlenecek yol: (O R Designer) SQL sınıflarına LINQ oluşturma](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)