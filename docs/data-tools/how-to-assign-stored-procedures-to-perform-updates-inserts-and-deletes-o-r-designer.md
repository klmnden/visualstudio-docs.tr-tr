---
title: Güncelleştirmeyi gerçekleştirmek için saklı yordamları ekleme ve LINQ to SQL O/R Tasarımcısı silme
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e88224ab-ff61-4a3a-b6b8-6f3694546cac
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: aefe5037120636c02b8d3fa73e4ec1fc4bc02a48
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55920450"
---
# <a name="how-to-assign-stored-procedures-to-perform-updates-inserts-and-deletes-or-designer"></a>Nasıl yapılır: Güncelleştirme, ekleme ve silme (O/R Tasarımcısı) gerçekleştirmek için saklı yordamlar atama

Saklı yordamlar eklenebilir **O/R Tasarımcısı** ve tipik olarak yürütülen <xref:System.Data.Linq.DataContext> yöntemleri. ' % S'varsayılan LINQ ekleme, güncelleştirme gerçekleştiren ve bir veritabanına varlık sınıflardan değişiklikler kaydedildiğinde siler SQL çalışma zamanı davranışı için geçersiz kılmak için de kullanılabilir (örneğin, çağrılırken <xref:System.Data.Linq.DataContext.SubmitChanges%2A> yöntemi).

> [!NOTE]
> Depolanmış yordamınızdaki istemciye geri gönderilecek gereken değer döndürürse (örneğin, hesaplanan değerler saklı yordamda), saklı yordamlarınızı çıkış parametreleri oluşturun. Çıktı parametreleri kullanamıyorsanız, O/R tasarımcısı tarafından oluşturulan yazma güvenmek yerine bir kısmi yöntem uygulaması geçersiz kılar. Veritabanı tarafından oluşturulan değerleri için eşlenmiş üyeleri ekleme veya güncelleştirme işlemleri başarıyla tamamlanmadan sonra uygun değerler belirlemeniz gerekir. Daha fazla bilgi için [sorumlulukları geliştirici olarak geçersiz kılma varsayılan davranış](/dotnet/framework/data/adonet/sql/linq/responsibilities-of-the-developer-in-overriding-default-behavior).

> [!NOTE]
> LINQ to SQL veritabanı tarafından oluşturulan değerleri otomatik olarak kimlik (otomatik artış), rowguıdcol (veritabanı tarafından oluşturulan GUID) ve zaman damgası sütunları için işler. Veritabanı üretilmiş değerler diğer sütun türlerinde beklenmedik bir null değer neden olur. Veritabanı tarafından oluşturulan değerleri döndürülecek el ile ayarlamanız <xref:System.Data.Linq.Mapping.ColumnAttribute.IsDbGenerated%2A> için **true** ve <xref:System.Data.Linq.Mapping.ColumnAttribute.AutoSync%2A> aşağıdakilerden birine: [AutoSync.Always](<xref:System.Data.Linq.Mapping.AutoSync.Always>), [AutoSync.OnInsert](<xref:System.Data.Linq.Mapping.AutoSync.OnInsert>), veya [AutoSync.OnUpdate](<xref:System.Data.Linq.Mapping.AutoSync.OnUpdate>).

## <a name="configure-the-update-behavior-of-an-entity-class"></a>Bir varlık sınıfı güncelleştirme davranışını yapılandırma

Varsayılan olarak, bir veritabanı (ekleme, güncelleştirme ve silme) veri LINQ to SQL varlık sınıfları için yapılan değişikliklerle güncelleştirmek için mantığı, LINQ to SQL çalışma zamanı tarafından sağlanır. Çalışma zamanı varsayılan tablo (sütun ve birincil anahtar bilgileri) şemaya dayalı INSERT, UPDATE ve DELETE komutlarını oluşturur. Varsayılan davranış istenildiği gibi gerekli ekleme, güncelleştirme ve silme Tablonuzdaki verileri işlemek için gerekli gerçekleştirmek için belirli saklı yordamlar atayarak güncelleştirme davranışını yapılandırabilirsiniz. Varlık sınıflarınızı görünümleriyle eşleme, varsayılan davranışı gibi değil oluşturulduğunda, aynı zamanda bunu yapabilirsiniz. Son olarak, veritabanı saklı yordamlar aracılığıyla tablo erişim gerektirdiğinde güncelleştirme varsayılan davranışı geçersiz kılabilirsiniz.

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

### <a name="to-assign-stored-procedures-to-override-the-default-behavior-of-an-entity-class"></a>Bir varlık sınıfı varsayılan davranışı geçersiz kılmak için saklı yordamlar atama

1.  Açık **LINQ to SQL** Tasarımcısı'nda dosya. (Çift **.dbml** dosyası **Çözüm Gezgini**.)

2.  İçinde **Sunucu Gezgini** veya **veritabanı Gezgini**, genişletme **saklı yordamlar** INSERT, Update, kullanma ve/veya silmek istediğiniz saklı yordamları bulun Varlık sınıfı komutları.

3.  Saklı yordam üzerine sürükleyin **O/R Tasarımcısı**.

     Saklı yordam yöntemler bölmesi eklenen bir <xref:System.Data.Linq.DataContext> yöntemi. Daha fazla bilgi için [DataContext yöntemi (O/R Tasarımcısı)](../data-tools/datacontext-methods-o-r-designer.md).

4.  Güncelleştirmeleri gerçekleştirmek için saklı yordam kullanmak istediğiniz varlık sınıfı seçin.

5.  İçinde **özellikleri** penceresinde komut geçersiz kılmayı seçin (**Ekle**, **güncelleştirme**, veya **Sil**).

6.  Sözcükleri yanındaki üç nokta (...) tıklayın **kullanım çalışma zamanı** açmak için **davranışı Yapılandır** iletişim kutusu.

7.  Seçin **özelleştirme**.

8.  İstenen saklı yordamda **Özelleştir** listesi.

9. Listesini denetleyin **yöntem bağımsız değişkenleri** ve **sınıfı özellikleri** doğrulamak için **yöntem bağımsız değişkenleri** uygun eşleme **sınıfıözellikleri**. Özgün yöntemi bağımsız değişken eşleme (`Original_<ArgumentName>`) özgün özelliklerine (`<PropertyName> (Original)`) için `Update` ve `Delete` komutları.

    > [!NOTE]
    > Adları eşleştiğinde varsayılan olarak, yöntem bağımsız değişkenleri sınıfın özelliklerine eşlenir. Tablo arasında varlık sınıfı adları artık eşleşen özellik değiştirdiyseniz, Tasarımcı doğru Eşleme belirleyemiyorsa eşlemek için eşdeğer sınıf özelliği seçmek olabilir.

10. Tıklayın **Tamam** veya **uygulamak**.

    > [!NOTE]
    >  Tıkladığınız sürece her sınıf ve davranış birleşimini davranışını yapılandırmak devam **Uygula** her değişikliği yaptıktan sonra. Tıklamadan önce sınıf veya davranış değiştirirseniz **Uygula**, bir uyarı iletişim kutusu görünür ve yaptığınız değişiklikleri uygulamak için bir fırsat sunar.

Güncelleştirmeler için varsayılan çalışma zamanı mantığını kullanarak geri almak için yanındaki tıklayın **Ekle**, **güncelleştirme**, veya **Sil** komutunu **özellikleri**  penceresi ve ardından **çalışma zamanı kullanmak** içinde **davranışı Yapılandır** iletişim kutusu.

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [DataContext metotları](../data-tools/datacontext-methods-o-r-designer.md)
- [LINQ to SQL (.NET Framework)](/dotnet/framework/data/adonet/sql/linq/index)
- [Ekleme, güncelleştirme ve silme işlemleri (.NET Framework)](/dotnet/framework/data/adonet/sql/linq/insert-update-and-delete-operations)