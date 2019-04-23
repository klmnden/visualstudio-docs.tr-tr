---
title: Veri kümelerindeki verileri düzenleme
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- datasets [Visual Basic], editing data
- data [Visual Studio], editing in datasets
ms.assetid: 50d5c580-fbf7-408f-be70-e63ac4f4d0eb
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: d693113db28acc456625f7c22b671006ed17038b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60096991"
---
# <a name="edit-data-in-datasets"></a>Veri kümelerindeki verileri düzenleme
Herhangi bir veritabanı tablosundaki verileri çok düzenlediğiniz gibi veri tablolardaki verileri düzenleyin. İşlem ekleme, güncelleştirme ve tablodaki kayıtları silme içerebilir. Verilere bağlı formunda, hangi alanların kullanıcı tarafından düzenlenebilir olduğunu belirtebilirsiniz. Bu gibi durumlarda, böylece değişiklikleri veritabanına geri daha sonra gönderilebilecek tüm değişiklik izleme veri bağlama altyapı işler. Verileri program aracılığıyla düzenlemeleri yapın ve bu değişiklikleri veritabanına geri göndermek istediğinize, nesneleri ve değişiklik izleme bunu yöntemleri kullanmanız gerekir.

Gerçek veriler değiştirmenin yanı sıra, ayrıca Sorgulayabileceğiniz bir <xref:System.Data.DataTable> verilerin belirli satırları döndürür. Örneğin, ayrı satırlara, satırları (özgün ve önerilen) belirli sürümleri, değiştirilen satırları veya hatalar içeren satırların sorgu.

## <a name="to-edit-rows-in-a-dataset"></a>Bir veri kümesindeki satırları düzenleme
Mevcut bir satırı içinde düzenlemek için bir <xref:System.Data.DataTable>, bulmanız gerekir <xref:System.Data.DataRow> düzenleyin ve ardından istenen sütunlar için güncelleştirilmiş değerleri atamak istiyorsunuz.

Satır dizini bilmiyorsanız istediğiniz düzen kullanın `FindBy` yöntemi birincil anahtara göre aramak için:

[!code-csharp[VbRaddataEditing#3](../data-tools/codesnippet/CSharp/edit-data-in-datasets_1.cs)]
[!code-vb[VbRaddataEditing#3](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_1.vb)]

Satır dizini biliyorsanız erişebilir ve satır şu şekilde düzenler:

[!code-csharp[VbRaddataEditing#5](../data-tools/codesnippet/CSharp/edit-data-in-datasets_2.cs)]
[!code-vb[VbRaddataEditing#5](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_2.vb)]

## <a name="to-insert-new-rows-into-a-dataset"></a>Bir veri kümesine satırlar eklemek için
Verilere bağlı denetimler genellikle kullanan uygulamalar üzerinden yeni kayıt ekleme **yeni Ekle** düğmesini bir [BindingNavigator denetimine](/dotnet/framework/winforms/controls/bindingnavigator-control-windows-forms).

El ile yeni kayıtlar ekleme için yeni bir veri satırı üzerinde DataTable yöntemi çağırarak oluşturun. Ardından, satır <xref:System.Data.DataRow> koleksiyon (<xref:System.Data.DataTable.Rows%2A>), <xref:System.Data.DataTable>:

[!code-csharp[VbRaddataEditing#1](../data-tools/codesnippet/CSharp/edit-data-in-datasets_3.cs)]
[!code-vb[VbRaddataEditing#1](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_3.vb)]

Veri kümesi güncelleştirmeleri veri kaynağına göndermek gereken bilgileri korumak için kullanılması <xref:System.Data.DataRow.Delete%2A> bir veri tablosundan satırları kaldırmak için yöntemi. Örneğin, uygulamanız bir TableAdapter kullanıyorsa (veya <xref:System.Data.Common.DataAdapter>), TableAdapter bağdaştırıcısının `Update` yöntemi olan veritabanındaki satırları siler bir <xref:System.Data.DataRow.RowState%2A> , <xref:System.Data.DataRowState.Deleted>.

Güncelleştirmeleri veri kaynağına geri göndermek uygulamanızı gereksinimi yoksa doğrudan veri satır koleksiyonu erişerek kayıtları kaldırmak mümkündür (<xref:System.Data.DataRowCollection.Remove%2A>).

#### <a name="to-delete-records-from-a-data-table"></a>Bir veri tablosundan kayıtları silmek için

- Çağrı <xref:System.Data.DataRow.Delete%2A> yöntemi bir <xref:System.Data.DataRow>.

     Bu yöntem, fiziksel olarak kayıt kaldırmaz. Bunun yerine, kayıt silme işlemi için işaretler.

    > [!NOTE]
    >  Count özelliği alırsanız bir <xref:System.Data.DataRowCollection>, sonuçta elde edilen sayı silinme için işaretlenmiş kayıtları içerir. Doğru bir silme için işaretlenen olmayan kayıt sayısını almak için bakarak koleksiyon döngü <xref:System.Data.DataRow.RowState%2A> her kaydın özellik. (Kayıt silinmek üzere işaretlenmiş bir <xref:System.Data.DataRow.RowState%2A> , <xref:System.Data.DataRowState.Deleted>.) Alternatif olarak, filtreleri satır durumuna dayalı bir veri kümesinin veri görünümü oluşturabilir ve buradan count özelliği edinin.

Aşağıdaki örnek nasıl çağrılacağını gösterir <xref:System.Data.DataRow.Delete%2A> yöntemin ilk satırında işaretlemek için `Customers` tablo silindi olarak:

[!code-csharp[VbRaddataEditing#8](../data-tools/codesnippet/CSharp/edit-data-in-datasets_4.cs)]
[!code-vb[VbRaddataEditing#8](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_4.vb)]

## <a name="determine-if-there-are-changed-rows"></a>Değiştirilen satırların olup olmadığını belirleme
Bir veri kümesindeki kayıtlara değişiklik yapıldığında, onları yürütene kadar o değişiklikler hakkındaki bilgiler depolanır. Çağırdığınızda değişiklikleri `AcceptChanges` yöntemi veya bir veri kümesi veya veri tablosunun çağırdığınızda `Update` bir Tableadapver ya da veri bağdaştırıcısının yöntemi.

Her veri satırı izlenen iki yolla değişiklikler şunlardır:

- Her veri satırı için ilgili bilgiler içerir, <xref:System.Data.DataRow.RowState%2A> (örneğin, <xref:System.Data.DataRowState.Added>, <xref:System.Data.DataRowState.Modified>, <xref:System.Data.DataRowState.Deleted>, veya <xref:System.Data.DataRowState.Unchanged>).

- Her değiştirilen veri satırı o satırın birden çok sürümünü içerir (<xref:System.Data.DataRowVersion>), özgün sürüm (değişikliklerden önce) ve geçerli sürümü (değişikliklerden sonra). Bir değişiklik olduğunda Beklemede olduğu süre boyunca (ne zaman yanıt süresi <xref:System.Data.DataTable.RowChanging> olay), üçüncü bir sürüm — önerilen sürüm — de kullanılabilir.

<xref:System.Data.DataSet.HasChanges%2A> Yöntemi bir veri kümesinin döndürür `true` kümesinde değişiklik yapılmadıysa. Değiştirilen satırların var olduğunu belirledikten sonra çağırabilirsiniz `GetChanges` yöntemi bir <xref:System.Data.DataSet> veya <xref:System.Data.DataTable> değiştirilen satırlar kümesini geri dönmek için.

#### <a name="to-determine-if-changes-have-been-made-to-any-rows"></a>Bir satırda değişiklik yapılıp yapılmadığını belirlemek için

- Çağrı <xref:System.Data.DataSet.HasChanges%2A> değiştirilen satırları denetlemek için bir veri kümesinin yöntemi.

Aşağıdaki örnek, dönüş değeri denetleyin işlemi gösterilmektedir <xref:System.Data.DataSet.HasChanges%2A> adlı bir veri kümesinde değiştirilen satırların olup olmadığını algılamak için `NorthwindDataset1`:

[!code-csharp[VbRaddataEditing#12](../data-tools/codesnippet/CSharp/edit-data-in-datasets_5.cs)]
[!code-vb[VbRaddataEditing#12](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_5.vb)]

## <a name="determine-the-type-of-changes"></a>Değişikliklerin türünü belirleme
Ne tür değişiklikleri görmek için yapıldı bir veri kümesinde bir değer aktararak de göz atabilirsiniz <xref:System.Data.DataRowState> sabit listesine <xref:System.Data.DataSet.HasChanges%2A> yöntemi.

#### <a name="to-determine-what-type-of-changes-have-been-made-to-a-row"></a>Belirlemek için ne tür değişiklikler yapıldığını satır

- Başarılı bir <xref:System.Data.DataRowState> değerini <xref:System.Data.DataSet.HasChanges%2A> yöntemi.

Aşağıdaki örnekte adlı veri kümesini denetlemek nasıl gösterir `NorthwindDataset1` herhangi bir yeni satır kendisine eklenmiş olursa belirlemek için:

[!code-csharp[VbRaddataEditing#13](../data-tools/codesnippet/CSharp/edit-data-in-datasets_6.cs)]
[!code-vb[VbRaddataEditing#13](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_6.vb)]

## <a name="to-locate-rows-that-have-errors"></a>Hatalar içeren satırların bulmak için
Tek tek sütunlara ve veri satırı çalışırken hatalarla karşılaşabilirsiniz. Denetleyebilirsiniz `HasErrors` hataları içinde mevcut olup olmadığını belirlemek için özellik bir <xref:System.Data.DataSet>, <xref:System.Data.DataTable>, veya <xref:System.Data.DataRow>.

1. Denetleme `HasErrors` kümesinde herhangi bir hata olup olmadığını görmek için özellik.

2. Varsa `HasErrors` özelliği `true`, tablolar, koleksiyonlarına yinelemek ve ardından hata satırı bulur. satırlar, aracılığıyla.

[!code-csharp[VbRaddataEditing#23](../data-tools/codesnippet/CSharp/edit-data-in-datasets_7.cs)]
[!code-vb[VbRaddataEditing#23](../data-tools/codesnippet/VisualBasic/edit-data-in-datasets_7.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'daki veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md)