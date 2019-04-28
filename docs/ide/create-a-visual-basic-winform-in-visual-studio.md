---
title: Oluşturma bir Windows Forms uygulaması Visual Basic ile
description: Visual Basic, adım adım ile Visual Studio'da bir Windows Forms uygulaması oluşturmayı öğrenin.
ms.date: 03/23/2019
ms.topic: tutorial
ms.prod: visual-studio-windows
ms.technology: vs-ide-general
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- vb
ms.workload:
- multiple
ms.openlocfilehash: 4619a56bfe052a1fb191af8edfd1cef8b376617b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62976819"
---
# <a name="create-a-windows-forms-app-in-visual-studio-with-visual-basic"></a>Bir Windows oluşturma Visual Basic ile Visual Studio'da Forms uygulaması

Bu kısa giriş Visual Studio tümleşik geliştirme ortamı (IDE) için bir Windows tabanlı kullanıcı arabirimi (UI) olan basit bir Visual Basic uygulama oluşturacaksınız.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

> [!NOTE]
> Bu öğreticideki ekran görüntüleri bazıları, koyu tema kullanın. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](../ide/quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, Visual Basic uygulama projesi oluşturacaksınız. Proje türü bile herhangi bir şey ekledik önce ihtiyacınız olacak tüm şablon dosyaları ile birlikte gelir.

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **Visual Basic**ve ardından **Windows Masaüstü**. Orta bölmede seçin **Windows Forms uygulaması (.NET Framework)**. Dosya adı `HelloWorld`.

     Görmüyorsanız **Windows Forms uygulaması (.NET Framework)** proje şablonu, / İptal **yeni proje** iletişim kutusu ve üst menü çubuğundan seçin **Araçları**  >  **Araçları ve özellikleri Al**. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET masaüstü geliştirme** iş yükü, ardından **Değiştir**.

     ![Visual Studio Yükleyicisi'nde .NET core iş yükü](../ide/media/install-dot-net-desktop-env.png)

::: moniker-end

::: moniker range="vs-2019"

1. Open Visual Studio 2019.

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

   !['Yeni Proje oluştur' penceresini görüntüleyin](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. Üzerinde **yeni bir proje oluşturma** penceresinde girin veya yazın *Windows Forms* arama kutusuna. Ardından, **Visual Basic** dilden listeleyin ve ardından **Windows** Platform listesinde. 

   Tüm dil ve platform filtreleri uyguladıktan sonra seçin **Windows Forms uygulaması (.NET Framework)** şablonu seçip **sonraki**.

   ![Windows Forms uygulaması (.NET Framework) Visual Basic şablonu seçin](../get-started/visual-basic/media/vs-2019/vb-create-new-project-search-winforms-filtered.png)

   > [!NOTE]
   > Görmüyorsanız, **Windows Forms uygulaması (.NET Framework)** şablon yükleyebileceğiniz buradan **yeni bir proje oluşturma** penceresi. İçinde **aradığınızı bulamadınız?** message öğesini **daha fazla araçları ve özellikleri yükleme** bağlantı.
   >
   > !['Daha fazla araçları ve özellikleri yükleme' bağlantı 'Yeni Proje oluştur' penceresinde 'aradığınızı bulma yok' iletisi](../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Ardından, Visual Studio yükleyicisinde seçin seçin **.NET Masaüstü geliştirmesinden** iş yükü.
   > 
   > ![Visual Studio Yükleyicisi'nde .NET core iş yükü](../ide/media/install-dot-net-desktop-env.png)
   >
   > Bundan sonra seçin **Değiştir** Visual Studio Yükleyicisi'nde düğmesi. Çalışmanızı kaydetmek için istenebilir; Bu durumda, bunu yapın. Ardından, **devam** iş yükünü yüklemek için. Ardından, 2. adım bu dönün "[proje oluşturma](#create-a-project)" yordamı.

1. İçinde **yeni projenizi yapılandırın** penceresinde yazın veya girin *HelloWorld* içinde **proje adı** kutusu. Ardından, **Oluştur**.

   !['yeni projenizi yapılandırın' penceresinde 'HelloWorld' projenizi adlandırın](../get-started/visual-basic/media/vs-2019/vb-name-your-winform-project-helloworld.png)

   Yeni projeniz Visual Studio açılır.

::: moniker-end

## <a name="create-the-application"></a>Uygulama oluşturma

Visual Basic projesi şablonu seçin ve dosyanızın adı sonra Visual Studio sizin için bir form açılır. Bir Windows kullanıcı arabirimi biçimidir. "Hello World" uygulaması formu için denetimler ekleyerek oluşturacağız ve ardından size uygulamayı çalıştıracaksınız.

### <a name="add-a-button-to-the-form"></a>Forma bir düğme ekleyin

1. Tıklayın **araç kutusu** araç kutusu çıkış penceresini açmak için.

     ![Araç araç kutusu penceresini açmak için tıklayın](../ide/media/vb-toolbox-toolwindow.png)

     (Görmüyorsanız **araç kutusu** çıkış seçeneği tuşlarına basarak açabilirsiniz **Ctrl**+**Alt**+**X**.)

2. Tıklayın **PIN** simgesini yerleştirmek için **araç kutusu** penceresi.

     ![Araç kutusu penceresini IDE sabitlemek için Raptiye simgesine tıklayın](../ide/media/vb-pin-the-toolbox-window.png)

3. Tıklayın **düğmesi** denetlemek ve ardından form üzerine sürükleyin.

     ![Forma bir düğme ekleyin](../ide/media/vb-add-a-button-to-form1.png)

4. İçinde **Görünüm** bölüm (veya **yazı tipleri** bölümünde), **özellikleri** penceresinde, tür `Click this`ve tuşuna **Enter**.

     ![Düğmeyi form üzerinde metin ekleme](../ide/media/vb-button-control-text.png)

     (Görmüyorsanız **özellikleri** penceresinde açabilirsiniz, menü çubuğundan. Bunu yapmak için tıklatın **görünümü** > **Özellikler penceresi**. Veya basın **F4**.)

5. İçinde **tasarım** bölümünü **özellikleri** penceresinde adını değiştirmek **Button1** için `btnClickThis`ve tuşuna **Enter**.

     ![Düğmeyi form üzerinde bir işlev ekleme](../ide/media/vb-button-control-function.png)

### <a name="add-a-label-to-the-form"></a>Forma bir etiket ekleyin

Bir eylem oluşturmak için bir düğme denetimi ekledik, metni göndermek için bir etiket denetimi ekleyelim.

1. Seçin **etiket** denetimi **araç kutusu** pencere, form üzerine sürükleyin ve altındaki açılan **tıklatın** düğmesi.

2. İçinde **tasarım** bölümünü **özellikleri** penceresinde adını değiştirmek **Label1** için `lblHelloWorld`ve tuşuna **Enter**.

### <a name="add-code-to-the-form"></a>Forma kod ekleyin

1. İçinde **Form1.vb &#91;tasarım&#93;**  penceresinde çift **tıklatın** açmak için düğmeyi **Form1.vb** penceresi.

      (Alternatif olarak, genişletebilirsiniz **Form1.vb** içinde **Çözüm Gezgini**ve ardından **Form1**.)

2. İçinde **Form1.vb** penceresi, arasında **Private Sub** satır ve **End Sub** satır (veya arasında **Public Class Form1** satır ve  **End Class** satır), aşağıdaki kodu yazın.

     ![Forma kod ekleyin](../ide/media/vb-add-code-to-the-form.png)

## <a name="run-the-application"></a>Uygulamayı çalıştırın

1. Tıklayın **Başlat** uygulamayı çalıştırmak için düğme.

     ![Uygulamayı çalıştırıp hata ayıklama Başlat'a tıklayın](../ide/media/vb-click-start-hello-world.png)

   Birden fazla işlem gerçekleşir. Visual Studio IDE'de **tanılama araçları** penceresi açılır ve bir **çıkış** penceresi açılır, çok. Ancak IDE dışında bir **Form1** iletişim kutusu görüntülenir. Dahil edilir, **tıklatın** düğme ve metin bildiren **Label1**.

2. Tıklayın **tıklatın** düğmesine **Form1** iletişim kutusu. Dikkat **Label1** metin değişiklikleri **Merhaba Dünya!**.

    ![Label1 metin içeren bir Form1 iletişim kutusu ](../ide/media/vb-form1-dialog-hello-world.png)

Bu hızlı başlangıcı tamamladığınızda Tebrikler! Visual Basic ve Visual Studio IDE hakkında biraz öğrenilen umuyoruz. Daha kapsamlı anlamak için delve istiyorsanız, Lütfen bir öğreticide ile devam **öğreticiler** İçindekiler bölümünde.

## <a name="see-also"></a>Ayrıca bkz.

* [Hızlı Başlangıç: Visual Basic ile Visual Studio'da konsol uygulaması oluşturma](quickstart-visual-basic-console.md)
* [Visual Basic IntelliSense hakkında daha fazla bilgi edinin](visual-basic-specific-intellisense.md)
