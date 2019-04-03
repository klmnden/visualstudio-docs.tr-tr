---
title: İlk Konsol uygulamanızı Visual Basic ile oluşturma
description: Visual Basic, adım adım ile Visual Studio'da basit bir Hello World konsol uygulaması oluşturmayı öğrenin.
ms.custom: seodec18
ms.date: 03/23/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
ms.topic: quickstart
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- vb
ms.workload:
- multiple
ms.openlocfilehash: d0ccaf648d4109679b7d1343df462ae4e8da3822
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58856249"
---
# <a name="quickstart-create-your-first-console-app-in-visual-studio-with-visual-basic"></a>Hızlı Başlangıç: Visual Basic ile Visual Studio'da ilk Konsol uygulamanızı oluşturma

Bu 5-10 dakikalık bir giriş Visual Studio tümleşik geliştirme ortamı (IDE), konsolda çalışan basit bir Visual Basic uygulaması oluşturacaksınız.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, Visual Basic uygulama projesi oluşturacaksınız. Proje türü bile herhangi bir şey ekledik önce ihtiyacınız olacak tüm şablon dosyaları ile birlikte gelir!

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **Visual Basic**ve ardından **.NET Core**. Orta bölmede seçin **konsol uygulaması (.NET Core)**. Ardından Projeyi adlandırın *HelloWorld*.

   ![Konsol uygulaması (.NET Core) proje şablonunu yeni proje iletişim kutusunda Visual Studio IDE](../ide/media/new-project-vb-dotnetcore-helloworld-console-app.png)

     Görmüyorsanız **konsol uygulaması (.NET Core)** proje şablonu, tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu.

   ![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantısına tıklayın](../ide/media/vb-open-visual-studio-installer-hello-world.png)

     Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

     ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../ide/media/dot-net-core-xplat-dev-workload.png)

::: moniker-end

::: moniker range="vs-2019"

> [!NOTE]
> Bu hızlı başlangıçta ekran görüntüleri bazıları, koyu tema kullanın. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

1. Open Visual Studio 2019.

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

   !['Yeni Proje oluştur' penceresini görüntüleyin](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. Üzerinde **yeni bir proje oluşturma** penceresinde girin veya yazın *konsol* arama kutusuna. Ardından, **Visual Basic** dilden listeleyin ve ardından **Windows** Platform listesinde. 

   Tüm dil ve platform filtreleri uyguladıktan sonra seçin **konsol uygulaması (.NET Core)** şablonu seçip **sonraki**.

   ![Konsol uygulaması (.NET Framework) için Visual Basic şablonu seçin](../get-started/visual-basic/media/vs-2019/vb-create-new-project-search-console-net-core-filtered.png)

   > [!NOTE]
   > Görmüyorsanız, **konsol uygulaması (.NET Core)** şablon yükleyebileceğiniz buradan **yeni bir proje oluşturma** penceresi. İçinde **aradığınızı bulamadınız?** message öğesini **daha fazla araçları ve özellikleri yükleme** bağlantı.
   >
   > !['Daha fazla araçları ve özellikleri yükleme' bağlantı 'Yeni Proje oluştur' penceresinde 'aradığınızı bulma yok' iletisi](../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Ardından, Visual Studio yükleyicisinde **.NET Core çoklu platform geliştirme** iş yükü.
   >
   > ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../get-started/media/dot-net-core-xplat-dev-workload.png)
   >
   > Bundan sonra seçin **Değiştir** Visual Studio Yükleyicisi'nde düğmesi. Çalışmanızı kaydetmek için istenebilir; Bu durumda, bunu yapın. Ardından, **devam** iş yükünü yüklemek için. Ardından, 2. adım bu dönün "[proje oluşturma](#create-a-project)" yordamı.

1. İçinde **yeni projenizi yapılandırın** penceresinde yazın veya girin *WhatIsYourName* içinde **proje adı** kutusu. Ardından, **Oluştur**.

   !['yeni projenizi yapılandırın' penceresinde 'WhatIsYourName' projenizi adlandırın](../get-started/visual-basic/media/vs-2019/vb-name-your-project-whatname.png)

   Yeni projeniz Visual Studio açılır.

::: moniker-end

## <a name="create-the-application"></a>Uygulama oluşturma

Visual Basic projesi şablonu seçin ve projenizi adlandırın sonra Visual Studio sizin için basit bir "Hello World" uygulaması oluşturur. Çağrı <xref:System.Console.WriteLine%2A> "Hello World!" sabit dizesini görüntülemek için yöntemi Konsol penceresinde.

![Şablondan varsayılan Merhaba Dünya kodu görüntüleme](../ide/media/vb-console-helloworld-template.png)

Tıklarsanız **HelloWorld** düğmesi IDE program hata ayıklama modunda çalıştırabilirsiniz.

  ![Programın hata ayıklama modunda çalıştırmak için Merhaba Dünya düğmesine tıklayın](../ide/media/vb-console-hello-world-button.png)

Bunu yaptığınızda, konsol penceresinde kapatılmadan önce yalnızca bir süre için görülebilir. Çünkü böyle `Main` yöntemi, tek bir deyim yürütüldükten sonra ve uygulama sona şekilde sonlandırır.

### <a name="add-some-code"></a>Kod ekleyin

Uygulamayı duraklatmak ve ardından kullanıcı girdisi isteyin biraz kod ekleyelim.

1. Çağırdıktan hemen sonra aşağıdaki kodu ekleyin <xref:System.Console.WriteLine%2A> yöntemi:

   ```vb
   Console.Write("Press any key to continue...")
   Console.ReadKey(true)
   ```

    Bir tuşa basın kadar bu program duraklatılır.

2. Menü çubuğunda, seçin **derleme** > **Çözümü Derle**.

   Bu, just-in-time (JIT) derleyici tarafından ikili koda dönüştürülür bir ara dile (IL) programınızı derler.

## <a name="run-the-application"></a>Uygulamayı çalıştırma

1. Tıklayın **HelloWorld** araç çubuğunda.

   ![Araç çubuğundan programı çalıştırmak için Merhaba Dünya düğmesine tıklayın](../ide/media/vb-console-hello-world-button.png)

2. Konsol penceresini kapatmak için herhangi bir tuşa basın.

   ![Konsol penceresinde Hello World gösteren ve devam etmek için herhangi bir tuşa basın](../ide/media/vb-console-hello-world-press-any-key.png)

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıcı tamamladığınızda Tebrikler! Visual Basic ve Visual Studio IDE hakkında biraz öğrenilen umuyoruz. Daha fazla bilgi için şu öğreticiyle devam edin.

> [!div class="nextstepaction"]
> [Visual Studio'da Visual Basic ile çalışmaya başlama](../get-started/visual-basic/tutorial-console.md)
