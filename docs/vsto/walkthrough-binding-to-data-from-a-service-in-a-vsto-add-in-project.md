---
title: VSTO eklenti projesindeki hizmetten veriye bağlama
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- databases [Office development in Visual Studio], scrolling records
- records [Office development in Visual Studio], scrolling
- data [Office development in Visual Studio], scrolling database records
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 60aefd40c48dc3789ab84ee5873aa6a53f4ee3fe
ms.sourcegitcommit: b56dc6fadc6c924beed36bb4c2ccc16cf6bcfa1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "68740116"
---
# <a name="walkthrough-bind-to-data-from-a-service-in-a-vsto-add-in-project"></a>İzlenecek yol: VSTO eklenti projesindeki bir hizmetten veriye bağlama
  VSTO eklenti projelerinde verileri konak denetimlerine bağlayabilirsiniz. Bu izlenecek yol, Microsoft Office bir Word belgesine nasıl denetim ekleneceğini, denetimlerin MSDN Içerik hizmetinden alınan verilere nasıl bağlanacağını ve çalışma zamanında olaylara nasıl yanıt verileceğini gösterir.

 **Uygulama hedefi:** Bu konudaki bilgiler Word 2010 için uygulama düzeyi projelere yöneliktir. Daha fazla bilgi edinmek için bkz. [Office Uygulaması ve Proje Türüne Göre Kullanılabilen Özellikler](../vsto/features-available-by-office-application-and-project-type.md).

 Bu izlenecek yol aşağıdaki görevleri gösterir:

- Çalışma zamanında bir belgeye denetimekleme.<xref:Microsoft.Office.Tools.Word.RichTextContentControl>

- <xref:Microsoft.Office.Tools.Word.RichTextContentControl> Denetimi bir Web hizmetinden veriye bağlama.

- <xref:Microsoft.Office.Tools.Word.ContentControlBase.Entering> Bir<xref:Microsoft.Office.Tools.Word.RichTextContentControl> denetimin olayına yanıt verme.

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolu tamamlamak için aşağıdaki bileşenlere ihtiyacınız vardır:

- [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]

- [!INCLUDE[Word_15_short](../vsto/includes/word-15-short-md.md)]veya [!INCLUDE[Word_14_short](../vsto/includes/word-14-short-md.md)].

## <a name="create-a-new-project"></a>Yeni bir proje oluşturma
 İlk adım, bir Word VSTO eklenti projesi oluşturmaktır.

### <a name="to-create-a-new-project"></a>Yeni bir proje oluşturmak için

1. Visual Basic veya C#kullanarak **MTPS içerik hizmeti**adlı bir Word VSTO eklentisi projesi oluşturun.

     Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

     Visual Studio, `ThisAddIn.vb` veya `ThisAddIn.cs` dosyasını açar ve projeyi **Çözüm Gezgini**ekler.

## <a name="add-a-web-service"></a>Web hizmeti Ekle
 Bu izlenecek yol için, MTPS Içerik hizmeti adlı bir Web hizmeti kullanın. Bu Web hizmeti, bir XML dizesi veya düz metin biçiminde belirtilen bir MSDN makalesindeki bilgileri döndürür. Daha sonraki bir adımda, döndürülen bilgilerin bir içerik denetiminde nasıl görüntüleneceği gösterilmektedir.

### <a name="to-add-the-mtps-content-service-to-the-project"></a>MTPS içerik hizmetini projeye eklemek için

1. **Veri** menüsünde **Yeni veri kaynağı Ekle**' ye tıklayın.

2. **Veri kaynağı Yapılandırma sihirbazında** **hizmet**' e ve ardından **İleri**' ye tıklayın.

3. **Adres** alanına aşağıdaki URL 'yi yazın:

     **http:\//Services.msdn.Microsoft.com/ContentServices/contentservice.asmx**

4. Tıklayın **Git**.

5. **Ad alanı** alanında **contentservice**yazın ve **Tamam**' a tıklayın.

6. **Başvuru ekleme Sihirbazı** Iletişim kutusunda **son**' a tıklayın.

## <a name="add-a-content-control-and-bind-to-data-at-runtime"></a>İçerik denetimi ekleme ve çalışma zamanında veriye bağlama
 VSTO eklenti projelerinde, çalışma zamanında denetimleri ekler ve bağlarsınız. Bu izlenecek yol için, Kullanıcı denetimin içine tıkladığında, içerik denetimini Web hizmetinden veri almaya yönelik şekilde yapılandırın.

### <a name="to-add-a-content-control-and-bind-to-data"></a>İçerik denetimi eklemek ve verilere bağlamak için

1. `ThisAddIn` Sınıfında, MTPS içerik hizmeti, içerik denetimi ve veri bağlama için değişkenleri bildirin.

     [!code-csharp[Trin_WordAddIn_BindingDataToContentControl#2](../vsto/codesnippet/CSharp/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.cs#2)]
     [!code-vb[Trin_WordAddIn_BindingDataToContentControl#2](../vsto/codesnippet/VisualBasic/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.vb#2)]

2. `ThisAddIn` Sınıfına aşağıdaki yöntemi ekleyin. Bu yöntem, etkin belgenin başlangıcında bir içerik denetimi oluşturur.

     [!code-csharp[Trin_WordAddIn_BindingDataToContentControl#4](../vsto/codesnippet/CSharp/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.cs#4)]
     [!code-vb[Trin_WordAddIn_BindingDataToContentControl#4](../vsto/codesnippet/VisualBasic/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.vb#4)]

3. `ThisAddIn` Sınıfına aşağıdaki yöntemi ekleyin. Bu yöntem, Web hizmetine bir istek oluşturmak ve göndermek için gereken nesneleri başlatır.

     [!code-csharp[Trin_WordAddIn_BindingDataToContentControl#6](../vsto/codesnippet/CSharp/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.cs#6)]
     [!code-vb[Trin_WordAddIn_BindingDataToContentControl#6](../vsto/codesnippet/VisualBasic/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.vb#6)]

4. Kullanıcı içerik denetiminin içini tıklattığında ve verileri içerik denetimine bağladığında içerik denetimleri hakkında MSDN Kitaplığı belgesini almak için bir olay işleyicisi oluşturun.

     [!code-csharp[Trin_WordAddIn_BindingDataToContentControl#5](../vsto/codesnippet/CSharp/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.cs#5)]
     [!code-vb[Trin_WordAddIn_BindingDataToContentControl#5](../vsto/codesnippet/VisualBasic/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.vb#5)]

5. `AddRichTextControlAtRange` `InitializeServiceObjects` Yönteminden ve`ThisAddIn_Startup` yöntemlerini çağırın. Programcılar C# için bir olay işleyicisi ekleyin.

     [!code-csharp[Trin_WordAddIn_BindingDataToContentControl#3](../vsto/codesnippet/CSharp/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.cs#3)]
     [!code-vb[Trin_WordAddIn_BindingDataToContentControl#3](../vsto/codesnippet/VisualBasic/trin_wordaddin_bindingdatatocontentcontrol/ThisAddIn.vb#3)]

## <a name="test-the-add-in"></a>Eklentiyi test etme
 Word 'ü <xref:Microsoft.Office.Tools.Word.RichTextContentControl> açtığınızda denetim görüntülenir. Denetimdeki metin, içinde tıkladığınızda değişir.

### <a name="to-test-the-vsto-add-in"></a>VSTO eklentisini test etmek için

1. **F5**tuşuna basın.

2. İçerik denetiminin içine tıklayın.

     Bilgiler, MTPS Içerik hizmetinden indirilir ve içerik denetimi içinde görüntülenir.

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
