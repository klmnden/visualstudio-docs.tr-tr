---
title: Office Projelerindeki Olaylar
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Sheet1_Startup
- ThisDocument_Shutdown
- ThisDocument_Startup
- application-level add-ins [Office development in Visual Studio], events
- event handlers [Office development in Visual Studio]
- ThisWorkbook_Startup
- Sheet2_Startup
- ThisWorkbook_Shutdown
- document-level customizations [Office development in Visual Studio], events
- Sheet2_Shutdown
- Startup event
- Sheet3_Shutdown
- add-ins [Office development in Visual Studio], events
- Shutdown event
- ThisAddIn_Startup
- Sheet3_Startup
- Startup method [Office development in Visual Studio]
- Shutdown method [Office development in Visual Studio]
- Sheet1_Shutdown
- events [Office development in Visual Studio]
- ThisAddIn_Shutdown
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ae8d89baf864c73bed42e4f478624bc930e3c143
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253617"
---
# <a name="events-in-office-projects"></a>Office Projelerindeki Olaylar
  Her Office proje şablonu otomatik olarak birkaç olay işleyicisi oluşturur. Belge düzeyi özelleştirmeleri için olay işleyicileri, VSTO eklentilerine yönelik olay işleyicilerinden biraz farklıdır.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

## <a name="document-level-projects"></a>Belge düzeyi projeleri
 Visual Studio, belge düzeyi özelleştirmelerde yeni veya mevcut belge veya çalışma sayfalarının arkasında oluşturulan kod sağlar. Bu kod iki farklı olay oluşturur: **Başlatma** ve **kapatmadan**.

### <a name="startup-event"></a>Startup olayı
 **Başlangıç** olayı, belge çalıştıktan sonra ana bilgisayar öğelerinin (belge, çalışma kitabı veya çalışma sayfası) her biri için oluşturulur ve derlemedeki tüm başlatma kodu çalıştırılır. Bu, kodunuzun üzerinde çalıştığı sınıfın oluşturucusunda çalıştırılacak son şeydir. Konak öğeleri hakkında daha fazla bilgi için bkz. [konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md).

 Belge düzeyinde bir proje oluşturduğunuzda, Visual Studio oluşturulan kod dosyalarındaki **Başlangıç** olayı için olay işleyicileri oluşturur:

- Microsoft Office Word projeleri için, olay işleyicisi olarak adlandırılır `ThisDocument_Startup`.

- Microsoft Office Excel projeleri için, olay işleyicileri aşağıdaki adlara sahiptir:

  - `Sheet1_Startup`

  - `Sheet2_Startup`

  - `Sheet3_Startup`

  - `ThisWorkbook_Startup`

### <a name="shutdown-event"></a>Shutdown olayı
 Bir konak öğesi (belge veya çalışma sayfası), kodunuzun yüklendiği uygulama etki alanının kaldırılması ile ilgili olduğu her bir konak öğesi için (belge veya çalışma sayfası) tetiklenir. Bu,, ' i kaldırdığından, sınıfında çağrılacak son şeydir.

 Belge düzeyinde bir proje oluşturduğunuzda, Visual Studio, oluşturulan kod dosyalarındaki **kapalı** olay için olay işleyicileri oluşturur:

- Microsoft Office Word projeleri için, olay işleyicisi olarak adlandırılır `ThisDocument_Shutdown`.

- Microsoft Office Excel projeleri için, olay işleyicileri aşağıdaki adlara sahiptir:

  - `Sheet1_Shutdown`

  - `Sheet2_Shutdown`

  - `Sheet3_Shutdown`

  - `ThisWorkbook_Shutdown`

> [!NOTE]
> Belgenin **kapalı** olay işleyicisi sırasında denetimleri program aracılığıyla kaldırmayın. **Kapatmadan** önce belgenin UI öğeleri artık kullanılamaz. Uygulama kapanmadan önce denetimleri kaldırmak istiyorsanız, kodunuzu, **Beforeckaybetme** veya **BeforeSave**gibi başka bir olay işleyicisine ekleyin.

### <a name="event-handler-method-declarations"></a>Olay işleyicisi yöntem bildirimleri
 Her olay işleyicisi yöntemi bildirimi kendisine geçirilen bağımsız değişkenlere sahiptir: *gönderici* ve *e*. Excel 'de *gönderici* bağımsız değişkeni, `Sheet1` veya `Sheet2`gibi bir sayfaya başvurur, *Gönderen* bağımsız değişkeni belgeye başvurur. *E* bağımsız değişkeni, bu durumda kullanılmayan bir olayın standart bağımsız değişkenlerine başvurur.

 Aşağıdaki kod örneği, Word için belge düzeyi projelerindeki varsayılan olay işleyicilerini gösterir.

 [!code-vb[Trin_VstcoreWordAutomation#121](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#121)]
 [!code-csharp[Trin_VstcoreWordAutomation#121](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#121)]

 Aşağıdaki kod örneği, Excel için belge düzeyi projelerindeki varsayılan olay işleyicilerini gösterir.

> [!NOTE]
> Aşağıdaki kod örneği, `Sheet1` sınıfındaki olay işleyicilerini gösterir. Diğer konak öğesi sınıflarında bulunan olay işleyicilerinin adları, sınıf adına karşılık gelir. Örneğin, `Sheet2` sınıfında, **Başlangıç** olayı işleyicisi adlandırılır `Sheet2_Startup`. Sınıfında, **Başlangıç** olayı işleyicisi adlandırılır `ThisWorkbook_Startup`. `ThisWorkbook`

 [!code-csharp[Trin_VstcoreExcelAutomation#83](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#83)]
 [!code-vb[Trin_VstcoreExcelAutomation#83](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#83)]

### <a name="order-of-events-in-document-level-excel-projects"></a>Belge düzeyindeki Excel projelerinde olay sırası
 Excel projelerindeki **Başlangıç** olayı işleyicileri şu sırada çağrılır:

1. `ThisWorkbook_Startup`.

2. `Sheet1_Startup`.

3. `Sheet2_Startup`.

4. `Sheet3_Startup`.

5. Sırayla diğer sayfalar.

   Çalışma kitabı çözümündeki **kapalı** olay işleyicileri şu sırada çağrılır:

6. `ThisWorkbook_Shutdown`.

7. `Sheet1_Shutdown`.

8. `Sheet2_Shutdown`.

9. `Sheet3_Shutdown`.

10. Sırayla diğer sayfalar.

    Sıra, proje derlendiğinde belirlenir. Kullanıcı çalışma zamanında sayfaları yeniden düzenler, çalışma kitabının bir sonraki açılışında veya kapatılışında olayların oluşturulma sırasını değiştirmez.

## <a name="vsto-add-in-projects"></a>VSTO eklenti projeleri
 Visual Studio, VSTO eklentilerinde oluşturulan kodu sağlar. Bu kod iki farklı olay oluşturur: <xref:Microsoft.Office.Tools.AddInBase.Startup> ve <xref:Microsoft.Office.Tools.AddInBase.Shutdown>.

### <a name="startup-event"></a>Startup olayı
 <xref:Microsoft.Office.Tools.AddIn.Startup> Olay, VSTO eklentisi yüklendikten sonra ve derlemedeki tüm başlatma kodları çalıştırıldıktan sonra tetiklenir. Bu olay, oluşturulan kod dosyasındaki `ThisAddIn_Startup` yöntemi tarafından işlenir.

 VSTO eklentisi <xref:Microsoft.Office.Tools.AddInBase.RequestComAddInAutomationService%2A> yöntemi geçersiz kılmadığı takdirde olayişleyicisindekikod,çalıştırılacakilkkullanıcıkodudur.`ThisAddIn_Startup` Bu durumda, `ThisAddIn_Startup` olay işleyicisi öğesinden sonra <xref:Microsoft.Office.Tools.AddInBase.RequestComAddInAutomationService%2A>çağrılır.

 Kod bir belgenin açık olmasını `ThisAdd-In_Startup` gerektiriyorsa olay işleyicisine kod eklemeyin. Bunun yerine, bir Kullanıcı bir belge oluşturduğunda veya açtığında Office uygulamasının oluşturduğu bir olaya bu kodu ekleyin. Daha fazla bilgi için bkz. [Office uygulaması başladığında belgeye erişme](../vsto/programming-vsto-add-ins.md#AccessingDocuments).

 VSTO eklentilerinin başlangıç dizisi hakkında daha fazla bilgi için bkz. [VSTO eklentileri mimarisi](../vsto/architecture-of-vsto-add-ins.md).

### <a name="shutdown-event"></a>Shutdown olayı
 <xref:Microsoft.Office.Tools.AddInBase.Shutdown> Olay, kodunuzun yüklendiği uygulama etki alanı boşaltılacak şekilde olduğunda tetiklenir. Bu olay, oluşturulan kod dosyasındaki `ThisAddIn_Shutdown` yöntemi tarafından işlenir. Bu olay işleyicisi, VSTO eklentisi kaldırıldığında çalıştırılacak son kullanıcı kodudur.

#### <a name="shutdown-event-in-outlook-vsto-add-ins"></a>Outlook VSTO Eklentilerindeki kapalı olayı
 <xref:Microsoft.Office.Tools.AddInBase.Shutdown> Olay yalnızca Kullanıcı Outlook 'ta com eklentileri iletişim kutusunu kullanarak VSTO eklentisini devre dışı bıraktığında tetiklenir. Outlook çıktığında bu değildir. Outlook 'Tan çıkıldığında çalışması gereken bir kodunuz varsa, aşağıdaki olaylardan birini işleyin:

- <xref:Microsoft.Office.Interop.Outlook.Application> Nesnesinin <xref:Microsoft.Office.Interop.Outlook.ApplicationEvents_11_Event.Quit> olayı.

- <xref:Microsoft.Office.Interop.Outlook.Explorer> Nesnesinin <xref:Microsoft.Office.Interop.Outlook.ExplorerEvents_10_Event.Close> olayı.

> [!NOTE]
> Outlook 'u, çıkış sırasında kayıt defteri <xref:Microsoft.Office.Tools.AddInBase.Shutdown> 'ni değiştirerek olayı daha sonra tetikleyerek uygulamayı zorlayabilirsiniz. Ancak, bir yönetici bu ayarı geri döndürüyorsa, `ThisAddIn_Shutdown` yönteme eklediğiniz herhangi bir kod artık Outlook 'tan çıkıldığında çalışmaz. Daha fazla bilgi için bkz. [Outlook 2010 için değişiklikleri kapatır](http://go.microsoft.com/fwlink/?LinkID=184614).

## <a name="see-also"></a>Ayrıca bkz.
- [Office çözümleri geliştirme](../vsto/developing-office-solutions.md)
- [Nasıl yapılır: Visual Studio 'da Office projeleri oluşturma](../vsto/how-to-create-office-projects-in-visual-studio.md)
- [Program belge düzeyi özelleştirmeleri](../vsto/programming-document-level-customizations.md)
- [Program VSTO eklentileri](../vsto/programming-vsto-add-ins.md)
- [Office proje şablonlarına genel bakış](../vsto/office-project-templates-overview.md)
