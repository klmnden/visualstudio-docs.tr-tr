---
title: LINQ to SQL sınıfları O/R Tasarımcısı kullanarak arasında bir ilişki oluşturma
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 56133e65-81f3-44c3-bc28-ffdd0671a0d2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 9d7bf1be05ebabcaac319cce591cf82cd2ab5f5d
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60112292"
---
# <a name="how-to-create-an-association-between-linq-to-sql-classes-or-designer"></a>Nasıl yapılır: LINQ to SQL sınıfları (O/R Tasarımcısı) arasında ilişkilendirme oluşturma
Varlık sınıfları arasındaki ilişkilendirmeleri [!INCLUDE[vbtecdlinq](../data-tools/includes/vbtecdlinq_md.md)] veritabanındaki tablolar arasında ilişki benzer. Kullanarak varlık sınıfları arasında ilişkiler oluşturabilirsiniz **ilişkilendirme Düzenleyicisi** iletişim kutusu.

Kullandığınızda, bir üst ve alt sınıfı seçmelisiniz **ilişkilendirme Düzenleyicisi** ilişkilendirme oluşturmak için iletişim kutusu. Birincil anahtarı içeren varlık sınıfı üst sınıftır; yabancı anahtar içeren varlık sınıfı alt sınıfıdır. Örneğin, varlık sınıfları eşleştiren oluşturulup oluşturulmadığını `Northwind Customers` ve `Orders` tablolar `Customer` sınıfı üst sınıfın olacaktır ve `Order` sınıfı alt sınıfı olması.

> [!NOTE]
>  Tablodan sürüklediğinizde **Sunucu Gezgini** veya **veritabanı Gezgini** üzerine **Object Relational Designer** (**O/R Tasarımcısı**), ilişkileri otomatik olarak var olan bir yabancı anahtar ilişkileri veritabanında temel alınarak oluşturulur.

## <a name="association-properties"></a>İlişki özellikleri
İlişkilendirmeyi seçtiğinizde bir ilişkilendirme oluşturduktan sonra **O/R Tasarımcısı**, içindeki bazı yapılandırılabilir özellik vardır **özellikleri** penceresi. (Satır ilgili sınıflar arasında bir ilişkilendirmedir.) Aşağıdaki tabloda bir ilişkilendirmenin özellikleri için açıklamalar sağlar.

|Özellik|Açıklama|
|--------------|-----------------|
|**önem düzeyi**|Bire çok veya birebir ilişki olup olmadığını denetler.|
|**Alt özellik**|Bir koleksiyon veya ilişkilendirme yabancı anahtar tarafındaki alt kayıtlara bir başvuru olan üst bir özellik oluşturulup oluşturulmayacağını belirtir. Arasındaki ilişki, içinde `Customer` ve `Order`, **alt özellik** ayarlanır **True**, adlı bir özellik `Orders` üst sınıf üzerinde oluşturulur.|
|**Üst özellik**|İlişkilendirilen üst sınıfa başvuran alt sınıftaki özellik. Örneğin, arasındaki ilişki içinde `Customer` ve `Order`, adlı bir özellik `Customer` başvuran ilişkili müşterinin sipariş üzerinde oluşturulur `Order` sınıfı.|
|**Katılım özellikleri**|İlişki özellikleri görüntüler ve sağlayan bir **üç nokta** yeniden açılır düğmesini (…) **ilişkilendirme Düzenleyicisi** iletişim kutusu.|
|**benzersiz**|Yabancı hedef sütunların benzersiz bir kısıtlaması olup olmadığını belirtir.|

## <a name="to-create-an-association-between-entity-classes"></a>Varlık sınıfları arasında ilişkilendirme oluşturma

1. İlişkideki üst sınıfın temsil ettiği varlık sınıfı sağ tıklatın, **Ekle**ve ardından **ilişkilendirme**.

2. Doğrulayın doğru **üst sınıf** seçili **ilişkilendirme Düzenleyicisi** iletişim kutusu.

3. Seçin **alt sınıf** birleşik giriş kutusundaki.

4. Seçin **ilişkilendirme özellikleri** sınıfları ilgilidir. Genellikle, bu veritabanında tanımlanan yabancı anahtar ilişkisi eşlenir. Örneğin, `Customers` ve `Orders` association **ilişkilendirme özellikleri** olan `CustomerID` her sınıf için.

5. Tıklayın **Tamam** bir ilişki oluşturmak için.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [İzlenecek yol: SQL sınıflarına LINQ oluşturma](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md)
- [Nasıl yapılır: Birincil anahtarları temsil eder](/dotnet/framework/data/adonet/sql/linq/how-to-represent-primary-keys)