---
title: 'İzlenecek yol: Bir sunucudaki çalışma kitabındaki önbelleğe alınmış verileri değiştirme'
ms.date: 08/14/2019
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- workbooks [Office development in Visual Studio], changing server data
- datasets [Office development in Visual Studio], accessing on server
- server-side data access [Office development in Visual Studio]
- data [Office development in Visual Studio], accessing on server
- documents [Office development in Visual Studio], server-side data access
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 06fb2532a128384369a9f3617166c9f340f21030
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551343"
---
# <a name="walkthrough-change-cached-data-in-a-workbook-on-a-server"></a>İzlenecek yol: Bir sunucudaki çalışma kitabındaki önbelleğe alınmış verileri değiştirme
  Bu izlenecek yol, Microsoft Office bir Excel çalışma kitabında önbelleğe alınmış bir veri kümesinin <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> sınıfını kullanarak Excel 'i başlatmadan nasıl değiştirileceğini gösterir.

 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]

[!include[Add-ins note](includes/addinsnote.md)]

 Bu izlenecek yol aşağıdaki görevleri gösterir:

- AdventureWorksLT veritabanından veri içeren bir veri kümesi tanımlama.

- Excel çalışma kitabı projesinde ve konsol uygulaması projesinde veri kümesinin örneklerini oluşturma.

- Çalışma kitabındaki <xref:Microsoft.Office.Tools.Excel.ListObject> veri kümesine bağlanan bir oluşturma ve çalışma kitabı açıldığında verileri <xref:Microsoft.Office.Tools.Excel.ListObject> ile doldurma.

- Çalışma kitabındaki veri kümesini veri önbelleğine ekleme.

- Excel 'i başlatmadan, konsol uygulamasındaki kodu çalıştırarak önbelleğe alınmış veri kümesindeki verilerin bir sütununu değiştirme.

  Bu izlenecek yol, geliştirme bilgisayarınızda kodu çalıştırdığınız varsayılmaktadır, ancak bu izlenecek yol tarafından gösterilen kod, Excel yüklü olmayan bir sunucuda kullanılabilir.

> [!NOTE]
> Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için bkz. [Visual STUDIO IDE 'Yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md).

## <a name="prerequisites"></a>Önkoşullar
 Bu izlenecek yolu tamamlamak için aşağıdaki bileşenlere ihtiyacınız vardır:

- [!INCLUDE[vsto_vsprereq](../vsto/includes/vsto-vsprereq-md.md)]

- [!INCLUDE[Excel_14_short](../vsto/includes/excel-14-short-md.md)].

- AdventureWorksLT örnek veritabanının eklendiği Microsoft SQL Server veya Microsoft SQL Server Express çalışan bir örneğine erişim. AdventureWorksLT veritabanını [CodePlex Web sitesinden](http://go.microsoft.com/fwlink/?linkid=87843)indirebilirsiniz. Veritabanı ekleme hakkında daha fazla bilgi için aşağıdaki konulara bakın:

  - SQL Server Management Studio veya SQL Server Management Studio Express kullanarak bir veritabanı eklemek için bkz [. nasıl yapılır: Bir veritabanı ekleyin (SQL Server Management Studio)](/sql/relational-databases/databases/attach-a-database).

  - Komut satırını kullanarak bir veritabanı eklemek için bkz [. nasıl yapılır: SQL Server Express](/previous-versions/sql/)bir veritabanı dosyası ekleyin.

## <a name="create-a-class-library-project-that-defines-a-dataset"></a>Veri kümesini tanımlayan bir sınıf kitaplığı projesi oluşturma
 Bir Excel çalışma kitabı projesinde ve bir konsol uygulamasında aynı veri kümesini kullanmak için, veri kümesini bu projelerin her ikisi tarafından başvurulan ayrı bir derlemede tanımlamanız gerekir. Bu izlenecek yol için bir sınıf kitaplığı projesinde veri kümesini tanımlayın.

### <a name="to-create-the-class-library-project"></a>Sınıf kitaplığı projesi oluşturmak için

1. Başlangıç [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].

2. **Dosya** menüsünde, **Yeni**' nin üzerine gelin ve ardından **Proje**' ye tıklayın.

3. Şablonlar bölmesinde,  **C# görsel** veya **Visual Basic**öğesini genişletin ve ardından **Windows**' a tıklayın.

4. Proje şablonları listesinde, **sınıf kitaplığı**' nı seçin.

5. **Ad** kutusuna **AdventureWorksDataSet**yazın.

6. **Araştır**' a tıklayın, *%USERPROFILE%\My BELGELERINIZE* (Windows XP ve önceki sürümler için) veya *%UserProfile%\Documents* (Windows Vista Için) klasörüne gidin ve ardından **Klasör Seç**' e tıklayın.

7. **Yeni proje** iletişim kutusunda, **çözüm için dizin oluştur** onay kutusunun seçili olmadığından emin olun.

8.           **Tamam**'ı tıklatın.

     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]**Çözüm Gezgini** Için bir **AdventureWorksDataSet** projesi ekler ve **Class1.cs** veya **Class1. vb** kod dosyasını açar.

9. **Çözüm Gezgini**' de, **Class1.cs** veya **Class1. vb**öğesine sağ tıklayın ve ardından **Sil**' e tıklayın. Bu izlenecek yol için bu dosyaya ihtiyacınız yoktur.

## <a name="define-a-dataset-in-the-class-library-project"></a>Sınıf kitaplığı projesinde bir veri kümesi tanımlama
 SQL Server 2005 için AdventureWorksLT veritabanından veri içeren bir türü belirtilmiş veri kümesi tanımlayın. Bu izlenecek yolda daha sonra, bu veri kümesine bir Excel çalışma kitabı projesinden ve konsol uygulaması projesinden başvurabileceksiniz.

 Veri kümesi, AdventureWorksLT veritabanının Product tablosundaki verileri temsil eden türsüz bir *veri* kümesidir. Türü belirtilmiş veri kümeleri hakkında daha fazla bilgi için bkz. [Visual Studio 'Da veri kümesi araçları](../data-tools/dataset-tools-in-visual-studio.md).

### <a name="to-define-a-typed-dataset-in-the-class-library-project"></a>Sınıf kitaplığı projesinde türü belirtilmiş bir veri kümesini tanımlamak için

1. **Çözüm Gezgini**' de, **AdventureWorksDataSet** projesine tıklayın.

2. **Veri kaynakları** penceresi görünür değilse, menü çubuğunda,**diğer Windows** > **veri kaynaklarını** **görüntüle** > ' yi seçerek bunu görüntüleyin.

3. **Veri kaynağı Yapılandırma Sihirbazı 'nı**başlatmak Için **Yeni veri kaynağı Ekle** ' yi seçin.

4. **Veritabanı**' na ve ardından **İleri**' ye tıklayın.

5. AdventureWorksLT veritabanına mevcut bir bağlantınız varsa, bu bağlantıyı seçin ve **İleri**' ye tıklayın.

    Aksi takdirde, **Yeni bağlantı**' ya tıklayın ve yeni bağlantıyı oluşturmak Için **bağlantı ekle** iletişim kutusunu kullanın. Daha fazla bilgi için bkz. [yeni bağlantılar ekleme](../data-tools/add-new-connections.md).

6. **Bağlantı dizesini uygulama yapılandırma dosyasına kaydet** sayfasında, **İleri**' ye tıklayın.

7. **Veritabanı nesnelerinizi seçin** sayfasında **Tablolar** ' ı genişletin ve **ürün (SalesLT)** öğesini seçin.

8.           **Son**'a tıklayın.

    *AdventureWorksLTDataSet. xsd* dosyası, **AdventureWorksDataSet** projesine eklenir. Bu dosya aşağıdaki öğeleri tanımlar:

   - Adında `AdventureWorksLTDataSet`bir türü belirtilmiş veri kümesi. Bu veri kümesi AdventureWorksLT veritabanındaki ürün tablosunun içeriğini temsil eder.

   - Adında `ProductTableAdapter`bir TableAdapter. Bu TableAdapter, `AdventureWorksLTDataSet`içindeki verileri okumak ve yazmak için kullanılabilir. Daha fazla bilgi için bkz. [TableAdapter Overview](../data-tools/fill-datasets-by-using-tableadapters.md#tableadapter-overview).

     Bu iki nesneyi daha sonra Bu izlenecek yolda kullanacaksınız.

9. **Çözüm Gezgini**, **AdventureWorksDataSet** öğesine sağ tıklayın ve **Oluştur**' a tıklayın.

     Projenin hata olmadan yapılandırıldığını doğrulayın.

## <a name="create-an-excel-workbook-project"></a>Excel çalışma kitabı projesi oluşturma
 Veri arabirimi için bir Excel çalışma kitabı projesi oluşturun. Bu kılavuzda daha sonra, verileri görüntüleyen bir <xref:Microsoft.Office.Tools.Excel.ListObject> oluşturacak ve veri kümesinin bir örneğini çalışma kitabındaki veri önbelleğine ekleyeceksiniz.

### <a name="to-create-the-excel-workbook-project"></a>Excel çalışma kitabı projesi oluşturmak için

1. **Çözüm Gezgini**, **AdventureWorksDataSet** çözümüne sağ tıklayın, **Ekle**' nin üzerine gelin ve ardından **Yeni proje**' ye tıklayın.

2. Şablonlar bölmesinde,  **C# Visual** veya **Visual Basic**öğesini genişletin ve ardından **Office**' i genişletin.

3. Genişletilmiş **Office** düğümü altında **2010** düğümünü seçin.

4. Proje şablonları listesinde, Excel çalışma kitabı projesini seçin.

5. **Ad** kutusuna **AdventureWorksReport**yazın. Konumu değiştirmeyin.

6.           **Tamam**'ı tıklatın.

     **Office proje sihirbazı Visual Studio Araçları** açılır.

7. **Yeni bir belge oluştur** ' un seçili olduğundan emin olun ve **Tamam**' ı tıklatın.

     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]tasarımcıda **AdventureWorksReport** çalışma kitabını açar ve **Çözüm Gezgini** **AdventureWorksReport** projesini ekler.

## <a name="add-the-dataset-to-data-sources-in-the-excel-workbook-project"></a>Veri kümesini Excel çalışma kitabı projesindeki veri kaynaklarına ekleme
 Veri kümesini Excel çalışma kitabında görüntüleyebilmeniz için önce Excel çalışma kitabı projesindeki veri kaynaklarına veri kümesini eklemeniz gerekir.

### <a name="to-add-the-dataset-to-the-data-sources-in-the-excel-workbook-project"></a>Veri kümesini Excel çalışma kitabı projesindeki veri kaynaklarına eklemek için

1. **Çözüm Gezgini**, **AdventureWorksReport** projesi altındaki **Sheet1.cs** veya **Sheet1. vb** öğesine çift tıklayın.

     Çalışma kitabı tasarımcıda açılır.

2. **Veri** menüsünde **Yeni veri kaynağı Ekle**' ye tıklayın.

     **Veri kaynağı Yapılandırma Sihirbazı** açılır.

3. **Nesne**' ye ve ardından **İleri**' ye tıklayın.

4. **Bağlamak Istediğiniz nesneyi seçin** sayfasında, **Başvuru Ekle**' ye tıklayın.

5. **Projeler** sekmesinde, **AdventureWorksDataSet** ' e ve ardından **Tamam**' a tıklayın.

6. **AdventureWorksDataSet** derlemesinin **AdventureWorksDataSet** ad alanı altında, **AdventureWorksLTDataSet** ' e ve ardından **son**' a tıklayın.

     **Veri kaynakları** penceresi açılır ve **AdventureWorksLTDataSet** veri kaynakları listesine eklenir.

## <a name="create-a-listobject-that-is-bound-to-an-instance-of-the-dataset"></a>Veri kümesinin örneğine bağlanan bir ListObject oluşturma
 Çalışma kitabında veri kümesini göstermek için bir veri kümesinin örneğine <xref:Microsoft.Office.Tools.Excel.ListObject> bağlanan bir oluşturun. Verilere yönelik bağlama denetimleri hakkında daha fazla bilgi için bkz. [Office çözümlerinde verileri denetimlere bağlama](../vsto/binding-data-to-controls-in-office-solutions.md).

### <a name="to-create-a-listobject-that-is-bound-to-an-instance-of-the-dataset"></a>Veri kümesinin bir örneğine bağlanan bir ListObject oluşturmak için

1. **Veri kaynakları** penceresinde, **AdventureWorksDataSet**altındaki **AdventureWorksLTDataSet** düğümünü genişletin.

2. **Ürün** düğümünü seçin, görüntülenen aşağı açılan oka tıklayın ve açılan listeden **ListObject** ' i seçin.

     Aşağı açılan ok görünmezse, çalışma kitabının tasarımcıda açık olduğunu onaylayın.

3. **Ürün** tablosunu a1 hücresine sürükleyin.

     Çalışma <xref:Microsoft.Office.Tools.Excel.ListObject> sayfasında a1 `productListObject` hücresinden başlayarak adlı bir denetim oluşturulur. Aynı zamanda, adlı `adventureWorksLTDataSet` <xref:System.Windows.Forms.BindingSource> ve `productBindingSource` adlı bir veri kümesi nesnesi projeye eklenir. <xref:Microsoft.Office.Tools.Excel.ListObject> , <xref:System.Windows.Forms.BindingSource>' A bağlanır ve veri kümesi nesnesine bağlanır.

## <a name="add-the-dataset-to-the-data-cache"></a>Veri kümesini veri önbelleğine ekleme
 Excel çalışma kitabı projesi dışındaki kodun çalışma kitabındaki veri kümesine erişmesini sağlamak için veri kümesini veri önbelleğine eklemeniz gerekir. Veri önbelleği hakkında daha fazla bilgi için bkz. [belge düzeyi özelleştirmelerde önbelleğe alınmış veriler](../vsto/cached-data-in-document-level-customizations.md) ve [Önbellek verileri](../vsto/caching-data.md).

### <a name="to-add-the-dataset-to-the-data-cache"></a>Veri kümesini veri önbelleğine eklemek için

1. Tasarımcıda **AdventureWorksLTDataSet**' e tıklayın.

2. **Özellikler** penceresinde **değiştiriciler** özelliğini **Public**olarak ayarlayın.

3. **CacheInDocument** özelliğini **true**olarak ayarlayın.

## <a name="initialize-the-dataset-in-the-workbook"></a>Çalışma kitabındaki veri kümesini başlatma
 Konsol uygulamasını kullanarak önbelleğe alınmış veri kümesinden verileri almak için önce önbelleğe alınmış veri kümesini verilerle doldurmanız gerekir.

### <a name="to-initialize-the-dataset-in-the-workbook"></a>Çalışma kitabında veri kümesini başlatmak için

1. **Çözüm Gezgini**, **Sheet1.cs** veya **Sheet1. vb** dosyasını sağ tıklayın ve **kodu görüntüle**' ye tıklayın.

2. `Sheet1_Startup` Olay işleyicisini aşağıdaki kodla değiştirin. Bu kod, şu anda boşsa, `ProductTableAdapter` verileri önbelleğe alınmış veri kümesini dolduracak şekilde, **AdventureWorksDataSet** projesinde tanımlanan sınıfının bir örneğini kullanır.

     [!code-csharp[Trin_CachedDataWalkthroughs#8](../vsto/codesnippet/CSharp/AdventureWorksDataSet/AdventureWorksReport/Sheet1.cs#8)]
     [!code-vb[Trin_CachedDataWalkthroughs#8](../vsto/codesnippet/VisualBasic/AdventureWorksDataSet/AdventureWorksReport/Sheet1.vb#8)]

## <a name="checkpoint"></a>Checkpoint
 Hatasız derlendiğinden ve çalıştığından emin olmak için Excel çalışma kitabı projesini derleyin ve çalıştırın. Bu işlem, önbelleğe alınmış veri kümesini de doldurur ve verileri çalışma kitabına kaydeder.

### <a name="to-build-and-run-the-project"></a>Projeyi derleyip çalıştırmak için

1. **Çözüm Gezgini**, **AdventureWorksReport** projesine sağ tıklayın, **Hata Ayıkla**' yı seçin ve ardından **Yeni örnek Başlat**' ı tıklatın.

     Proje oluşturulmuştur ve çalışma kitabı Excel 'de açılır. Aşağıdakileri doğrulayın:

    - Veriler <xref:Microsoft.Office.Tools.Excel.ListObject> ile doldurulur.

    - Öğesinin<xref:Microsoft.Office.Tools.Excel.ListObject> ilk satırı için **ListPrice** sütunundaki değer 1431,5 ' dir. Bu izlenecek yolda daha sonra, **ListPrice** sütunundaki değerleri değiştirmek için bir konsol uygulaması kullanacaksınız.

2. Çalışma kitabını kaydedin. Dosya adını veya çalışma kitabının konumunu değiştirmeyin.

3. Excel 'i kapatın.

## <a name="create-a-console-application-project"></a>Konsol uygulaması projesi oluşturma
 Çalışma kitabındaki önbelleğe alınmış veri kümesindeki verileri değiştirmek için kullanılacak bir konsol uygulaması projesi oluşturun.

### <a name="to-create-the-console-application-project"></a>Konsol uygulaması projesi oluşturmak için

1. **Çözüm Gezgini**, **AdventureWorksDataSet** çözümüne sağ tıklayın, **Ekle**' nin üzerine gelin ve ardından **Yeni proje**' ye tıklayın.

2. **Proje türleri** bölmesinde,  **C# Visual** veya **Visual Basic**öğesini genişletin ve ardından **Windows**' a tıklayın.

3. **Şablonlar** bölmesinde **konsol uygulaması**' nı seçin.

4. **Ad** kutusuna **DataWriter**yazın. Konumu değiştirmeyin.

5.           **Tamam**'ı tıklatın.

     [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]**DataWriter** projesini **Çözüm Gezgini** ekler ve **program.cs** veya **Module1. vb** kod dosyasını açar.

## <a name="change-data-in-the-cached-dataset-by-using-the-console-application"></a>Konsol uygulamasını kullanarak önbelleğe alınmış veri kümesindeki verileri değiştirme
 Verileri yerel`AdventureWorksLTDataSet` bir nesne içine okumak, bu verileri değiştirmek ve sonra önbelleğe alınmış veri kümesine geri kaydetmek için konsol uygulamasındaki sınıfınıkullanın.<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument>

### <a name="to-change-data-in-the-cached-dataset"></a>Önbelleğe alınmış veri kümesindeki verileri değiştirmek için

1. **Çözüm Gezgini**, **DataWriter** projesine sağ tıklayın ve **Başvuru Ekle**' ye tıklayın.

2. **.Net** sekmesinde, **Microsoft. VisualStudio. Tools. Applications**' ı seçin.

3.           **Tamam**'ı tıklatın.

4. **Çözüm Gezgini**, **DataWriter** projesine sağ tıklayın ve **Başvuru Ekle**' ye tıklayın.

5. **Projeler** sekmesinde, **AdventureWorksDataSet**' i seçin ve **Tamam**' ı tıklatın.

6. Kod düzenleyicisinde *program.cs* veya *Module1. vb* dosyasını açın.

7. Aşağıdaki **using** (for C#) veya **Imports** (for Visual Basic) ifadesini kod dosyasının en üstüne ekleyin.

    [!code-csharp[Trin_CachedDataWalkthroughs#1](../vsto/codesnippet/CSharp/AdventureWorksDataSet/DataWriter/Program.cs#1)]
    [!code-vb[Trin_CachedDataWalkthroughs#1](../vsto/codesnippet/VisualBasic/AdventureWorksDataSet/DataWriter/Module1.vb#1)]

8. `Main` Yöntemine aşağıdaki kodu ekleyin. Bu kod aşağıdaki nesneleri bildirir:

   - `AdventureWorksLTDataSet` **AdventureWorksDataSet** projesinde tanımlanan türün örneği.

   - **AdventureWorksReport** projesinin Build klasöründeki AdventureWorksReport çalışma kitabının yolu.

   - Çalışma kitabındaki veri önbelleğine erişmek için kullanılacak nesne.<xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument>

     > [!NOTE]
     > Aşağıdaki kod, *. xlsx* dosya uzantısına sahip bir çalışma kitabı kullandığınızı varsayar. Projenizdeki çalışma kitabının farklı bir dosya uzantısı varsa, yolu gereken şekilde değiştirin.

     [!code-csharp[Trin_CachedDataWalkthroughs#6](../vsto/codesnippet/CSharp/AdventureWorksDataSet/DataWriter/Program.cs#6)]
     [!code-vb[Trin_CachedDataWalkthroughs#6](../vsto/codesnippet/VisualBasic/AdventureWorksDataSet/DataWriter/Module1.vb#6)]

9. Önceki adımda eklediğiniz koddan sonra `Main` yöntemine aşağıdaki kodu ekleyin. Bu kod aşağıdaki görevleri gerçekleştirir:

   - Çalışma kitabındaki önbelleğe <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument.CachedData%2A> alınmış veri kümesine <xref:Microsoft.VisualStudio.Tools.Applications.ServerDocument> erişmek için sınıfının özelliğini kullanır.

   - Önbelleğe alınmış veri kümesindeki verileri yerel veri kümesine okur.

   - Veri kümesinin ürün `ListPrice` tablosundaki her ürünün değerini değiştirir.

   - Çalışma kitabındaki önbelleğe alınmış veri kümesine değişiklikleri kaydeder.

     [!code-csharp[Trin_CachedDataWalkthroughs#7](../vsto/codesnippet/CSharp/AdventureWorksDataSet/DataWriter/Program.cs#7)]
     [!code-vb[Trin_CachedDataWalkthroughs#7](../vsto/codesnippet/VisualBasic/AdventureWorksDataSet/DataWriter/Module1.vb#7)]

10. **Çözüm Gezgini**, **DataWriter** projesine sağ tıklayın, **Hata Ayıkla**' nın üzerine gelin ve ardından **Yeni örnek Başlat**' a tıklayın.

     Konsol uygulaması, önbelleğe alınmış veri kümesini yerel veri kümesine okurken iletileri görüntüler, yerel veri kümesindeki ürün fiyatlarını değiştirir ve yeni değerleri önbelleğe alınmış veri kümesine kaydeder. Uygulamayı kapatmak için **ENTER** tuşuna basın.

## <a name="test-the-workbook"></a>Çalışma kitabını test etme
 Çalışma kitabını <xref:Microsoft.Office.Tools.Excel.ListObject> açtığınızda, artık önbelleğe alınmış veri kümesindeki verilerin `ListPrice` sütununda yaptığınız değişiklikleri görüntüler.

### <a name="to-test-the-workbook"></a>Çalışma kitabını test etmek için

1. Hala açıksa, Visual Studio tasarımcısında AdventureWorksReport çalışma kitabını kapatın.

2. **AdventureWorksReport** projesinin Build klasöründeki AdventureWorksReport çalışma kitabını açın. Varsayılan olarak, derleme klasörü aşağıdaki konumlardan birinde bulunur:

    - *%USERPROFILE%\My Documents\AdventureWorksReport\bin\Debug* (Windows XP ve önceki sürümleri için)

    - *%Userprofile%\Documents\AdventureWorksReport\bin\Debug* (Windows Vista için)

3. Öğesinin<xref:Microsoft.Office.Tools.Excel.ListObject> ilk satırı için **ListPrice** sütunundaki değerin artık 1574,65 olduğunu doğrulayın.

4. Çalışma kitabını kapatın.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: Bir sunucudaki çalışma kitabına veri ekleme](../vsto/walkthrough-inserting-data-into-a-workbook-on-a-server.md)
