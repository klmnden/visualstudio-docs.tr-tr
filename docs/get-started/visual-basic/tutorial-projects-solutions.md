---
title: Öğretici projeler ve çözümler Visual Basic
ms.date: 12/12/2018
ms.technology: vs-ide-general
ms.custom: get-started
ms.topic: tutorial
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 8931e16751355a7f25c9ab88dbcd554bc7cb0ea7
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59664459"
---
# <a name="learn-about-projects-and-solutions-using-visual-basic"></a>Projeleri ve Visual Basic kullanan çözümler hakkında bilgi edinin

Giriş niteliğindeki bu makalede şunları oluşturma ne demek keşfedeceğiz bir *çözüm* ve *proje* Visual Studio'da. Kod projeleri, örneğin bir sınıf kitaplığı projesi ve karşılık gelen bir test projesi ilgili daha fazla ya da bir çözüm, bir düzenlemek için kullanılan bir kapsayıcıdır. Bir proje özelliklerini ve bazı içerebileceği dosyalara göz atacağız. Ayrıca bir başvuru bir projeden diğerine oluşturacağız.

::: moniker range="vs-2017"

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

Bir proje kavramı anlamak için eğitim bir alıştırma olarak size bir çözüm ve proje sıfırdan oluşturmak. Visual Studio içinde genel kullanımı, büyük olasılıkla çeşitli proje bazılarını kullanacaksınız *şablonları* yeni bir proje oluşturduğunuzda, Visual Studio sunar.

> [!NOTE]
> Çözümler ve projeler, Visual Studio'da uygulama geliştirme gerekmez. Ayrıca, kod ve kodlama, derleme ve hata ayıklama başlangıç içeren bir klasör açabilirsiniz. Örneğin, kopyalama, bir [GitHub](https://github.com/) depo, Visual Studio projeleri ve çözümleri içermeyebilir. Daha fazla bilgi için [kod Visual Studio'da projeler veya çözümler olmadan geliştirme](../../ide/develop-code-in-visual-studio-without-projects-or-solutions.md).

## <a name="solutions-and-projects"></a>Projeler ve çözümler

Adını rağmen bir çözüm "yanıt" değildir. Bir çözüm sadece bir düzenlemek için Visual Studio tarafından kullanılan bir kapsayıcı ya da ilgili daha fazla proje. Visual Studio'da bir çözümü açtığınızda, çözüm içeren tüm projeleri otomatik olarak yükler.

### <a name="create-a-solution"></a>Bir çözüm oluşturun

Bizim araştırması boş bir çözüm oluşturarak başlayacağız. Visual Studio bilmek aldıktan sonra büyük olasılıkla çok sık boş çözüm oluşturduğunuzu bulamaz. Yeni bir proje oluşturduğunuzda, Visual Studio otomatik olarak değil bir çözüm zaten varsa açık proje barındırmak için bir çözüm oluşturur.

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

1. Menü çubuğunda, **dosya** > **yeni** > **proje**.

   **Yeni proje** iletişim kutusu açılır.

1. Sol bölmede genişletin **diğer proje türleri**, ardından **Visual Studio çözümleri**. Orta bölmede seçin **boş çözüm** şablonu. Çözümünüzü ad **QuickSolution**ve ardından **Tamam**.

   ![Visual Studio'da boş çözüm şablonu](../media/tutorial-projects-new-solution.png)

   **Başlangıç sayfası** kapatır ve çözüm görünür **Çözüm Gezgini** Visual Studio penceresinin sağ tarafındaki. Büyük olasılıkla kullanacağınız **Çözüm Gezgini** genellikle projelerinizi içeriğini gidin.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın.

2. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

3. Üzerinde **yeni bir proje oluşturun** want **boş çözüm** arama kutusuna seçin **boş çözüm** şablonu seçip **sonraki**.

4. Çözüm adı **QuickSolution**ve ardından **Oluştur**.

   Bir çözüm görünür **Çözüm Gezgini** Visual Studio penceresinin sağ tarafındaki. Büyük olasılıkla kullanacağınız **Çözüm Gezgini** genellikle projelerinizi içeriğini gidin.

::: moniker-end

### <a name="add-a-project"></a>Bir proje ekleyin

Artık ilk Projemizin çözüme ekleyelim. Biz ile boş bir proje başlatın ve ihtiyacımız öğe projeye ekleyin.

1. Sağ tıklayın veya bağlam menüsünde **çözüm 'QuickSolution'** içinde **Çözüm Gezgini**, seçin **Ekle** > **YeniProje**.

   **Yeni Proje Ekle** iletişim kutusu açılır.

1. Sol bölmede genişletin **Visual Basic** ve **Windows Masaüstü**. Orta bölmede seçin **boş proje (.NET Framework)** şablonu. Projeyi adlandırın **QuickDate**, ardından **Tamam** düğmesi.

   QuickDate adlı bir proje çözümde altında görünür **Çözüm Gezgini**. Şu anda tek dosya adlı içerdiği *App.config*.

   > [!NOTE]
   > Görmüyorsanız **Visual Basic** iletişim kutusunun sol bölmesinde yüklemeniz gerekir. **.NET masaüstü geliştirme** Visual Studio *iş yükü*. Visual Studio iş yükü tabanlı yükleme yalnızca bunu geliştirme türü için gereksinim duyduğunuz bileşenleri yüklemek için kullanır. Yeni bir iş yükünü yüklemek için kolay bir yolu seçmektir **açık Visual Studio yükleyicisi** sol alt köşesine bağlantıyı **Yeni Proje Ekle** iletişim kutusu. Visual Studio Yükleyicisi'ni başlattıktan sonra seçin **.NET masaüstü geliştirme** iş yükü ve ardından **Değiştir** düğmesi.

   ![Visual Studio yükleyicisi bağlantıyı aç](media/tutorial-projects-open-installer-vb.png)

## <a name="add-an-item-to-the-project"></a>Projeye bir öğe ekleyin

Boş bir proje sahibiz. Bir kod dosyası ekleyelim.

1. Sağ tıklayın veya bağlam menüsünde **QuickDate** projesi **Çözüm Gezgini**, seçin **Ekle** > **yeni öğe** .

   **Yeni Öğe Ekle** iletişim kutusu açılır.

1. Genişletin **ortak öğeler**, ardından **kod**. Orta bölmede seçin **sınıfı** öğe şablonu. Sınıf adı **Takvim**ve ardından **Ekle** düğmesi.

   Adlı bir dosya *Calendar.vb* projeye eklenir. *.Vb* uçta Visual Basic kod dosyasına verilen dosya uzantısıdır. Dosya visual proje hiyerarşisinde görünür **Çözüm Gezgini**, ve içeriğinin Düzenleyicisi'nde açın.

1. Öğesinin içeriğini değiştirin *Calendar.vb* dosyasındaki kodu aşağıdaki kodla:

   ```vb
   Class Calendar
       Public Shared Function GetCurrentDate() As Date
           Return DateTime.Now.Date
       End Function
   End Class
   ```

   `Calendar` Sınıfı içeren tek bir işlev `GetCurrentDate`, geçerli tarihi döndürür.

1. Çift tıklayarak proje özelliklerini açın **Projem** içinde **Çözüm Gezgini**. Üzerinde **uygulama** sekmesinde, **uygulama türü** için **sınıf kitaplığı**. Projeyi başarıyla oluşturmak Bu adım gereklidir.

1. Sağ tıklayarak projeyi derleyin **QuickDate** içinde **Çözüm Gezgini** seçip **yapı**. İçinde bir derleme başarılı iletisini görmeniz gerekir **çıkış** penceresi.

## <a name="add-a-second-project"></a>İkinci bir proje ekleyin

Birden fazla proje içeren çözümler için ortaktır ve genellikle bu projeler birbirine başvuru. Çözümdeki bazı projeler sınıf kitaplıkları, yürütülebilir bazı uygulamalar olabilir ve bazı Birim testi projelerini veya Web sitesi olabilir.

Birim testi projesi, çözüm ekleyelim. Biz bir ek kod dosyası projeye eklemek zorunda kalmamak için bu kez proje şablonundan başlayacağız.

1. Sağ tıklayın veya bağlam menüsünde **çözüm 'QuickSolution'** içinde **Çözüm Gezgini**, seçin **Ekle** > **YeniProje**.

   **Yeni Proje Ekle** iletişim kutusu açılır.

1. Sol bölmede genişletin **Visual Basic** ve **Test** kategorisi. Orta bölmede seçin **birim testi projesi (.NET Framework)** proje şablonu. Projeyi adlandırın **QuickTest**ve ardından **Tamam** düğmesi.

   İkinci bir proje eklenir **Çözüm Gezgini**ve adlı bir dosya *UnitTest1.vb* düzenleyicisinde açılır.

   ![İki proje ile Visual Studio Çözüm Gezgini](media/tutorial-projects-solution-explorer-vb.png)

## <a name="add-a-project-reference"></a>Bir proje başvurusu Ekle

Yeni birim test projesi bizim yöntemi test etmek için kullanılacak yapacağız **QuickDate** proje Biz bu projeye bir başvuru eklemeniz gerekir. Bu oluşturur bir *derleme bağımlılığı* çözümü oluşturduğunuzda iki projeler arasında güncelleştirmeyeceği **QuickDate** önce oluşturulan **QuickTest**.

1. Seçin **başvuruları** düğümünde **QuickTest** proje ve seçin sağ tıklayın veya bağlam menüsünden **Başvuru Ekle**.

   ![Başvuru menü ekleme](media/tutorial-projects-add-reference-vb.png)

   **Başvuru Yöneticisi** iletişim kutusu açılır.

1. Sol bölmede genişletin **projeleri** ve **çözüm**. Orta bölmede yanındaki onay kutusunu seçin **QuickDate**ve ardından **Tamam** düğmesi.

   Bir başvuru **QuickDate** projesi eklenir.

## <a name="add-test-code"></a>Test kodu ekleyin

1. Visual Basic kod dosyasına test kodu artık ekleyeceğiz. Öğesinin içeriğini değiştirin *UnitTest1.vb* aşağıdaki kod ile.

   ```vb
   <TestClass()> Public Class UnitTest1

       <TestMethod()> Public Sub TestGetCurrentDate()
           Assert.AreEqual(Date.Now.Date, QuickDate.Calendar.GetCurrentDate())
       End Sub

   End Class
   ```

   "Dalgalı" bazı kodları altında kırmızı bir görürsünüz. Bu hatayı test projesini yaparak gidereceğiz bir [arkadaş derleme](/dotnet/visual-basic/programming-guide/concepts/assemblies-gac/friend-assemblies) için **QuickDate** proje.

1. Geri **QuickDate** projesini açarsanız *Calendar.vb* zaten açık değilse dosyasını bulun ve aşağıdakileri ekleyin [Imports deyimi](/dotnet/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type) ve <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> çok özniteliği test projesi hatayı çözümleyin.

   ```vb
   Imports System.Runtime.CompilerServices

   <Assembly: InternalsVisibleTo("QuickTest")>
   ```

   Kod dosyası şu şekilde görünmelidir:

   ![Visual Basic kodu](media/tutorial-projects-code-vb.png)

## <a name="project-properties"></a>Proje Özellikleri

Satırda *Calendar.vb* içeren dosya <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute> özniteliği derleme adını (dosya adı) başvuruda **QuickTest** proje. Proje adı ile aynı derleme adı her zaman olmayabilir. Proje derleme adını bulmak için proje özelliklerini açın.

1. İçinde **Çözüm Gezgini**seçin **QuickTest** proje. Sağ tıklayın veya bağlam menüsünü seçin **özellikleri**, veya tuşuna basarak **Alt**+**Enter**. (Ayrıca çift **Projem** içinde **Çözüm Gezgini**.)

   *Özellik sayfaları* üzerinde açık proje için **uygulama** sekmesi. Özellik sayfaları, proje için çeşitli ayarları içerir. Dikkat derleme adını **QuickTest** projedir gerçekten "QuickTest". Bunu değiştirmek istiyorsanız, burada yaptığınız budur. Test projesi oluşturduğunuzda, daha sonra elde edilen ikili dosyasının adı gelen değiştirirsiniz *QuickTest.dll* , seçtiğiniz için.

   ![Proje Özellikleri](../media/tutorial-projects-properties.png)

1. Projenin özellik sayfalarındaki, diğer sekmelerdeki gibi keşfedebilirsiniz **derleme** ve **ayarları**. Bu sekme, farklı proje türleri için farklıdır.

## <a name="optional-run-the-test"></a>(İsteğe bağlı) Testi çalıştırın

Birim testinizi çalıştığını denetlemek istiyorsanız seçin **Test** > **çalıştırma** > **tüm testleri** menü çubuğundan. Bir pencere olarak adlandırılan **Test Gezgini** açar, görmelisiniz, **TestGetCurrentDate** test geçer.

![Visual Studio geçirilen gösteren metin Gezgini'nde test](../media/tutorial-projects-test-explorer.png)

> [!TIP]
> Varsa **Test Gezgini** değil, otomatik olarak Aç seçerek açın **Test** > **Windows** > **TestGezgini** menü çubuğundan.

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio daha fazla araştırmak istiyorsanız, birini izleyerek bir uygulama oluşturmayı göz önünde bulundurun [Visual Basic öğreticiler](index.yml).

## <a name="see-also"></a>Ayrıca bkz.

- [Projeler ve çözümler oluşturma](../../ide/creating-solutions-and-projects.md)
- [Proje ve çözüm özelliklerini yönetme](../../ide/managing-project-and-solution-properties.md)
- [Bir projedeki başvuruları yönetme](../../ide/managing-references-in-a-project.md)
- [Visual Studio’da projeler veya çözümler olmadan kod geliştirme](../../ide/develop-code-in-visual-studio-without-projects-or-solutions.md)
- [Visual Studio IDE'ye genel bakış](../../get-started/visual-studio-ide.md)