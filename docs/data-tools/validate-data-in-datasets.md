---
title: Veri kümelerindeki verileri doğrulama
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DataTable.ColumnChanging
- System.Data.DataTable.ColumnChanging
- System.Data.DataTable.RowChanging
- DataTable.RowChanging
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data validation, datasets
- data validation
- validating data, datasets
- updating datasets, validating data
ms.assetid: 79500596-1e4d-478e-a991-a636fd73a622
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: 80f258e87bd7bd197460d5ff9ab29b6964347f7c
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68925412"
---
# <a name="validate-data-in-datasets"></a>Veri kümelerindeki verileri doğrulama
Verilerin doğrulanması, veri nesnelerine girilen değerlerin bir veri kümesinin şeması içindeki kısıtlamalara uygun olduğunu onaylama işlemidir. Doğrulama işlemi, bu değerlerin uygulamanız için oluşturulan kurallara göre olduğunu da onaylar. Temel alınan veritabanına güncelleştirmeleri göndermeden önce verileri doğrulamak iyi bir uygulamadır. Bu, hataların yanı sıra bir uygulama ve veritabanı arasındaki gidiş dönüş sayısını azaltır.

Veri kümesine yazılan verilerin veri kümesine doğrulama denetimleri oluşturarak geçerli olduğunu doğrulayabilirsiniz. Veri kümesi, bir formda, bir bileşen içinde veya başka bir şekilde bir biçimde, doğrudan denetimler tarafından değil, güncelleştirmenin nasıl gerçekleştirildiğine bakılmaksızın verileri denetleyebilir. Veri kümesi uygulamanızın bir parçası olduğundan (veritabanı arka ucunun aksine) uygulamaya özgü doğrulama oluşturmak için mantıksal bir yerdir.

Uygulamanıza doğrulama eklemek için en iyi yer, DataSet 'in kısmi sınıf dosyasında bulunur. Ya [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] da[!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)]' de **veri kümesi Tasarımcısı** açın ve doğrulama oluşturmak istediğiniz sütun veya tabloya çift tıklayın. Bu eylem otomatik olarak bir <xref:System.Data.DataTable.ColumnChanging> veya <xref:System.Data.DataTable.RowChanging> olay işleyicisi oluşturur.

## <a name="validate-data"></a>Verileri doğrulama
Bir veri kümesi içinde doğrulama işlemi aşağıdaki yollarla gerçekleştirilir:

- Değişiklik sırasında tek bir veri sütunundaki değerleri kontrol eden, uygulamaya özgü bir doğrulama oluşturarak. Daha fazla bilgi için [nasıl yapılır: Sütun değişiklikleri](validate-data-in-datasets.md)sırasında verileri doğrulayın.

- Tüm veri satırları değiştirilirken, verileri değerlere denetleyerek uygulamaya özgü doğrulama bilgilerinizi oluşturarak. Daha fazla bilgi için [nasıl yapılır: Satır değişiklikleri](validate-data-in-datasets.md)sırasında verileri doğrulayın.

- Veri kümesinin gerçek şema tanımının bir parçası olarak anahtarlar, benzersiz kısıtlamalar ve benzeri bir oluşturma.

- <xref:System.Data.DataColumn> , Ve <xref:System.Data.DataColumn.MaxLength%2A> gibinesnenin<xref:System.Data.DataColumn.AllowDBNull%2A>özellikleriniayarlayarak. <xref:System.Data.DataColumn.Unique%2A>

Bir kayıtta değişiklik yapıldığında <xref:System.Data.DataTable> nesne tarafından birkaç olay tetiklenir:

- <xref:System.Data.DataTable.ColumnChanging> Ve<xref:System.Data.DataTable.ColumnChanged> olayları, tek bir sütundaki her değişiklikten sonra ve sonrasında oluşturulur. Bu <xref:System.Data.DataTable.ColumnChanging> olay, belirli sütunlardaki değişiklikleri doğrulamak istediğinizde yararlı olur. Önerilen değişiklik hakkındaki bilgiler, olaya bir bağımsız değişken olarak geçirilir.
- <xref:System.Data.DataTable.RowChanging> Ve<xref:System.Data.DataTable.RowChanged> olayları, bir satırdaki herhangi bir değişiklik sırasında ve sonrasında oluşturulur. <xref:System.Data.DataTable.RowChanging> Olay daha genel. Bu, satırda bir yerde değişiklik gerçekleştiğini gösterir, ancak hangi sütunun değiştiğini bilemezsiniz.

Varsayılan olarak, bir sütunda yapılan her değişiklik dört olay oluşturur. Birincisi <xref:System.Data.DataTable.ColumnChanging> , değiştirilmekte olan belirli <xref:System.Data.DataTable.ColumnChanged> bir sütunun ve olaylardır. Sonraki olaylar <xref:System.Data.DataTable.RowChanging> ve <xref:System.Data.DataTable.RowChanged> olaylardır. Satırda birden fazla değişiklik yapılırsa, olaylar her değişiklik için oluşturulur.

> [!NOTE]
> Veri satırının <xref:System.Data.DataRow.BeginEdit%2A> metodu, <xref:System.Data.DataTable.RowChanging> her sütun değişikliğinden sonra ve <xref:System.Data.DataTable.RowChanged> olaylarını kapatır. Bu durumda, <xref:System.Data.DataRow.EndEdit%2A> <xref:System.Data.DataTable.RowChanging> ve <xref:System.Data.DataTable.RowChanged> olayları yalnızca bir kez oluşturulduğunda, olay çağrılana kadar olay oluşturulmaz. Daha fazla bilgi için bkz. [veri kümesini doldururken kısıtlamaları](../data-tools/turn-off-constraints-while-filling-a-dataset.md)kapatma.

Seçtiğiniz olay, doğrulamanın ne kadar ayrıntılı olmasını istediğinize bağlıdır. Bir sütun değiştiğinde bir hatayı hemen yakalayabilmeniz önemliyse <xref:System.Data.DataTable.ColumnChanging> olayını kullanarak doğrulama oluşturun. Aksi takdirde, bir <xref:System.Data.DataTable.RowChanging> kerede birkaç hata oluşmasına neden olabilecek olayını kullanın. Ayrıca, verileriniz bir sütunun değerinin başka bir sütunun içeriğine göre doğrulanması için yapılandırılmış ise, <xref:System.Data.DataTable.RowChanging> olay sırasında doğrulama işlemini gerçekleştirin.

Kayıtlar güncelleştirilirken, <xref:System.Data.DataTable> nesne, değişiklikler yapıldığında ve değişiklikler yapıldıktan sonra yanıt verebildiği olaylar oluşturur.

Uygulamanız türü belirtilmiş bir veri kümesi kullanıyorsa, türü kesin belirlenmiş olay işleyicileri oluşturabilirsiniz. Bu, işleyicileri oluşturabileceğiniz, için ek olarak belirlenmiş dört olay ekler: `dataTableNameRowChanging`, `dataTableNameRowChanged`, `dataTableNameRowDeleting`, ve `dataTableNameRowDeleted`. Bu tür olay işleyicileri, kodunuzun daha kolay yazılması ve okunması için tablonuzun sütun adlarını içeren bir bağımsız değişken iletir.

## <a name="data-update-events"></a>Veri güncelleştirme olayları

|Olay|Açıklama|
|-----------|-----------------|
|<xref:System.Data.DataTable.ColumnChanging>|Bir sütundaki değer değiştiriliyor. Bu olay, önerilen yeni değerle birlikte satır ve sütunu size geçirir.|
|<xref:System.Data.DataTable.ColumnChanged>|Bir sütundaki değer değiştirildi. Olay satırı ve sütunu, önerilen değerle birlikte size geçirir.|
|<xref:System.Data.DataTable.RowChanging>|Bir <xref:System.Data.DataRow> nesne üzerinde yapılan değişiklikler veri kümesine geri aktarılmalıdır. <xref:System.Data.DataRow.BeginEdit%2A> <xref:System.Data.DataTable.ColumnChanging> Yöntemini çağırdıysanızolay,olayoluşturulduktanhemensonrabirsütundakiherdeğişiklikiçinoluşturulur.<xref:System.Data.DataTable.RowChanging> Değişiklik yapmadan önce <xref:System.Data.DataRow.BeginEdit%2A> çağrılırsa <xref:System.Data.DataTable.RowChanging> , olay <xref:System.Data.DataRow.EndEdit%2A> yalnızca yöntemini çağırdığınızda tetiklenir.<br /><br /> Olay, ne tür bir eylem (değişiklik, ekleme, vb.) gerçekleştirildiğinin belirten bir değer ile birlikte size satırı geçirir.|
|<xref:System.Data.DataTable.RowChanged>|Bir satır değiştirildi. Olay, ne tür bir eylem (değişiklik, ekleme, vb.) gerçekleştirildiğinin belirten bir değer ile birlikte size satırı geçirir.|
|<xref:System.Data.DataTable.RowDeleting>|Bir satır siliniyor. Olay, ne tür bir eylem (silme) gerçekleştirildiğinin belirten bir değer ile birlikte size satırı geçirir.|
|<xref:System.Data.DataTable.RowDeleted>|Bir satır silindi. Olay, ne tür bir eylem (silme) gerçekleştirildiğinin belirten bir değer ile birlikte size satırı geçirir.|

<xref:System.Data.DataTable.ColumnChanging>, Veolayları<xref:System.Data.DataTable.RowDeleting> güncelleştirme işlemi sırasında oluşturulur. <xref:System.Data.DataTable.RowChanging> Bu olayları, verileri doğrulamak veya diğer işleme türlerini gerçekleştirmek için kullanabilirsiniz. Güncelleştirme bu olaylar sırasında işlemde olduğundan, bir özel durum oluşturarak iptal edebilirsiniz ve bu da güncelleştirmenin tamamlanmasını önler.

<xref:System.Data.DataTable.ColumnChanged>, Veolayları<xref:System.Data.DataTable.RowDeleted> güncelleştirme başarıyla tamamlandığında oluşturulan bildirim olaylardır. <xref:System.Data.DataTable.RowChanged> Bu olaylar, başarılı bir güncelleştirmeye göre daha fazla işlem yapmak istediğinizde faydalıdır.

## <a name="validate-data-during-column-changes"></a>Sütun değişiklikleri sırasında verileri doğrulama

> [!NOTE]
> **Veri kümesi Tasarımcısı** , bir veri kümesine doğrulama mantığının eklenebileceği kısmi bir sınıf oluşturur. Tasarımcı tarafından oluşturulan veri kümesi, kısmi sınıftaki hiçbir kodu silmez veya değiştirmez.

Bir veri sütunundaki değer, <xref:System.Data.DataTable.ColumnChanging> olaya yanıt vererek değiştiğinde verileri doğrulayabilirsiniz. Bu olay, oluşturulduğunda, geçerli sütun için önerilen değeri<xref:System.Data.DataColumnChangeEventArgs.ProposedValue%2A>içeren bir olay bağımsız değişkeni () geçirir. İçeriğine `e.ProposedValue`göre şunları yapabilirsiniz:

- Hiçbir şey yapmadan önerilen değeri kabul edin.

- Sütun değiştirme olay işleyicisi içinden sütun hatası (<xref:System.Data.DataRow.SetColumnError%2A>) ayarlayarak önerilen değeri reddedin.

- İsteğe bağlı olarak <xref:System.Windows.Forms.ErrorProvider> , kullanıcıya bir hata iletisi göstermek için bir denetim kullanın. Daha fazla bilgi için bkz. [ErrorProvider Component](/dotnet/framework/winforms/controls/errorprovider-component-windows-forms).

Doğrulama <xref:System.Data.DataTable.RowChanging> olay sırasında da gerçekleştirilebilir.

## <a name="validate-data-during-row-changes"></a>Satır değişiklikleri sırasında verileri doğrulama
Doğrulamak istediğiniz her sütunun, uygulamanızın gereksinimlerini karşılayan veriler içerdiğini doğrulamak için kod yazabilirsiniz. Önerilen bir değer kabul edilemez ise, sütunu hata içerdiğini belirtecek şekilde ayarlayarak bunu yapın. Aşağıdaki örneklerde `Quantity` sütun 0 veya daha az olduğunda bir sütun hatası ayarlanır. Satır değişen olay işleyicileri aşağıdaki örneklere benzer olmalıdır.

### <a name="to-validate-data-when-a-row-changes-visual-basic"></a>Bir satır değiştiğinde verileri doğrulamak için (Visual Basic)

1. Kümenizde açın **veri kümesi Tasarımcısı**. Daha fazla bilgi için bkz [. İzlenecek yol: Veri Kümesi Tasarımcısı](walkthrough-creating-a-dataset-with-the-dataset-designer.md)veri kümesi oluşturma.

2. Doğrulamak istediğiniz tablonun başlık çubuğuna çift tıklayın. Bu eylem, <xref:System.Data.DataTable> veri kümesinin <xref:System.Data.DataTable.RowChanging> kısmi sınıf dosyasında öğesinin olay işleyicisini otomatik olarak oluşturur.

    > [!TIP]
    > Satır değiştiren olay işleyicisini oluşturmak için tablo adının sol tarafında çift tıklayın. Tablo adını çift tıklarsanız düzenleyebilirsiniz.

     [!code-vb[VbRaddataValidating#3](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_1.vb)]

### <a name="to-validate-data-when-a-row-changes-c"></a>Bir satır değiştiğinde verileri doğrulamak için (C#)

1. Kümenizde açın **veri kümesi Tasarımcısı**. Daha fazla bilgi için bkz [. İzlenecek yol: Veri Kümesi Tasarımcısı](walkthrough-creating-a-dataset-with-the-dataset-designer.md)veri kümesi oluşturma.

2. Doğrulamak istediğiniz tablonun başlık çubuğuna çift tıklayın. Bu eylem, <xref:System.Data.DataTable>için bir kısmi sınıf dosyası oluşturur.

    > [!NOTE]
    > **Veri kümesi Tasarımcısı** , <xref:System.Data.DataTable.RowChanging> olay için otomatik olarak bir olay işleyici oluşturmaz. <xref:System.Data.DataTable.RowChanging> Olayı işlemek için bir yöntem oluşturmanız ve olayı tablonun başlatma yönteminde bağlamak için kodu çalıştırmanız gerekir.

3. Aşağıdaki kodu kısmi sınıfa kopyalayın:

    ```csharp
    public override void EndInit()
    {
        base.EndInit();
        Order_DetailsRowChanging += TestRowChangeEvent;
    }

    public void TestRowChangeEvent(object sender, Order_DetailsRowChangeEvent e)
    {
        if ((short)e.Row.Quantity <= 0)
        {
            e.Row.SetColumnError("Quantity", "Quantity must be greater than 0");
        }
        else
        {
            e.Row.SetColumnError("Quantity", "");
        }
    }
    ```

## <a name="to-retrieve-changed-rows"></a>Değiştirilen satırları almak için
Bir veri tablosundaki her satır, <xref:System.Data.DataRow.RowState%2A> <xref:System.Data.DataRowState> Numaralandırmadaki değerleri kullanarak o satırın geçerli durumunu izlemeyi tutan bir özelliğe sahiptir. Bir `GetChanges` <xref:System.Data.DataSet> veya yönteminiçağırarakbirverikümesindenveyaveritablosundandeğiştirilensatırlarıdöndürebilirsiniz.<xref:System.Data.DataTable> Bir veri kümesinin `GetChanges` <xref:System.Data.DataSet.HasChanges%2A> yöntemini çağırarak, çağrılmadan önce değişikliklerin mevcut olduğunu doğrulayabilirsiniz.

> [!NOTE]
> Bir veri kümesine veya veri tablosuna değişiklikler yaptıktan sonra ( <xref:System.Data.DataSet.AcceptChanges%2A> yöntemini çağırarak) `GetChanges` , yöntem hiçbir veri döndürmez. Uygulamanızın değiştirilen satırları işlemesi gerekiyorsa, `AcceptChanges` metodu çağırmadan önce değişiklikleri işlemelidir.

Bir veri <xref:System.Data.DataSet.GetChanges%2A> kümesi veya veri tablosu yöntemini çağırmak, yalnızca değiştirilmiş kayıtları içeren yeni bir veri kümesi veya veri tablosu döndürür. Belirli kayıtları almak istiyorsanız — Örneğin, yalnızca yeni kayıtlar veya yalnızca değiştirilen kayıtlar —, <xref:System.Data.DataRowState> Numaralandırmadaki bir değeri, `GetChanges` yönteme parametre olarak geçirebilirsiniz.

Bir satırın farklı sürümlerine erişmek için numaralandırmayıkullanın(örneğin,işlemedenöncebirsatırdakiözgündeğerler).<xref:System.Data.DataRowVersion>

### <a name="to-get-all-changed-records-from-a-dataset"></a>Bir veri kümesinden tüm değiştirilen kayıtları almak için

- Bir veri kümesinin yöntemini çağırın. <xref:System.Data.DataSet.GetChanges%2A>

     Aşağıdaki örnek adlı `changedRecords` yeni bir veri kümesi oluşturur ve bunu adlı `dataSet1`başka bir veri kümesinden değiştirilen tüm kayıtlarla doldurur.

     [!code-csharp[VbRaddataEditing#14](../data-tools/codesnippet/CSharp/validate-data-in-datasets_2.cs)]
     [!code-vb[VbRaddataEditing#14](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_2.vb)]

### <a name="to-get-all-changed-records-from-a-data-table"></a>Bir veri tablosundan değiştirilen tüm kayıtları almak için

- <xref:System.Data.DataTable.GetChanges%2A> DataTable metodunu çağırın.

     Aşağıdaki örnek adlı `changedRecordsTable` yeni bir veri tablosu oluşturur ve adlı `dataTable1`başka bir veri tablosundan değiştirilen tüm kayıtlarla doldurur.

     [!code-csharp[VbRaddataEditing#15](../data-tools/codesnippet/CSharp/validate-data-in-datasets_3.cs)]
     [!code-vb[VbRaddataEditing#15](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_3.vb)]

### <a name="to-get-all-records-that-have-a-specific-row-state"></a>Belirli bir satır durumuna sahip tüm kayıtları almak için

- Bir veri kümesinin veya veri tablosunun <xref:System.Data.DataRowState> yönteminiçağırınvebirsabitlistesideğerinibağımsızdeğişkenolarakgeçirin.`GetChanges`

     Aşağıdaki örnekte, adlı `addedRecords` yeni bir veri kümesinin nasıl oluşturulacağı ve yalnızca `dataSet1` veri kümesine eklenen kayıtlarla doldurulması gösterilmektedir.

     [!code-csharp[VbRaddataEditing#16](../data-tools/codesnippet/CSharp/validate-data-in-datasets_4.cs)]
     [!code-vb[VbRaddataEditing#16](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_4.vb)]

     Aşağıdaki örnek, son olarak `Customers` tabloya eklenen tüm kayıtların nasıl geri alınacağını gösterir:

     [!code-csharp[VbRaddataEditing#17](../data-tools/codesnippet/CSharp/validate-data-in-datasets_5.cs)]
     [!code-vb[VbRaddataEditing#17](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_5.vb)]

## <a name="access-the-original-version-of-a-datarow"></a>DataRow 'ın orijinal sürümüne erişin
Veri satırlarında değişiklik yapıldığında veri kümesi, satırın hem özgün (<xref:System.Data.DataRowVersion.Original>) hem de yeni (<xref:System.Data.DataRowVersion.Current>) sürümlerini korur. Örneğin, `AcceptChanges` yöntemini çağırmadan önce, uygulamanız bir kaydın farklı sürümlerine erişebilir ( <xref:System.Data.DataRowVersion> numaralandırmada tanımlandığı gibi) ve değişiklikleri buna göre işleyebilir.

> [!NOTE]
> Bir satırın farklı sürümleri, `AcceptChanges` yalnızca düzenlendikten sonra ve yöntemi çağrılmadan önce bulunur. `AcceptChanges` Yöntem çağrıldıktan sonra, geçerli ve orijinal sürümler aynıdır.

<xref:System.Data.DataRowVersion> Değeri sütun dizini (veya bir dize olarak sütun adı) ile birlikte geçirmek, bu sütunun belirli satır sürümünden değeri döndürür. Değiştirilen sütun, <xref:System.Data.DataTable.ColumnChanging> ve <xref:System.Data.DataTable.ColumnChanged> olayları sırasında tanımlanır. Bu, doğrulama amacıyla farklı satır sürümlerini incelemek için iyi bir zamandır. Ancak, kısıtlamaları geçici olarak askıya aldıysanız, bu olaylar oluşturulmaz ve hangi sütunların değiştiğini programlı bir şekilde belirlemeniz gerekir. Bunu, <xref:System.Data.DataTable.Columns%2A> koleksiyonu kullanarak ve farklı <xref:System.Data.DataRowVersion> değerleri karşılaştırarak yapabilirsiniz.

### <a name="to-get-the-original-version-of-a-record"></a>Bir kaydın orijinal sürümünü almak için

- Döndürmek istediğiniz satırın değerini geçirerek <xref:System.Data.DataRowVersion> bir sütunun değerine erişin.

     Aşağıdaki örnek, içindeki <xref:System.Data.DataRowVersion> `CompanyName` bir alanın orijinal değerini almak için bir değerinin nasıl kullanılacağını gösterir: <xref:System.Data.DataRow>

     [!code-csharp[VbRaddataEditing#21](../data-tools/codesnippet/CSharp/validate-data-in-datasets_6.cs)]
     [!code-vb[VbRaddataEditing#21](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_6.vb)]

## <a name="access-the-current-version-of-a-datarow"></a>Bir DataRow 'ın geçerli sürümüne erişin

### <a name="to-get-the-current-version-of-a-record"></a>Bir kaydın geçerli sürümünü almak için

- Bir sütunun değerine erişin ve sonra dizine döndürmek istediğiniz bir satır sürümünü gösteren bir parametre ekleyin.

     Aşağıdaki örnek, içindeki <xref:System.Data.DataRowVersion> `CompanyName` bir alanın geçerli değerini almak için bir değerinin nasıl kullanılacağını gösterir: <xref:System.Data.DataRow>

     [!code-csharp[VbRaddataEditing#22](../data-tools/codesnippet/CSharp/validate-data-in-datasets_7.cs)]
     [!code-vb[VbRaddataEditing#22](../data-tools/codesnippet/VisualBasic/validate-data-in-datasets_7.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Visual Studio'daki veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md)
- [Nasıl yapılır: Windows Forms DataGridView Denetimindeki verileri doğrulama](/dotnet/framework/winforms/controls/how-to-validate-data-in-the-windows-forms-datagridview-control)
- [Nasıl yapılır: Windows Forms ErrorProvider Bileşeni ile form doğrulama için hata simgeleri görüntüle](/dotnet/framework/winforms/controls/display-error-icons-for-form-validation-with-wf-errorprovider)