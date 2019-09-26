---
title: 'İzlenecek yol: VSTO eklenti projesinde basit veri bağlama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data [Office development in Visual Studio], binding data
- data binding [Office development in Visual Studio], Word
- data [Office development in Visual Studio], simple binding data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 0e174782c46d24b7743d50faa9fac69d38c3d6c6
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255189"
---
# <a name="walkthrough-simple-data-binding-in-vsto-add-in-project"></a>İzlenecek yol: VSTO eklenti projesinde basit veri bağlama

VSTO eklenti projelerinde verileri konak denetimlerine ve Windows Forms denetimlerine bağlayabilirsiniz. Bu izlenecek yol, Microsoft Office bir Word belgesine nasıl denetim ekleneceğini ve çalışma zamanında denetimleri verilere nasıl bağlayacağınızı gösterir.

[!INCLUDE[appliesto_wdallapp](../vsto/includes/appliesto-wdallapp-md.md)]

Bu izlenecek yol aşağıdaki görevleri gösterir:

- <xref:Microsoft.Office.Tools.Word.ContentControl> Çalışma zamanında belgeye ekleme.

- Denetimi bir <xref:System.Windows.Forms.BindingSource> veri kümesinin örneğine bağlayan bir oluşturma.

- Kullanıcının kayıtlarda gezinmelerini ve denetimde görüntülemesini sağlama.

[!INCLUDE[note_settings_general](../sharepoint/includes/note-settings-general-md.md)]

## <a name="prerequisites"></a>Önkoşullar

Bu izlenecek yolu tamamlamak için aşağıdaki bileşenlere ihtiyacınız vardır:

- [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]

- [!INCLUDE[Word_15_short](../vsto/includes/word-15-short-md.md)]veya [!INCLUDE[Word_14_short](../vsto/includes/word-14-short-md.md)].

- `AdventureWorksLT` Örnek veritabanının eklendiği SQL Server 2005 veya SQL Server 2005 Express 'in çalışan bir örneğine erişim. `AdventureWorksLT` Veritabanını [CodePlex Web sitesinden](http://go.microsoft.com/fwlink/?LinkId=115611)indirebilirsiniz. Veritabanı ekleme hakkında daha fazla bilgi için aşağıdaki konulara bakın:

  - SQL Server Management Studio veya SQL Server Management Studio Express kullanarak bir veritabanı eklemek için bkz [. nasıl yapılır: Bir veritabanı ekleyin (SQL Server Management Studio)](/sql/relational-databases/databases/attach-a-database).

  - Komut satırını kullanarak bir veritabanı eklemek için bkz [. nasıl yapılır: SQL Server Express](/previous-versions/sql/)bir veritabanı dosyası ekleyin.

## <a name="create-a-new-project"></a>Yeni bir proje oluşturma

İlk adım, bir Word VSTO eklenti projesi oluşturmaktır.

### <a name="to-create-a-new-project"></a>Yeni bir proje oluşturmak için

1. Visual Basic veya C#kullanarak **bir veritabanından belge doldurma**adlı bir Word VSTO eklentisi projesi oluşturun.

     Daha fazla bilgi için [nasıl yapılır: Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)'da Office projeleri oluşturun.

     Visual Studio, *ThisAddIn. vb* veya *ThisAddIn.cs* dosyasını açar ve **belgeyi bir veritabanı projesinden doldurma** **Çözüm Gezgini**ekler.

2. [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] Projeniz[!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]veya ' i hedefliyorsa, *Microsoft. Office. Tools. Word. v 4.0. Utilities. dll* derlemesine bir başvuru ekleyin. Bu izlenecek yolda daha sonra belgeye Windows Forms denetimleri eklemek için bu başvuru gerekir.

## <a name="create-a-data-source"></a>Bir veri kaynağı oluşturun

Projenize türü belirtilmiş bir veri kümesi eklemek için **veri kaynakları** penceresini kullanın.

### <a name="to-add-a-typed-dataset-to-the-project"></a>Projeye türü belirtilmiş bir veri kümesi eklemek için

1. **Veri kaynakları** penceresi görünür değilse, menü çubuğunda,**diğer Windows** > **veri kaynaklarını** **görüntüle** > ' yi seçerek bunu görüntüleyin.

2. **Veri kaynağı Yapılandırma Sihirbazı 'nı**başlatmak Için **Yeni veri kaynağı Ekle** ' yi seçin.

3. **Veritabanı**' na ve ardından **İleri**' ye tıklayın.

4. `AdventureWorksLT` Veritabanına var olan bir bağlantınız varsa, bu bağlantıyı seçin ve **İleri**' ye tıklayın.

    Aksi takdirde, **Yeni bağlantı**' ya tıklayın ve yeni bağlantıyı oluşturmak Için **bağlantı ekle** iletişim kutusunu kullanın. Daha fazla bilgi için bkz. [yeni bağlantılar ekleme](../data-tools/add-new-connections.md).

5. **Bağlantı dizesini uygulama yapılandırma dosyasına kaydet** sayfasında, **İleri**' ye tıklayın.

6. **Veritabanı nesnelerinizi seçin** sayfasında **Tablolar** ' ı genişletin ve müşteri ' yi **(SalesLT)** seçin.

7. **Son**'a tıklayın.

    *AdventureWorksLTDataSet. xsd* dosyası **Çözüm Gezgini**eklenir. Bu dosya aşağıdaki öğeleri tanımlar:

   - Adında `AdventureWorksLTDataSet`bir türü belirtilmiş veri kümesi. Bu veri kümesi AdventureWorksLT veritabanındaki **Customer (SalesLT)** tablosunun içeriğini temsil eder.

   - Adında `CustomerTableAdapter`bir TableAdapter. Bu TableAdapter, `AdventureWorksLTDataSet`içindeki verileri okumak ve yazmak için kullanılabilir. Daha fazla bilgi için bkz. [TableAdapter Overview](../data-tools/fill-datasets-by-using-tableadapters.md#tableadapter-overview).

     Bu iki nesneyi daha sonra Bu izlenecek yolda kullanacaksınız.

## <a name="create-controls-and-binding-controls-to-data"></a>Verilere denetimler oluşturma ve denetimleri bağlama

Bu izlenecek yolda veritabanı kayıtlarını görüntüleme arabirimi temel ve belge içinde oluşturulur. Tek seferde tek bir veritabanı kaydını <xref:Microsoft.Office.Tools.Word.Controls.Button> görüntülerveikidenetimkayıtlardailerivegerikaydıramanızaimkantanır.<xref:Microsoft.Office.Tools.Word.ContentControl> İçerik denetimi, veritabanına bağlanmak <xref:System.Windows.Forms.BindingSource> için bir kullanır.

Verilere yönelik bağlama denetimleri hakkında daha fazla bilgi için bkz. [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md).

### <a name="to-create-the-interface-in-the-document"></a>Belgede arabirim oluşturmak için

1. Sınıfında, `AdventureWorksLTDataSet` veritabanı `Customer` tablosunu göstermek ve kaydırmak için aşağıdaki denetimleri bildirin. `ThisAddIn`

     [!code-vb[Trin_WordAddInDatabase#1](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#1)]
     [!code-csharp[Trin_WordAddInDatabase#1](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#1)]

2. Yönteminde, veri kümesini başlatmak için aşağıdaki kodu ekleyin, veri kümesini `AdventureWorksLTDataSet` veritabanından alınan bilgilerle doldurabilirsiniz. `ThisAddIn_Startup`

     [!code-vb[Trin_WordAddInDatabase#2](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#2)]
     [!code-csharp[Trin_WordAddInDatabase#2](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#2)]

3. `ThisAddIn_Startup` Yöntemine aşağıdaki kodu ekleyin. Bu, belgeyi genişleten bir konak öğesi oluşturur. Daha fazla bilgi için bkz. [çalışma ZAMANıNDA VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md).

     [!code-vb[Trin_WordAddInDatabase#3](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#3)]
     [!code-csharp[Trin_WordAddInDatabase#3](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#3)]

4. Belgenin başlangıcında birkaç Aralık tanımlayın. Bu aralıklar, metin eklemek ve denetimlerin yerleştirileceği yeri belirler.

     [!code-vb[Trin_WordAddInDatabase#4](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#4)]
     [!code-csharp[Trin_WordAddInDatabase#4](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#4)]

5. Arabirim denetimlerini daha önce tanımlı aralıklara ekleyin.

     [!code-vb[Trin_WordAddInDatabase#5](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#5)]
     [!code-csharp[Trin_WordAddInDatabase#5](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#5)]

6. Kullanarak içerik denetimini `AdventureWorksLTDataSet` bağlayın. <xref:System.Windows.Forms.BindingSource> Geliştiriciler C# için, <xref:Microsoft.Office.Tools.Word.Controls.Button> denetimler için iki olay işleyicisi ekleyin.

     [!code-vb[Trin_WordAddInDatabase#6](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#6)]
     [!code-csharp[Trin_WordAddInDatabase#6](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#6)]

7. Veritabanı kayıtlarında gezinmek için aşağıdaki kodu ekleyin.

     [!code-vb[Trin_WordAddInDatabase#7](../vsto/codesnippet/VisualBasic/trin_wordaddindatabase/ThisAddIn.vb#7)]
     [!code-csharp[Trin_WordAddInDatabase#7](../vsto/codesnippet/CSharp/trin_wordaddindatabase/ThisAddIn.cs#7)]

## <a name="test-the-add-in"></a>Eklentiyi test etme

Word 'ü açtığınızda içerik denetimi veri `AdventureWorksLTDataSet` kümesinden verileri görüntüler. **Sonraki** ve **önceki** düğmelere tıklayarak veritabanı kayıtlarında ilerleyin.

### <a name="to-test-the-vsto-add-in"></a>VSTO eklentisini test etmek için

1. **F5**tuşuna basın.

     Adlı `customerContentControl` bir içerik denetimi oluşturulur ve verilerle doldurulur. Aynı zamanda, adlı `adventureWorksLTDataSet` <xref:System.Windows.Forms.BindingSource> ve `customerBindingSource` adlı bir veri kümesi nesnesi projeye eklenir. <xref:Microsoft.Office.Tools.Word.ContentControl> , <xref:System.Windows.Forms.BindingSource>' A bağlanır ve veri kümesi nesnesine bağlanır.

2. Veritabanı kayıtlarında gezinmek için **İleri** ve **önceki** düğmelere tıklayın.

## <a name="see-also"></a>Ayrıca bkz.

- [Office çözümlerindeki veriler](../vsto/data-in-office-solutions.md)
- [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md)
- [Nasıl yapılır: Çalışma sayfalarını bir veritabanındaki verilerle doldurma](../vsto/how-to-populate-worksheets-with-data-from-a-database.md)
- [Nasıl yapılır: Belgeleri bir veritabanındaki verilerle doldurma](../vsto/how-to-populate-documents-with-data-from-a-database.md)
- [Nasıl yapılır: Belgeleri hizmetlerdeki verilerle Doldur](../vsto/how-to-populate-documents-with-data-from-services.md)
- [Nasıl yapılır: Nesneleri nesnelerdeki verilerle Doldur](../vsto/how-to-populate-documents-with-data-from-objects.md)
- [Nasıl yapılır: Çalışma sayfasındaki veritabanı kayıtları arasında kaydırma](../vsto/how-to-scroll-through-database-records-in-a-worksheet.md)
- [Nasıl yapılır: Bir veri kaynağını konak denetimindeki verilerle güncelleştirme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)
- [İzlenecek yol: Belge düzeyi projede basit veri bağlama](../vsto/walkthrough-simple-data-binding-in-a-document-level-project.md)
- [İzlenecek yol: Belge düzeyi projede karmaşık veri bağlama](../vsto/walkthrough-complex-data-binding-in-a-document-level-project.md)
- [Office çözümlerinde yerel veritabanı dosyalarını kullanma genel bakış](../vsto/using-local-database-files-in-office-solutions-overview.md)
- [Yeni veri kaynağı ekleme](../data-tools/add-new-data-sources.md)
- [Visual Studio'da verilere Windows Forms denetimleri bağlama](../data-tools/bind-windows-forms-controls-to-data-in-visual-studio.md)
- [Nasıl yapılır: Nesneleri nesnelerdeki verilerle Doldur](../vsto/how-to-populate-documents-with-data-from-objects.md)
- [Nasıl yapılır: Bir veri kaynağını konak denetimindeki verilerle güncelleştirme](../vsto/how-to-update-a-data-source-with-data-from-a-host-control.md)
- [Office çözümlerinde yerel veritabanı dosyalarını kullanma genel bakış](../vsto/using-local-database-files-in-office-solutions-overview.md)
- [BindingSource Bileşenine Genel Bakış](/dotnet/framework/winforms/controls/bindingsource-component-overview)
