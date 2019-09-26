---
title: Çalışma zamanında form bölgesine erişme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Inspectors [Office development in Visual Studio]
- Explorers [Office development in Visual Studio]
- form regions [Office development in Visual Studio], accessing at run time
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5dd8818b57a1aa33b70254303150d8f00e36cc02
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255793"
---
# <a name="access-a-form-region-at-run-time"></a>Çalışma zamanında form bölgesine erişme

|Uygulandığı öğe:|
|----------------|
|Bu konunun içerdiği bilgiler, yalnızca Microsoft Office'in aşağıdaki proje türleri ve sürümleri için geçerlidir. Daha fazla bilgi için bkz. [Office uygulaması ve proje türü tarafından kullanılabilen özellikler](../vsto/features-available-by-office-application-and-project-type.md).<br /><br /> **Proje türü**<br /><br /> -VSTO eklenti projeleri<br /><br /> **Microsoft Office sürümü**<br /><br /> -   [!INCLUDE[Outlook_14_short](../vsto/includes/outlook-14-short-md.md)]|

 Form bölgelerine Outlook projenizin içinden herhangi bir yerden erişmek için sınıfınıkullanın.`Globals` `Globals` Sınıfı hakkında daha fazla bilgi için bkz. [Office Projelerindeki Nesnelere Genel erişim](../vsto/global-access-to-objects-in-office-projects.md).

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="access-form-regions-that-appear-in-a-specific-outlook-inspector-window"></a>Belirli bir Outlook Inspector penceresinde görünen erişim formu bölgeleri
 Belirli bir Outlook denetçisinde görünen tüm form bölgelerine erişmek için, `FormRegions` `Globals` sınıfının özelliğini çağırın ve denetçisi temsil eden bir <xref:Microsoft.Office.Interop.Outlook.Inspector> nesneyi geçirin.

 Aşağıdaki örnek, şu anda odağa sahip olan Inspector 'da görünen form bölgelerinin koleksiyonunu alır. Bu örnek daha sonra adlı `formRegion1` koleksiyondaki bir form bölgesine erişir ve metin kutusunda görüntülenen metni olarak `Hello World`ayarlar.

 [!code-vb[Trin_Outlook_FR_Access#2](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Access_O12/ThisAddIn.vb#2)]
 [!code-csharp[Trin_Outlook_FR_Access#2](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Access_O12/ThisAddIn.cs#2)]

## <a name="access-form-regions-that-appear-in-a-specific-outlook-explorer-window"></a>Belirli bir Outlook Explorer penceresinde görünen erişim formu bölgeleri
 Belirli bir Outlook Explorer 'da görünen tüm form bölgelerine erişmek için, `FormRegions` `Globals` sınıfının özelliğini çağırın ve Gezgini temsil eden bir <xref:Microsoft.Office.Interop.Outlook.Explorer> nesneyi geçirin.

 Aşağıdaki örnek, Gezgin 'de Şu anda odaklanmış olan form bölgelerinin koleksiyonunu alır. Bu örnek daha sonra adlı `formRegion1` koleksiyondaki bir form bölgesine erişir ve metin kutusunda görüntülenen metni olarak `Hello World`ayarlar.

 [!code-vb[Trin_Outlook_FR_Access#3](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Access_O12/ThisAddIn.vb#3)]
 [!code-csharp[Trin_Outlook_FR_Access#3](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Access_O12/ThisAddIn.cs#3)]

## <a name="access-all-form-regions"></a>Tüm form bölgelerine erişin
 Tüm araştırıcılar ve tüm Denetçilerde görünen tüm form bölgelerine erişmek için, `FormRegions` `Globals` sınıfının özelliğini çağırın.

 Aşağıdaki örnek, tüm araştırıcılar ve tüm Denetçilerde görünen form bölgelerinin koleksiyonunu alır. Bu örnekte, adlı `formRegion1` bir form bölgesine erişilir ve metin kutusunda görüntülenen metin olarak `Hello World`ayarlanır.

 [!code-vb[Trin_Outlook_FR_Access#1](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Access_O12/ThisAddIn.vb#1)]
 [!code-csharp[Trin_Outlook_FR_Access#1](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Access_O12/ThisAddIn.cs#1)]

## <a name="access-controls-on-a-form-region"></a>Form bölgesindeki erişim denetimleri
 `Globals` Sınıfını kullanarak form bölgesindeki denetimlere erişmek için, denetimleri form bölgesi kod dosyası dışındaki kod için erişilebilir yapmanız gerekir.

### <a name="form-regions-designed-in-the-form-region-designer"></a>Form bölgesi tasarımcısında tasarlanan form bölgeleri
 İçin C#, erişmek istediğiniz her bir denetimin değiştiricisini değiştirin. Bunu yapmak için, form bölgesi tasarımcısında her bir denetimi seçin ve **Özellikler** penceresinde **değiştiriciler** özelliğini **iç** veya **ortak** olarak değiştirin. Örneğin, öğesinin `textBox1` **değiştirici** özelliğini **iç**olarak değiştirirseniz yazarak `textBox1` `Globals.FormRegions.FormRegion1.textBox1`erişebilirsiniz.

 Visual Basic için değiştiriciyi değiştirmenize gerek yoktur.

### <a name="imported-form-regions"></a>İçeri aktarılan form bölgeleri
 Outlook 'ta tasarlanan bir form bölgesini içeri aktardığınızda, form bölgesindeki her bir denetimin erişim değiştiricisi Private olur. İçe aktarılan bir form bölgesini değiştirmek için form bölgesi tasarımcısını kullanamadığı için, **Özellikler** penceresinde bir denetimin değiştiricisini değiştirmenin bir yolu yoktur.

 Form bölgesi kod dosyası dışından bir denetime erişimi etkinleştirmek için, bu denetimi döndürmek üzere form bölgesi kod dosyasında bir özellik oluşturun.

 İçinde C#özellikler oluşturma hakkında daha fazla bilgi için bkz [. nasıl yapılır: &#40;Okuma yazma özellikleri&#35; C programlama kılavuzunu&#41;](/dotnet/csharp/programming-guide/classes-and-structs/how-to-declare-and-use-read-write-properties)bildirin ve kullanın.

 Visual Basic özellikler oluşturma hakkında daha fazla bilgi için bkz [. nasıl yapılır: Özellik oluşturun (Visual Basic)](/dotnet/visual-basic/programming-guide/language-features/procedures/how-to-create-a-property).

## <a name="see-also"></a>Ayrıca bkz.
- [Outlook form bölgeleri oluşturma yönergeleri](../vsto/guidelines-for-creating-outlook-form-regions.md)
- [İzlenecek yol: Outlook form bölgesi tasarlama](../vsto/walkthrough-designing-an-outlook-form-region.md)
- [Nasıl yapılır: Outlook eklenti projesine form bölgesi ekleme](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md)
- [Outlook form bölgelerindeki özel eylemler](../vsto/custom-actions-in-outlook-form-regions.md)
- [Form bölgesini Outlook ileti sınıfıyla ilişkilendirme](../vsto/associating-a-form-region-with-an-outlook-message-class.md)
- [İzlenecek yol: Outlook 'ta tasarlanan form bölgesini içeri aktarma](../vsto/walkthrough-importing-a-form-region-that-is-designed-in-outlook.md)
- [Nasıl yapılır: Outlook 'un form bölgesi görüntülemesini engelle](../vsto/how-to-prevent-outlook-from-displaying-a-form-region.md)
- [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)
- [Çalışma zamanında Şerite erişin](../vsto/accessing-the-ribbon-at-run-time.md)
