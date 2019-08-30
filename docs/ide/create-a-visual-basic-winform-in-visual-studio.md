---
title: Visual Basic Windows Forms uygulama oluşturma
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
ms.openlocfilehash: c031a047a0331eea0f8397a303d2b5cb0af650e6
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180139"
---
# <a name="create-a-windows-forms-app-in-visual-studio-with-visual-basic"></a>Bir Windows oluşturma Visual Basic ile Visual Studio'da Forms uygulaması

Bu kısa giriş Visual Studio tümleşik geliştirme ortamı (IDE) için bir Windows tabanlı kullanıcı arabirimi (UI) olan basit bir Visual Basic uygulama oluşturacaksınız.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

> [!NOTE]
> Bu öğreticideki ekran görüntülerinin bazıları koyu temayı kullanır. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](../ide/quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, Visual Basic uygulama projesi oluşturacaksınız. Proje türü bile herhangi bir şey ekledik önce ihtiyacınız olacak tüm şablon dosyaları ile birlikte gelir.

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan **Dosya** > **Yeni** > **Proje**' yi seçin.

3. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **Visual Basic**ve ardından **Windows Masaüstü**. Orta bölmede seçin **Windows Forms uygulaması (.NET Framework)** . Dosya adı `HelloWorld`.

     Görmüyorsanız **Windows Forms uygulaması (.NET Framework)** proje şablonu, / İptal **yeni proje** iletişim kutusu ve üst menü çubuğundan seçin **Araçları**  >  **Araçları ve özellikleri Al**. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET masaüstü geliştirme** iş yükü, ardından **Değiştir**.

     ![Visual Studio Yükleyicisi'nde .NET core iş yükü](../ide/media/install-dot-net-desktop-env.png)

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio 2019 ' i açın.

1. Başlangıç penceresinde **Yeni proje oluştur**' u seçin.

   ![' Yeni proje oluştur ' penceresini görüntüleyin](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. **Yeni proje oluştur** penceresinde, arama kutusuna *Windows Forms* girin veya yazın. Ardından, dil listesinden **Visual Basic** ' yi seçin ve ardından platform listesinden **Windows** ' u seçin. 

   Dil ve platform filtrelerini uyguladıktan sonra **Windows Forms App (.NET Framework)** şablonunu seçin ve ardından **İleri**' yi seçin.

   ![Windows Forms uygulaması için Visual Basic şablonu seçin (.NET Framework)](../get-started/visual-basic/media/vs-2019/vb-create-new-project-search-winforms-filtered.png)

   > [!NOTE]
   > **Windows Forms App (.NET Framework)** şablonunu görmüyorsanız, **Yeni proje oluştur** penceresinden yükleyebilirsiniz. **Aradığınızı bulamıyor musunuz?** iletisi için **daha fazla araç ve özellik yüklemeyi** seçin bağlantısına tıklayın.
   >
   > ![' Yeni proje oluştur ' penceresindeki ' daha fazla araç ve özellik yüklemesi ' ' ne aradığınızı bulma ' iletisi bağlantısı](../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Sonra, Visual Studio Yükleyicisi **.net masaüstü geliştirme** Iş yükünü seçin.
   > 
   > ![Visual Studio Yükleyicisi'nde .NET core iş yükü](../ide/media/install-dot-net-desktop-env.png)
   >
   > Bundan sonra Visual Studio Yükleyicisi **Değiştir** düğmesini seçin. İşinizi kaydetmeniz istenebilir; Öyleyse, bunu yapın. Sonra, iş yükünü yüklemek için **devam** ' ı seçin. Ardından, bu "[Proje oluşturma](#create-a-project)" yordamında 2. adıma geri dönün.

1. **Yeni projeyi yapılandırın** penceresinde, **Proje adı** kutusuna *HelloWorld* yazın veya girin. Ardından **Oluştur**' u seçin.

   ![' yeni projenizi yapılandırın ' penceresinde, projenizi ' HelloWorld ' olarak adlandırın](../get-started/visual-basic/media/vs-2019/vb-name-your-winform-project-helloworld.png)

   Visual Studio yeni projenizi açar.

::: moniker-end

## <a name="create-the-application"></a>Uygulama oluşturma

Visual Basic projesi şablonu seçin ve dosyanızın adı sonra Visual Studio sizin için bir form açılır. Bir Windows kullanıcı arabirimi biçimidir. "Hello World" uygulaması formu için denetimler ekleyerek oluşturacağız ve ardından size uygulamayı çalıştıracaksınız.

### <a name="add-a-button-to-the-form"></a>Forma bir düğme ekleyin

1. Tıklayın **araç kutusu** araç kutusu çıkış penceresini açmak için.

     ![Araç araç kutusu penceresini açmak için tıklayın](../ide/media/vb-toolbox-toolwindow.png)

     ( **Araç kutusu** açılır seçeneğini görmüyorsanız, **CTRL**+**alt**+**X**tuşlarına basarak açabilirsiniz.)

2. Tıklayın **PIN** simgesini yerleştirmek için **araç kutusu** penceresi.

     ![Araç kutusu penceresini IDE sabitlemek için Raptiye simgesine tıklayın](../ide/media/vb-pin-the-toolbox-window.png)

3. Tıklayın **düğmesi** denetlemek ve ardından form üzerine sürükleyin.

     ![Forma bir düğme ekleyin](../ide/media/vb-add-a-button-to-form1.png)

4. **Özellikler** `Click this`penceresinin **Görünüm** bölümünde (veya **Fonts** bölümünde), yazın ve ardından **ENTER**tuşuna basın.

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

2. **Form1. vb** penceresinde, **özel alt** çizgi ile **bitiş alt** çizgisi arasında (veya **ortak sınıf Form1** çizgisi ile **bitiş sınıfı** satırı arasında) aşağıdaki kodu yazın.

     ![Forma kod ekleyin](../ide/media/vb-add-code-to-the-form.png)

## <a name="run-the-application"></a>Uygulamayı çalıştırın

1. Tıklayın **Başlat** uygulamayı çalıştırmak için düğme.

     ![Uygulamayı çalıştırıp hata ayıklama Başlat'a tıklayın](../ide/media/vb-click-start-hello-world.png)

   Birden fazla işlem gerçekleşir. Visual Studio IDE'de **tanılama araçları** penceresi açılır ve bir **çıkış** penceresi açılır, çok. Ancak IDE dışında bir **Form1** iletişim kutusu görüntülenir. Dahil edilir, **tıklatın** düğme ve metin bildiren **Label1**.

2. Tıklayın **tıklatın** düğmesine **Form1** iletişim kutusu. Dikkat **Label1** metin değişiklikleri **Merhaba Dünya!** .

    ![Label1 metin içeren bir Form1 iletişim kutusu ](../ide/media/vb-form1-dialog-hello-world.png)

Bu hızlı başlangıcı tamamladığınızda Tebrikler! Visual Basic ve Visual Studio IDE hakkında biraz öğrenilen umuyoruz. Daha kapsamlı anlamak için delve istiyorsanız, Lütfen bir öğreticide ile devam **öğreticiler** İçindekiler bölümünde.

## <a name="see-also"></a>Ayrıca bkz.

* [Hızlı Başlangıç: Visual Basic ile Visual Studio 'da bir konsol uygulaması oluşturma](quickstart-visual-basic-console.md)
* [Visual Basic IntelliSense hakkında daha fazla bilgi edinin](visual-basic-specific-intellisense.md)
