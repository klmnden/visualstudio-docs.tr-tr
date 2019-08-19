---
title: 'İzlenecek yol: Excel için ilk VSTO eklentisini oluşturma'
ms.date: 08/14/2019
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- application-level add-ins [Office development in Visual Studio], creating your first project
- Office development in Visual Studio, creating your first project
- add-ins [Office development in Visual Studio], creating your first project
- Excel [Office development in Visual Studio], creating your first project
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 52b683b1f75f2967807f171c204fbf02a2e5db69
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69548007"
---
# <a name="walkthrough-create-your-first-vsto-add-in-for-excel"></a>İzlenecek yol: Excel için ilk VSTO eklentisini oluşturma
  Bu açıklayıcı izlenecek yol, Excel Microsoft Office için uygulama düzeyi eklentisi oluşturmayı gösterir. Bu tür çözümde oluşturduğunuz özellikler, hangi çalışma kitaplarının açık olduğuna bakılmaksızın uygulamanın kendisi tarafından kullanılabilir.

 [!INCLUDE[appliesto_xlallapp](../vsto/includes/appliesto-xlallapp-md.md)]

[!include[Add-ins note](includes/addinsnote.md)]

 Bu izlenecek yol aşağıdaki görevleri gösterir:

- Excel için Excel VSTO eklentisi projesi oluşturma.

- Çalışma kitabına metin eklemek için Excel 'in nesne modelini kullanan kodu yazma.

- Test etmek için projeyi oluşturma ve çalıştırma.

- VSTO eklentisinin geliştirme bilgisayarınızda artık otomatik olarak çalışmamasını sağlamak için tamamlanmış projeyi Temizleme.

  [!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolu tamamlamak için aşağıdaki bileşenlere ihtiyacınız vardır:

- [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]

- [!INCLUDE[Excel_15_short](../vsto/includes/excel-15-short-md.md)]veya [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)].

## <a name="create-the-project"></a>Projeyi oluşturma

#### <a name="to-create-a-new-excel-vsto-add-in-project-in-visual-studio"></a>Visual Studio 'da yeni bir Excel VSTO eklentisi projesi oluşturmak için

1. Başlangıç [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].

2. **Dosya** menüsünde, **Yeni**' nin üzerine gelin ve ardından **Proje**' ye tıklayın.

3. Şablonlar bölmesinde, **Visual C#**  veya **Visual Basic**öğesini genişletin ve ardından **Office/SharePoint**' i genişletin.

4. Genişletilmiş **Office/SharePoint** düğümü altında **Office eklentileri** düğümünü seçin.

5. Proje şablonları listesinde, **excel 2010 eklentisi** veya **Excel 2013 eklentisi**' ni seçin.

6. **Ad** kutusuna **FirstExcelAddIn**yazın.

7.           **Tamam**'ı tıklatın.

     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]**FirstExcelAddIn** projesini oluşturur ve ThisAddIn kod dosyasını düzenleyicide açar.

## <a name="write-code-to-add-text-to-the-saved-workbook"></a>Kaydedilen çalışma kitabına metin eklemek için kod yazın
 Ardından, ThisAddIn kod dosyasına kod ekleyin. Yeni kod, etkin çalışma sayfasının ilk satırına ortak metin eklemek için Excel nesne modelini kullanır. Etkin çalışma sayfası, Kullanıcı çalışma kitabını kaydettiğinde açık olan çalışma kitabıdır. Varsayılan olarak, ThisAddIn kod dosyası aşağıdaki oluşturulan kodu içerir:

- `ThisAddIn` Sınıfın kısmi tanımı. Bu sınıf, kodunuz için bir giriş noktası sağlar ve Excel 'in nesne modeline erişim sağlar. Daha fazla bilgi için bkz. [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md). `ThisAddIn` Sınıfın geri kalanı, değiştirmemelisiniz bir gizli kod dosyasında tanımlanır.

- `ThisAddIn_Startup` Ve`ThisAddIn_Shutdown` olay işleyicileri. Bu olay işleyicileri, Excel VSTO eklentinizi yüklediğinde ve kaldırdığında çağrılır. Bu olay işleyicilerini, yüklendiğinde VSTO eklentisini başlatmak ve eklenti tarafından kullanılan kaynakları temizlemek için kullanın. Daha fazla bilgi için bkz. [Office Projelerindeki Olaylar](../vsto/events-in-office-projects.md).

### <a name="to-add-a-line-of-text-to-the-saved-workbook"></a>Kaydedilen çalışma kitabına bir metin satırı eklemek için

1. ThisAddIn kod dosyasında, `ThisAddIn` sınıfına aşağıdaki kodu ekleyin. Yeni kod, bir çalışma kitabı kaydedildiğinde oluşan olay <xref:Microsoft.Office.Interop.Excel.AppEvents_Event.WorkbookBeforeSave> için bir olay işleyicisini tanımlar.

    Kullanıcı bir çalışma kitabını kaydettiğinde, olay işleyicisi etkin çalışma sayfasının başlangıcına yeni metin ekler.

    [!code-vb[Trin_ExcelAddInTutorial#1](../vsto/codesnippet/VisualBasic/Trin_ExcelAddInTutorial/ThisAddIn.vb#1)]
    [!code-csharp[Trin_ExcelAddInTutorial#1](../vsto/codesnippet/CSharp/Trin_ExcelAddInTutorial/ThisAddIn.cs#1)]

2. Kullanıyorsanız C#, `ThisAddIn_Startup` olay işleyicisine aşağıdaki gerekli kodu ekleyin. Bu kod `Application_WorkbookBeforeSave` olay işleyicisini <xref:Microsoft.Office.Interop.Excel.AppEvents_Event.WorkbookBeforeSave> olayla bağlamak için kullanılır.

    [!code-csharp[Trin_ExcelAddInTutorial#2](../vsto/codesnippet/CSharp/Trin_ExcelAddInTutorial/ThisAddIn.cs#2)]

   Çalışma kitabını kaydedildiğinde değiştirmek için, önceki kod örnekleri aşağıdaki nesneleri kullanır:

- `ThisAddIn` Sınıfının `Application` alanı. Alan, Excel 'in <xref:Microsoft.Office.Interop.Excel.Application> geçerli örneğini temsil eden bir nesne döndürür. `Application`

- <xref:Microsoft.Office.Interop.Excel.AppEvents_Event.WorkbookBeforeSave> `Wb` Olay işleyicisinin olay işleyicisi parametresi. Parametresi, kaydedilen çalışma <xref:Microsoft.Office.Interop.Excel.Workbook> kitabını temsil eden bir nesnedir. `Wb` Daha fazla bilgi için [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md).

## <a name="test-the-project"></a>Projeyi test etme

### <a name="to-test-the-project"></a>Projeyi test etmek için

1. Projenizi derlemek ve çalıştırmak için **F5** tuşuna basın.

     Projeyi derlediğinizde kod, projenin yapı çıkış klasörüne dahil olan bir derlemeye derlenir. Visual Studio Ayrıca, Excel 'In VSTO eklentisini bulmasını ve yüklemesini sağlayan bir kayıt defteri girişleri kümesi oluşturur ve VSTO eklentisinin çalışmasını sağlamak için geliştirme bilgisayarındaki güvenlik ayarlarını yapılandırır. Daha fazla bilgi için bkz. [Office çözümleri oluşturma](../vsto/building-office-solutions.md).

2. Excel 'de çalışma kitabını kaydedin.

3. Aşağıdaki metnin çalışma kitabına eklendiğini doğrulayın.

     **Bu metin kod kullanılarak eklenmiştir.**

4. Excel 'i kapatın.

## <a name="clean-up-the-project"></a>Projeyi temizle
 Projeyi geliştirmeyi bitirdiğinizde, VSTO eklenti derlemesini, kayıt defteri girişlerini ve güvenlik ayarlarını geliştirme bilgisayarınızdan kaldırın. Aksi halde, VSTO eklentisi, geliştirme bilgisayarınızda Excel 'i her açışınızda çalışmaya devam edecektir.

### <a name="to-clean-up-the-completed-project-on-your-development-computer"></a>Geliştirme bilgisayarınızda tamamlanmış projeyi temizlemek için

1. Visual Studio 'da, **Yapı** menüsünde **Çözümü Temizle**' ye tıklayın.

## <a name="next-steps"></a>Sonraki adımlar
 Excel için temel bir VSTO eklentisi oluşturduğunuza göre, şu konulardan VSTO eklentileri geliştirme hakkında daha fazla bilgi edinebilirsiniz:

- VSTO eklentilerinde gerçekleştirebileceğiniz genel programlama görevleri: [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md).

- Excel VSTO eklentilerine özgü programlama görevleri: [Excel çözümleri](../vsto/excel-solutions.md).

- Excel 'in nesne modelini kullanma: [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md).

- Excel 'in Kullanıcı arabirimini (UI) özelleştirme (örneğin, şerit 'e özel bir sekme ekleyerek veya kendi özel görev bölmenizi oluşturarak). [OFFICE UI özelleştirmesi](../vsto/office-ui-customization.md).

- Excel için VSTO eklentileri oluşturma ve hata ayıklama: [Office çözümleri oluşturun](../vsto/building-office-solutions.md).

- Excel için VSTO eklentileri dağıtma: [Office çözümünü dağıtın](../vsto/deploying-an-office-solution.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümleri geliştirmesine genel &#40;bakış VSTO&#41;](../vsto/office-solutions-development-overview-vsto.md)
- [Excel çözümleri](../vsto/excel-solutions.md)
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [Excel nesne modeline genel bakış](../vsto/excel-object-model-overview.md)
- [Office UI özelleştirmesi](../vsto/office-ui-customization.md)
- [Office çözümleri oluşturma](../vsto/building-office-solutions.md)
- [Office çözümünü dağıtma](../vsto/deploying-an-office-solution.md)
- [Office proje şablonlarına genel bakış](../vsto/office-project-templates-overview.md)
