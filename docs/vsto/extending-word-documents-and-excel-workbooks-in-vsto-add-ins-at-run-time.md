---
title: Çalışma zamanında VSTO Eklentilerindeki Word belgelerini & Excel çalışma kitaplarını genişletme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- GetVstoObject method
- application-level add-ins [Office development in Visual Studio], adding controls to documents
- host items [Office development in Visual Studio], creating at run time in add-ins
- application-level add-ins [Office development in Visual Studio], extending Word documents
- application-level add-ins [Office development in Visual Studio], extending Excel workbooks
- controls [Office development in Visual Studio], adding at run time
- HasVstoObject method
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a80fc10690691e8bd923f9c98270b162e7063ffb
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253661"
---
# <a name="extend-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time"></a>VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme
  Word belgelerini ve Excel çalışma kitaplarını aşağıdaki yollarla özelleştirmek için bir VSTO eklentisi kullanabilirsiniz:

- Yönetilen denetimleri herhangi bir açık belge veya çalışma sayfasına ekleyin.

- Excel çalışma sayfasındaki var olan bir liste nesnesini, olayları ortaya çıkaran <xref:Microsoft.Office.Tools.Excel.ListObject> ve Windows Forms veri bağlama modeli kullanılarak verilere bağlanabilen bir genişletmeye dönüştürün.

- Belirli belgeler, çalışma kitapları ve çalışma sayfaları için Word ve Excel tarafından kullanıma sunulan uygulama düzeyi olaylara erişin.

  Bu işlevi kullanmak için, çalışma zamanında belgeyi veya çalışma kitabını genişleten bir nesne oluşturursunuz.

  **Uygulama hedefi:** Bu makaledeki bilgiler, aşağıdaki uygulamalar için VSTO eklentisi projelerine yöneliktir: Excel ve Word. Daha fazla bilgi için bkz. [Office uygulaması ve proje türü tarafından kullanılabilen özellikler](../vsto/features-available-by-office-application-and-project-type.md).

## <a name="generate-extended-objects-in-vsto-add-ins"></a>VSTO eklentilerinde Genişletilmiş nesneler oluşturma
 *Genişletilmiş nesneler* , Word veya Excel nesne modelleriyle ( *yerel Office nesneleri*olarak adlandırılır) yerel olarak var olan nesnelere işlevsellik ekleyen Office çalışma zamanı için Visual Studio Araçları tarafından verilen türlerin örnekleridir. Bir Word veya Excel nesnesi için genişletilmiş bir nesne oluşturmak için `GetVstoObject` yöntemini kullanın. Belirtilen bir kelime veya Excel nesnesi `GetVstoObject` için yöntemi ilk kez çağırdığınızda, belirtilen nesneyi genişleten yeni bir nesne döndürür. Yöntemini her çağırdığınızda ve aynı Word ya da Excel nesnesini belirttiğinizde, aynı genişletilmiş nesneyi döndürür.

 Genişletilmiş nesnenin türü, yerel Office nesnesinin türüyle aynı ada sahiptir, ancak tür <xref:Microsoft.Office.Tools.Excel> veya <xref:Microsoft.Office.Tools.Word> ad alanında tanımlanır. Örneğin, bir `GetVstoObject` <xref:Microsoft.Office.Interop.Word.Document> nesneyi genişletmek için yöntemini çağırırsanız, yöntemi bir <xref:Microsoft.Office.Tools.Word.Document> nesnesi döndürür.

 Yöntemler `GetVstoObject` , birincil olarak VSTO eklenti projelerinde kullanılmak üzere tasarlanmıştır. Bu yöntemleri belge düzeyi projelerde da kullanabilirsiniz, ancak bunları farklı şekilde ve daha az kullanımlar vardır.

 Genişletilmiş bir nesnenin belirli bir yerel Office nesnesi için önceden oluşturulup oluşturulmayacağını anlamak için `HasVstoObject` yöntemini kullanın. Daha fazla bilgi için bkz. [bir Office nesnesinin uzatılıp genişletilmediğini belirleme](#HasVstoObject).

### <a name="generate-host-items"></a>Konak öğeleri Oluştur
 Belge düzeyi nesnesini ( `GetVstoObject` <xref:Microsoft.Office.Interop.Excel.Workbook>Yani,, veya <xref:Microsoft.Office.Interop.Word.Document>) genişletmek için kullandığınızda, döndürülen nesneye bir konak öğesi denir. <xref:Microsoft.Office.Interop.Excel.Worksheet> Konak öğesi, diğer Genişletilmiş nesneler ve denetimler de dahil olmak üzere diğer nesneleri içerebilen bir türdür. Word veya Excel birincil birlikte çalışma derlemesinde karşılık gelen türe benzer, ancak ek özelliklere sahiptir. Konak öğeleri hakkında daha fazla bilgi için bkz. [konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md).

 Bir konak öğesi oluşturduktan sonra, belgeye, çalışma kitabına veya çalışma sayfasına yönetilen denetimler eklemek için onu kullanabilirsiniz. Daha fazla bilgi için bkz. [belgelere ve çalışma sayfalarına yönetilen denetimler ekleme](#AddControls).

#### <a name="to-generate-a-host-item-for-a-word-document"></a>Bir Word belgesi için bir konak öğesi oluşturmak için

- Aşağıdaki kod örneğinde, etkin belge için bir konak öğesinin nasıl oluşturulacağı gösterilmektedir.

     [!code-vb[Trin_WordAddInDynamicControls#8](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#8)]
     [!code-csharp[Trin_WordAddInDynamicControls#8](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#8)]

#### <a name="to-generate-a-host-item-for-an-excel-workbook"></a>Excel çalışma kitabı için bir konak öğesi oluşturmak için

- Aşağıdaki kod örneğinde, etkin çalışma kitabı için bir konak öğesinin nasıl oluşturulacağı gösterilmektedir.

     [!code-vb[Trin_ExcelAddInDynamicControls#2](../vsto/codesnippet/VisualBasic/trin_exceladdindynamiccontrols4/ThisAddIn.vb#2)]
     [!code-csharp[Trin_ExcelAddInDynamicControls#2](../vsto/codesnippet/CSharp/trin_exceladdindynamiccontrols4/ThisAddIn.cs#2)]

#### <a name="to-generate-a-host-item-for-an-excel-worksheet"></a>Excel çalışma sayfası için bir konak öğesi oluşturmak için

- Aşağıdaki kod örneğinde, bir projedeki etkin çalışma sayfası için bir konak öğesinin nasıl oluşturulacağı gösterilmektedir.

     [!code-vb[Trin_ExcelAddInDynamicControls#1](../vsto/codesnippet/VisualBasic/trin_exceladdindynamiccontrols4/ThisAddIn.vb#1)]
     [!code-csharp[Trin_ExcelAddInDynamicControls#1](../vsto/codesnippet/CSharp/trin_exceladdindynamiccontrols4/ThisAddIn.cs#1)]

### <a name="generate-listobject-host-controls"></a>ListObject konak denetimleri oluştur
 Öğesini genişletmek için `GetVstoObject` yöntemini kullandığınızda yöntemi bir <xref:Microsoft.Office.Tools.Excel.ListObject>döndürür. <xref:Microsoft.Office.Interop.Excel.ListObject> , <xref:Microsoft.Office.Tools.Excel.ListObject> Orijinalin <xref:Microsoft.Office.Interop.Excel.ListObject>tüm özelliklerine sahiptir. Ayrıca, ek işlevlere sahiptir ve Windows Forms veri bağlama modeli kullanılarak verilere bağlanabilir. Daha fazla bilgi için bkz. [ListObject denetimi](../vsto/listobject-control.md).

#### <a name="to-generate-a-host-control-for-a-listobject"></a>Bir ListObject için konak denetimi oluşturmak için

- Aşağıdaki kod örneği, bir projedeki etkin çalışma sayfasında <xref:Microsoft.Office.Tools.Excel.ListObject> ilki <xref:Microsoft.Office.Interop.Excel.ListObject> için nasıl oluşturulacağını gösterir.

     [!code-vb[Trin_ExcelAddInDynamicControls#3](../vsto/codesnippet/VisualBasic/trin_exceladdindynamiccontrols4/ThisAddIn.vb#3)]
     [!code-csharp[Trin_ExcelAddInDynamicControls#3](../vsto/codesnippet/CSharp/trin_exceladdindynamiccontrols4/ThisAddIn.cs#3)]

### <a name="AddControls"></a>Belgelere ve çalışma sayfalarına yönetilen denetimler ekleme
 <xref:Microsoft.Office.Tools.Word.Document> Ya<xref:Microsoft.Office.Tools.Excel.Worksheet>da oluşturduktan sonra, belgeye veya çalışma sayfasına bu genişletilmiş nesnelerin temsil ettiği denetimleri ekleyebilirsiniz. Denetim eklemek için, `Controls` <xref:Microsoft.Office.Tools.Word.Document> veya <xref:Microsoft.Office.Tools.Excel.Worksheet>özelliğini kullanın. Daha fazla bilgi için bkz. [çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md).

 Windows Forms denetimleri veya *konak denetimleri*ekleyebilirsiniz. Konak denetimi, [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] Word veya Excel birincil birlikte çalışma derlemesinde karşılık gelen bir denetimi sarmalayan tarafından sağlanmış bir denetimdir. Ana bilgisayar denetimi, temel alınan yerel Office nesnesinin tüm davranışlarını gösterir. Ayrıca, olaylar oluşturur ve Windows Forms veri bağlama modeli kullanılarak verilere bağlanabilir. Daha fazla bilgi için bkz. [konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md).

> [!NOTE]
> VSTO eklentisini kullanarak bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> çalışma sayfasına veya bir belgeye <xref:Microsoft.Office.Tools.Word.XMLNodes> bir <xref:Microsoft.Office.Tools.Word.XMLNode> denetim ekleyemez. Bu konak denetimleri program aracılığıyla eklenemez. Daha fazla bilgi için bkz. [konak öğelerinin ve konak denetimlerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).

### <a name="persist-and-remove-controls"></a>Kalıcı ve kaldırma denetimleri
 Yönetilen denetimleri bir belgeye veya çalışma sayfasına eklediğinizde, belge kaydedilip kapatıldığında denetimler kalıcı olmaz. Tüm konak denetimleri, yalnızca temeldeki yerel Office nesnelerinin arkasında bırakılması için kaldırılır. Örneğin, <xref:Microsoft.Office.Tools.Excel.ListObject> bir <xref:Microsoft.Office.Interop.Excel.ListObject>olur. Tüm Windows Forms denetimleri de kaldırılır, ancak denetimlerin ActiveX sarmalayıcıları belgede geride bırakılır. Denetimleri temizlemek için veya belgeyi bir dahaki sefer açıldığında denetimleri yeniden oluşturmak için VSTO eklentiye kod dahil etmeniz gerekir. Daha fazla bilgi için bkz. [Dinamik denetimleri Office belgelerinde kalıcı hale](../vsto/persisting-dynamic-controls-in-office-documents.md)getirme.

## <a name="access-application-level-events-on-documents-and-workbooks"></a>Belgeler ve çalışma kitaplarında uygulama düzeyi olaylara erişme
 Yerel Word ve Excel nesne modelleriyle bazı belge, çalışma kitabı ve çalışma sayfası olayları yalnızca uygulama düzeyinde oluşturulur. Örneğin, <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentBeforeSave> bir belge Word 'de açıldığında olay tetiklenir, ancak bu olay sınıf yerine <xref:Microsoft.Office.Interop.Word.Application> <xref:Microsoft.Office.Interop.Word.Document> sınıfında tanımlanır.

 VSTO eklentiinizdeki yalnızca yerel Office nesnelerini kullandığınızda, bu uygulama düzeyindeki olayları uygulamanız ve sonra olayı oluşturan belgenin özelleştirildiği bir belge olup olmadığını anlamak için ek kod yazmanız gerekir. Konak öğeleri, bu olayları belge düzeyinde sağlar, böylece belirli bir belge için olayları işlemek daha kolay olur. Bir konak öğesi oluşturabilir ve ardından bu konak öğesi için olayı işleyebilirsiniz.

### <a name="example-that-uses-native-word-objects"></a>Yerel Word nesneleri kullanan örnek
 Aşağıdaki kod örneği, Word belgeleri için uygulama düzeyindeki bir olayın nasıl işleneceğini gösterir. Yöntemi yeni bir belge oluşturur ve sonra bu belgenin kaydedilmesini engelleyen <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentBeforeSave> bir olay işleyicisini tanımlar. `CreateDocument` Olay, <xref:Microsoft.Office.Interop.Word.Application> nesne için oluşturulan uygulama düzeyi olayıdır ve olay işleyicisi, kaydedilen belgeyi `document1` temsil edip etmediğini tespit etmek için `Doc` parametresini `document1` nesnesiyle karşılaştırmalıdır.

 [!code-vb[Trin_WordAddInDynamicControls #12](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#12)]
 [!code-csharp[Trin_WordAddInDynamicControls#12](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#12)]

### <a name="examples-that-use-a-host-item"></a>Konak öğesi kullanan örnekler
 Aşağıdaki kod örnekleri, bir <xref:Microsoft.Office.Tools.Word.Document.BeforeSave> <xref:Microsoft.Office.Tools.Word.Document> konak öğesinin olayını işleyerek bu işlemi basitleştirir. Bu örneklerdeki <xref:Microsoft.Office.Tools.Word.Document> `document2` yöntemi nesnesini genişleten bir oluşturur ve sonra belgenin kaydedilmesini önleyen bir <xref:Microsoft.Office.Tools.Word.Document.BeforeSave> olay işleyicisi tanımlar. `CreateDocument2` Olay işleyicisi yalnızca `document2` kaydedildiğinde çağrılır ve hangi belgenin kaydedildiğini doğrulamak için ek bir iş yapmadan Kaydet eylemini iptal edebilir.

 Aşağıdaki kod örneği bu görevi gösterir.

 [!code-vb[Trin_WordAddInDynamicControls #13](../vsto/codesnippet/VisualBasic/trin_wordaddindynamiccontrols/ThisAddIn.vb#13)]
 [!code-csharp[Trin_WordAddInDynamicControls#13](../vsto/codesnippet/CSharp/Trin_WordAddInDynamicControls/ThisAddIn.cs#13)]

## <a name="HasVstoObject"></a>Bir Office nesnesinin uzatılıp genişletilmediğini belirleme
 Genişletilmiş bir nesnenin belirli bir yerel Office nesnesi için önceden oluşturulup oluşturulmayacağını anlamak için `HasVstoObject` yöntemini kullanın. Bu yöntem, genişletilmiş bir nesne zaten oluşturulmuşsa **true** değerini döndürür.

 `Globals.Factory.HasVstoMethod` Yöntemini kullanın. Genişletilmiş bir <xref:Microsoft.Office.Interop.Word.Document> nesne için test etmek istediğiniz veya <xref:Microsoft.Office.Interop.Excel.Worksheet>gibi yerel Word veya Excel nesnesini geçirin.

 Yöntemi `HasVstoObject` , yalnızca belirtilen bir Office nesnesi genişletilmiş bir nesne olduğunda kodu çalıştırmak istediğinizde yararlıdır. Örneğin, bir belgeyi kaydedilmeden önce yönetilen denetimleri kaldırmak için <xref:Microsoft.Office.Interop.Word.ApplicationEvents4_Event.DocumentBeforeSave> olayını işleyen bir Word VSTO eklentisi varsa, belgenin genişletilip genişletilmediğini anlamak için `HasVstoObject` yöntemini kullanın. Belge genişletilmemişse, yönetilen denetimleri olamaz ve olay işleyicisi belgedeki denetimleri temizlemeye çalışmak zorunda kalmadan dönebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Office geliştirme örnekleri ve izlenecek yollar](../vsto/office-development-samples-and-walkthroughs.md)
