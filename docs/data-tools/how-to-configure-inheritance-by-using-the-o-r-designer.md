---
title: 'Nasıl yapılır: O R Tasarımcısı kullanarak devralmayı yapılandırma'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e594af12-e777-434a-bc08-7dd2dac84cdc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 6430cd3092f6edbc514c7958e07961ccd234c161
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55931266"
---
# <a name="how-to-configure-inheritance-by-using-the-or-designer"></a>Nasıl yapılır: O/R Tasarımcısı kullanarak devralmayı yapılandırma
**Object Relational Designer** (**O/R Tasarımcısı**) ilişkisel sistemlerde sık uygulandığı şekilde tek tablolu devralma kavramını destekler. Tek tablo devralma işleminde üst bilgi hem de alt bilgi için alanları içeren bir tek veritabanı tablosu yok. İlişkisel verilerle bir ayrıştırıcı sütunu her kaydın ait olduğu sınıfı belirleyen bir değer içerir.

Örneğin, bir `Persons` herkesin şirket tarafından kullanılan içeren tablo. Bazı kişiler çalışanlar ve bazı kişiler yöneticileri. `Persons` Tablo adlı bir sütun içeren `EmployeeType` 1 değeri, yöneticileri ve 2 değerini çalışanlar için sahip; bu ayrıştırıcı sütunu. Bu senaryoda, çalışanların öğesinin oluşturabilir ve sınıf olan kayıtlar ile doldurmak bir `EmployeeType` değeri 2'dir. Ayrıca her sınıfların geçerli olmayan sütunları kaldırabilirsiniz.

Devralma kullanır (ve ilişkisel verilere karşılık gelir) nesne modeli oluşturma biraz kafa karıştırıcı olabilir. Aşağıdaki yordam kalıtım yapılandırmak için gereken adımları özetler **O/R Tasarımcısı**. Verileri kullanan bir kılavuz sağlanır için var olan bir tablo ve sütunlara başvuruda bulunmadan aşağıdaki genel adımları zor olabilir. Devralma kullanarak yapılandırmaya yönelik ayrıntılı adım adım yönergeler için **O/R Tasarımcısı**, bkz: [izlenecek yol: Tek tablo devralma (O/R Tasarımcısı) kullanarak SQL sınıflarına LINQ oluşturma](../data-tools/walkthrough-creating-linq-to-sql-classes-by-using-single-table-inheritance-o-r-designer.md).

## <a name="to-create-inherited-data-classes"></a>Devralınan veri sınıfları oluşturmak için

1.  Açık **O/R Tasarımcısı** ekleyerek bir **LINQ to SQL sınıfları** varolan bir Visual Basic öğesine veya C# proje.

2.  Temel sınıf olarak kullanmak istediğiniz tabloyu sürükleyin **O/R Tasarımcısı**.

3.  İkinci bir kopyası tablosunu sürükleyin **O/R Tasarımcısı** ve yeniden adlandırın. Türetilmiş bir sınıf ya da alt budur.

4.  Tıklayın **devralma** içinde **Object Relational Designer** sekmesinde **araç kutusu**, alt (adlandırdığınız tablosu) tıklayın ve ardından temel sınıfa bağlanın.

    > [!NOTE]
    >  Tıklayın **devralma** öğesi **araç kutusu** ve fare düğmesini bırakın, 3. adımda oluşturulan sınıf ikinci bir kopyası tıklatın ve 2. adımda oluşturduğunuz ilk sınıf'ye tıklayın. Devralım çizgisi üzerindeki oku ilk sınıfa işaret eder.

5.  Her sınıfta görünmesini istemiyorsanız ve ilişkileri için kullanılmayan tüm nesne özellikleri silin. Nesne özellikleri ilişkilendirmeler için kullanılan silmeye çalışıyorsanız, bir hata alırsınız: [Özellik \<özellik adı > ilişkilendirmesine katıldığından silinemiyor \<ilişkilendirme adı >](../data-tools/the-property-property-name-cannot-be-deleted-because-it-is-participating-in-the-association-association-name.md).

    > [!NOTE]
    >  Türetilmiş bir sınıf kendi temel sınıfta tanımlanan özellikleri devraldığından, aynı sütunlara her sınıfında tanımlanamaz. (Sütunları özellikleri olarak uygulanır.) Temel sınıf özelliğini temel alan ait devralma değiştiricisinin ayarlayarak türetilmiş sınıftaki sütunları oluşturulmasını etkinleştirebilirsiniz. Daha fazla bilgi için [devralma temelleri (Visual Basic)](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics).

6.  İçinde devralım çizgisini seçin **O/R Tasarımcısı**.

7.  İçinde **özellikleri** penceresinde **ayrıştırıcı özelliği** sınıflarınızı kayıtlara ayıran sütun adı.

8.  Ayarlama **türetilen sınıf ayrıştırıcısı değerinin** kaydı devralınan türü olarak atar veritabanındaki değerle özelliği. (Devralınan sınıf belirtmek için kullanılır ve ayrıştırıcı sütunda depolanan değer budur.)

9. Ayarlama **temel sınıf ayrıştırıcı değeri** özelliğini kaydı temel tür olarak belirten değer. (Ayrıştırıcı sütunu depolanır ve temel sınıf belirtmek için kullanılır değer budur.)

10. İsteğe bağlı olarak da ayarlayabilirsiniz **devralma varsayılan** devralma kod tanımlanan eşleşmeyen satırlar yüklenirken kullanılan bir devralma hiyerarşisi içindeki bir tür belirtmek için özellik. Kayıt, kendi ayrıştırıcı sütunu bir değere sahipse, diğer bir deyişle, ya da değer eşleşmiyor **türetilen sınıf ayrıştırıcısı değerinin** veya **temel sınıf ayrıştırıcı değeri** özellikleri, kayıt yükler olarak atanan türü **devralma varsayılan**.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [İzlenecek yol: (O R Designer) SQL sınıflarına LINQ oluşturma](how-to-create-linq-to-sql-classes-mapped-to-tables-and-views-o-r-designer.md)
- [Visual Studio'da verilere erişime](../data-tools/accessing-data-in-visual-studio.md)
- [LINQ to SQL](/dotnet/framework/data/adonet/sql/linq/index)
- [İzlenecek yol: Tek tablo devralma (O/R Tasarımcısı) kullanarak SQL sınıflarına LINQ oluşturma](../data-tools/walkthrough-creating-linq-to-sql-classes-by-using-single-table-inheritance-o-r-designer.md)
- [Devralma temelleri (Visual Basic)](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)
- [Devralma](/dotnet/csharp/programming-guide/classes-and-structs/inheritance)