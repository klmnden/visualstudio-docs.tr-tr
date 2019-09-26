---
title: ListObject denetimi
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VST.Toolbox.List
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- lists, events
- ListObject control
- ListObject control, events
- ListObject control, data binding
- ListObject control, improving performance when bound to data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 3b5286a4bddff2b529abd0a565bb4dbeef7ffaf3
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71251862"
---
# <a name="listobject-control"></a>ListObject denetimi
  <xref:Microsoft.Office.Tools.Excel.ListObject> Denetim, olayları ortaya çıkaran ve verilere bağlanabilen bir listesidir. Çalışma sayfasına bir liste eklediğinizde, Visual Studio Microsoft Office Excel nesne modelinde geçiş <xref:Microsoft.Office.Tools.Excel.ListObject> yapmak zorunda kalmadan doğrudan programlama yapabileceğiniz bir denetim oluşturur.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="create-the-control"></a>Denetim oluşturma
 Belge düzeyi projelerinde, tasarım zamanında veya çalışma zamanında <xref:Microsoft.Office.Tools.Excel.ListObject> çalışma sayfasına denetimler ekleyebilirsiniz. VSTO eklenti projelerinde, çalışma sayfalarına yalnızca çalışma zamanında denetim <xref:Microsoft.Office.Tools.Excel.ListObject> ekleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Çalışma sayfalarına](../vsto/how-to-add-listobject-controls-to-worksheets.md)ListObject denetimleri ekleyin.

> [!NOTE]
> Varsayılan olarak, çalışma sayfası kapatıldığında dinamik olarak oluşturulan liste nesneleri çalışma sayfasında konak denetimleri olarak kalıcı olmaz. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

## <a name="bind-data-to-the-control"></a>Verileri denetime bağlama
 Bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetim basit ve karmaşık veri bağlamayı destekler. Denetim, <xref:Microsoft.Office.Tools.Excel.ListObject.DataSource%2A> tasarım zamanında <xref:Microsoft.Office.Tools.Excel.ListObject.DataMember%2A> veçalışmazamanındayöntemikullanılarakbirverikaynağınabağlanabilir.<xref:Microsoft.Office.Tools.Excel.ListObject.SetDataBinding%2A> <xref:Microsoft.Office.Tools.Excel.ListObject>

> [!NOTE]
> , Verileri değiştiğinde olayları başlatan bir <xref:System.Data.DataTable>veri kaynağına bağlandığında otomatik olarak güncelleştirilir. <xref:Microsoft.Office.Tools.Excel.ListObject> Verileri değiştiğinde <xref:Microsoft.Office.Tools.Excel.ListObject> olayları yükseltmez bir veri kaynağına bağlarsanız, öğesini güncelleştirmek için <xref:Microsoft.Office.Tools.Excel.ListObject.RefreshDataRow%2A> <xref:Microsoft.Office.Tools.Excel.ListObject>veya <xref:Microsoft.Office.Tools.Excel.ListObject.RefreshDataRows%2A> metodunu çağırmanız gerekir.

 Yinelenen bir şema öğesini <xref:Microsoft.Office.Tools.Excel.ListObject> ilgili hücreyle eşleyerek çalışma sayfası hücresine bir eklediğinizde, Visual Studio otomatik olarak öğesini oluşturulan veri kümesiyle <xref:Microsoft.Office.Tools.Excel.ListObject> eşler. <xref:Microsoft.Office.Tools.Excel.ListObject> Ancak, otomatik olarak verilere bağlanmaz. Tasarım zamanında veya belge düzeyindeki bir projede <xref:Microsoft.Office.Tools.Excel.ListObject> çalışma zamanında veri kümesine bağlamak için gerekli adımları uygulayabilirsiniz. Bir VSTO eklentisinde çalışma zamanında <xref:Microsoft.Office.Tools.Excel.ListObject> veri kümesine programlı bir şekilde bağlanabilirsiniz.

 Veriler öğesinden <xref:Microsoft.Office.Tools.Excel.ListObject>ayrı olduğundan, doğrudan <xref:Microsoft.Office.Tools.Excel.ListObject>aracılığıyla değil, bağlantılı veri kümesi aracılığıyla veri eklemeli ve çıkarmanız gerekir. Bağlantılı veri kümesindeki veriler herhangi bir mekanizmaya göre güncelleştirilirse, <xref:Microsoft.Office.Tools.Excel.ListObject> denetim otomatik olarak değişiklikleri yansıtır. Daha fazla bilgi için bkz. [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md).

 Bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetimi hızlı bir şekilde bir veri kaynağına <xref:Microsoft.Office.Tools.Excel.ListObject> bağlayarak doldurabilirsiniz. Verileri veriye göre düzenlerseniz <xref:Microsoft.Office.Tools.Excel.ListObject>, değişiklikler otomatik olarak veri kaynağında de yapılır. ' I doldurup <xref:Microsoft.Office.Tools.Excel.ListObject> veri kaynağını değiştirmeden kullanıcının <xref:Microsoft.Office.Tools.Excel.ListObject> içindeki verileri değiştirmesini etkinleştirmek istiyorsanız, veri kaynağından ayırmak <xref:Microsoft.Office.Tools.Excel.ListObject> için <xref:Microsoft.Office.Tools.Excel.ListObject.Disconnect%2A> yöntemini kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: ListObject denetimlerini verilerle](../vsto/how-to-fill-listobject-controls-with-data.md)doldur.

> [!NOTE]
> Çakışan <xref:Microsoft.Office.Tools.Excel.ListObject> denetimlerde veri bağlama desteklenmiyor.

### <a name="improve-performance-in-listobject-controls"></a>ListObject denetimlerinde performansı geliştirme
 Bir XML dosyasını bir veri bağlama <xref:Microsoft.Office.Tools.Excel.ListObject> denetimine okumak, önce denetimi bağladığınızda daha yavaş olacak şekilde, <xref:System.Data.DataSet.ReadXml%2A> sonra da veri kümesini dolduracak şekilde daha yavaş olur. Performansı artırmak için, denetimi <xref:System.Data.DataSet.ReadXml%2A> paylaşmadan önce çağırın.

### <a name="disconnect-listobject-controls-from-the-data-source"></a>Veri kaynağından ListObject denetimlerinin bağlantısını kesme
 Bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetimi verileri bir veri kaynağına bağlayarak doldurduktan sonra, liste nesnesindeki verilerde yapılan değişikliklerin veri kaynağını etkilememesi için bağlantısını kesebilirsiniz. Daha fazla bilgi için [nasıl yapılır: ListObject denetimlerini verilerle](../vsto/how-to-fill-listobject-controls-with-data.md)doldur.

### <a name="restore-column-and-row-order"></a>Sütun ve satır sırasını geri yükleme
 Tasarım zamanında bir belgeye eklenen bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetime veri bağladığınızda, Visual Studio çalışma kitabının kaydedildiği her seferinde sütun ve satır sırasını izler. Bir kullanıcı çalışma zamanında <xref:Microsoft.Office.Tools.Excel.ListObject> sütunları veya satırları taşısa, çalışma kitabının bir sonraki açılışında yeni sıra korunur <xref:Microsoft.Office.Tools.Excel.ListObject> ve denetim veri kaynağına yeniden bağlanır.

 ' I özgün sütununa ve satır <xref:Microsoft.Office.Tools.Excel.ListObject> sırasına geri yüklemek istiyorsanız, <xref:Microsoft.Office.Tools.Excel.ListObject.ResetPersistedBindingInformation%2A> yöntemini çağırabilirsiniz. Bu yöntem, belirtilen <xref:Microsoft.Office.Tools.Excel.ListObject>sütun ve satır sırasıyla ilgili özel belge özelliklerini kaldırır. Öğesinin sütun ve satır sırasını <xref:Microsoft.Office.Tools.Excel.Workbook.Shutdown> korumak istemiyorsanız, <xref:Microsoft.Office.Tools.Excel.ListObject>çalışma kitabının olayından bu yöntemi çağırın.

## <a name="format"></a>Biçimi
 Bir <xref:Microsoft.Office.Interop.Excel.ListObject> <xref:Microsoft.Office.Tools.Excel.ListObject> denetime uygulanabilen biçimlendirme, bir denetime uygulanabilir. Buna kenarlık, yazı tipi, sayı biçimi ve stil dahildir. Son kullanıcılar, verileri bir veri ile bağlantılı <xref:Microsoft.Office.Tools.Excel.ListObject>olarak yeniden düzenleyebilir ve bu değişiklikler belge ile birlikte kalıcı hale getirilir, <xref:Microsoft.Office.Tools.Excel.ListObject> ancak belgeye tasarım zamanında eklenmiş olur. Belge bir dahaki sefer açıldığında, liste nesnesi aynı veri kaynağına bağlanır, ancak sütun sırası kullanıcıların değişikliklerini yansıtır.

## <a name="add-and-remove-columns-at-run-time"></a>Çalışma zamanında sütun ekleme ve kaldırma
 Çalışma zamanında veriye <xref:Microsoft.Office.Tools.Excel.ListObject> dayalı bir denetimde sütunları el ile ekleyemez veya kaldıramazsınız. Son Kullanıcı bir sütunu silmeye çalışırsa, hemen geri yüklenir ve eklenen sütunlar kaldırılır. Bu nedenle, kullanıcılara, verilere bağlı olan bir üzerinde bu işlemleri gerçekleştiremediğini açıklayan bir <xref:Microsoft.Office.Tools.Excel.ListObject> kod yazmak önemlidir. Visual Studio, veri bağlama ile <xref:Microsoft.Office.Tools.Excel.ListObject> ilgili çeşitli olaylar sağlar. Örneğin, kullanıcıyı silmeye çalıştıkları verilerin silinemediğini ve geri yüklendiğini uyarmak için <xref:Microsoft.Office.Tools.Excel.ListObject.OriginalDataRestored> olayını kullanabilirsiniz.

## <a name="add-and-remove-rows-at-run-time"></a>Çalışma zamanında satır ekleme ve kaldırma
 Veri kaynağı yeni satırların eklenmesine izin verdiğinden ve salt okunmadığından, <xref:Microsoft.Office.Tools.Excel.ListObject> veri kaynağı denetimine satırları el ile ekleyebilir ve kaldırabilirsiniz. Verileri doğrulamak <xref:Microsoft.Office.Tools.Excel.ListObject.BeforeAddDataBoundRow> için gibi olaylara karşı kod yazabilirsiniz. Daha fazla bilgi için [nasıl yapılır: ListObject denetimine](../vsto/how-to-validate-data-when-a-new-row-is-added-to-a-listobject-control.md)yeni bir satır eklendiğinde verileri doğrulayın.

 Bazen liste nesnesinin veri kaynağıyla ilişkisi rutin hatalara neden olur. Örneğin, içinde <xref:Microsoft.Office.Tools.Excel.ListObject>görünmesini istediğiniz sütunları eşleyebilirsiniz. bu nedenle, null değerleri kabul edemeyecek bir alan gibi kısıtlamalar bulunan sütunları atlarsanız, her satır oluşturulduğunda hatalar oluşur. <xref:Microsoft.Office.Tools.Excel.ListObject.ErrorAddDataBoundRow> Olay için bir olay işleyicisine eksik değerler eklemek için kod yazabilirsiniz.

## <a name="rename-listobject-controls-in-excel"></a>Excel 'de ListObject denetimlerini yeniden adlandırma
 Excel, **Tasarım** sekmesini kullanarak kullanıcıların çalışma zamanında Excel tablolarının adını değiştirmesine olanak sağlar. Ancak, <xref:Microsoft.Office.Tools.Excel.ListObject> denetim bu özelliği desteklemez. Bir Kullanıcı öğesine <xref:Microsoft.Office.Tools.Excel.ListObject>karşılık gelen bir Excel tablosunu yeniden adlandırmaya çalışırsa, çalışma kitabı kaydedildiğinde Excel tablosunun adı otomatik olarak özgün ada döndürülür.

## <a name="events"></a>Olaylar
 <xref:Microsoft.Office.Tools.Excel.ListObject> Denetim için aşağıdaki olaylar mevcuttur:

- <xref:Microsoft.Office.Tools.Excel.ListObject.BeforeAddDataBoundRow>

- <xref:Microsoft.Office.Tools.Excel.ListObject.BeforeDoubleClick>

- <xref:Microsoft.Office.Tools.Excel.ListObject.BeforeRightClick>

- <xref:Microsoft.Office.Tools.Excel.ListObject.BindingContextChanged>

- <xref:Microsoft.Office.Tools.Excel.ListObject.Change>

- <xref:Microsoft.Office.Tools.Excel.ListObject.DataBindingFailure>

- <xref:Microsoft.Office.Tools.Excel.ListObject.DataMemberChanged>

- <xref:Microsoft.Office.Tools.Excel.ListObject.DataSourceChanged>

- <xref:Microsoft.Office.Tools.Excel.ListObject.Deselected>

- <xref:Microsoft.Office.Tools.Excel.ListObject.ErrorAddDataBoundRow>

- <xref:Microsoft.Office.Tools.Excel.ListObject.OriginalDataRestored>

- <xref:Microsoft.Office.Tools.Excel.ListObject.Selected>

- <xref:Microsoft.Office.Tools.Excel.ListObject.SelectedIndexChanged>

- <xref:Microsoft.Office.Tools.Excel.ListObject.SelectionChange>

## <a name="see-also"></a>Ayrıca bkz.
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Nasıl yapılır: Çalışma sayfalarına ListObject denetimleri ekleme](../vsto/how-to-add-listobject-controls-to-worksheets.md)
- [Nasıl yapılır: ListObject denetimlerini yeniden boyutlandır](../vsto/how-to-resize-listobject-controls.md)
- [Nasıl yapılır: ListObject denetimine yeni bir satır eklendiğinde verileri doğrulama](../vsto/how-to-validate-data-when-a-new-row-is-added-to-a-listobject-control.md)
- [Nasıl yapılır: ListObject sütunlarını verilerle eşleme](../vsto/how-to-map-listobject-columns-to-data.md)
- [Nasıl yapılır: ListObject denetimlerini verilerle Doldur](../vsto/how-to-fill-listobject-controls-with-data.md)
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Nasıl yapılır: Çalışma sayfalarını bir veritabanındaki verilerle doldurma](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)
- [Konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
