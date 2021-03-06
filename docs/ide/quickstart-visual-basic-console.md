---
title: Visual Basic ile ilk konsol uygulamanızı oluşturma
description: Visual Studio 'da Visual Basic, adım adım ile basit bir Merhaba Dünya konsol uygulaması oluşturmayı öğrenin.
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
ms.openlocfilehash: c7da73ac3f47b6b63817ff905923b71e3354b06c
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180087"
---
# <a name="quickstart-create-your-first-console-app-in-visual-studio-with-visual-basic"></a>Hızlı Başlangıç: Visual Basic ile Visual Studio 'da ilk konsol uygulamanızı oluşturma

Visual Studio tümleşik geliştirme ortamına (IDE) bu 5-10 dakikalık bir giriş içinde, konsolunda çalışan basit bir Visual Basic uygulaması oluşturacaksınız.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, Visual Basic uygulama projesi oluşturacaksınız. Proje türü, ihtiyacınız olan tüm şablon dosyaları ile birlikte gelir, hatta herhangi bir şey eklemeden önce!

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan **Dosya** > **Yeni** > **Proje**' yi seçin.

3. Sol bölmedeki **Yeni proje** iletişim kutusunda **Visual Basic**' ı genişletin ve ardından **.NET Core**' u seçin. Orta bölmede **konsol uygulaması (.NET Core)** öğesini seçin. Ardından projeyi *HelloWorld*olarak adlandırın.

   ![Visual Studio IDE 'de yeni proje iletişim kutusundaki konsol uygulaması (.NET Core) proje şablonu](../ide/media/new-project-vb-dotnetcore-helloworld-console-app.png)

     **Konsol uygulaması (.NET Core)** proje şablonunu görmüyorsanız, **Yeni proje** Iletişim kutusunun sol bölmesindeki **Aç Visual Studio yükleyicisi** bağlantısına tıklayın.

   ![Yeni proje iletişim kutusundan Visual Studio Yükleyicisi aç bağlantısına tıklayın](../ide/media/vb-open-visual-studio-installer-hello-world.png)

     Visual Studio Yükleyicisi'ni başlatır. **.NET Core platformlar arası geliştirme** iş yükünü seçin ve ardından **Değiştir**' i seçin.

     ![Visual Studio Yükleyicisi .NET Core platformlar arası geliştirme iş yükü](../ide/media/dot-net-core-xplat-dev-workload.png)

::: moniker-end

::: moniker range="vs-2019"

> [!NOTE]
> Bu hızlı başlangıçtaki ekran görüntüleri koyu temasını kullanır. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

1. Visual Studio 2019 ' i açın.

1. Başlangıç penceresinde **Yeni proje oluştur**' u seçin.

   ![' Yeni proje oluştur ' penceresini görüntüleyin](../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. **Yeni proje oluştur** penceresinde, arama kutusuna *konsol* girin veya yazın. Ardından, dil listesinden **Visual Basic** ' yi seçin ve ardından platform listesinden **Windows** ' u seçin. 

   Dil ve platform filtrelerini uyguladıktan sonra **konsol uygulaması (.NET Core)** şablonunu seçin ve ardından **İleri**' yi seçin.

   ![Konsol uygulaması için Visual Basic şablonu seçin (.NET Framework)](../get-started/visual-basic/media/vs-2019/vb-create-new-project-search-console-net-core-filtered.png)

   > [!NOTE]
   > **Konsol uygulaması (.NET Core)** şablonunu görmüyorsanız, **Yeni proje oluştur** penceresinden yükleyebilirsiniz. **Aradığınızı bulamıyor musunuz?** iletisi için **daha fazla araç ve özellik yüklemeyi** seçin bağlantısına tıklayın.
   >
   > ![' Yeni proje oluştur ' penceresindeki ' daha fazla araç ve özellik yüklemesi ' ' ne aradığınızı bulma ' iletisi bağlantısı](../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Sonra, Visual Studio Yükleyicisi **.NET Core platformlar arası geliştirme** iş yükünü seçin.
   >
   > ![Visual Studio Yükleyicisi .NET Core platformlar arası geliştirme iş yükü](../get-started/media/dot-net-core-xplat-dev-workload.png)
   >
   > Bundan sonra Visual Studio Yükleyicisi **Değiştir** düğmesini seçin. İşinizi kaydetmeniz istenebilir; Öyleyse, bunu yapın. Sonra, iş yükünü yüklemek için **devam** ' ı seçin. Ardından, bu "[Proje oluşturma](#create-a-project)" yordamında 2. adıma geri dönün.

1. **Yeni projeyi yapılandırın** penceresinde, **Proje adı** kutusuna *WhatIsYourName* yazın veya girin. Ardından **Oluştur**' u seçin.

   ![' yeni projenizi yapılandırın ' penceresinde, ' WhatIsYourName ' projenizi adlandırın](../get-started/visual-basic/media/vs-2019/vb-name-your-project-whatname.png)

   Visual Studio yeni projenizi açar.

::: moniker-end

## <a name="create-the-application"></a>Uygulama oluşturma

Visual Basic proje şablonunuzu seçip projenizi adlandırın, Visual Studio sizin için basit bir "Merhaba Dünya" uygulaması oluşturur. "Merhaba Dünya! <xref:System.Console.WriteLine%2A> " değişmez dizesini göstermek için yöntemini çağırır Konsol penceresinde.

![Şablondan varsayılan Merhaba Dünya kodunu görüntüleme](../ide/media/vb-console-helloworld-template.png)

IDE 'deki **HelloWorld** düğmesine tıklarsanız, programı hata ayıklama modunda çalıştırabilirsiniz.

  ![Programı hata ayıklama modunda çalıştırmak için Merhaba Dünya düğmesine tıklayın](../ide/media/vb-console-hello-world-button.png)

Bunu yaptığınızda, konsol penceresi kapanmadan önce yalnızca bir süre görünür olur. Bu durum, `Main` yöntemi tek ifadesinin yürütüldükten sonra sonlandırdığı ve bu nedenle uygulamanın sona ermesidir.

### <a name="add-some-code"></a>Kod ekleme

Uygulamayı duraklatmak için bazı kodlar ekleyelim ve sonra Kullanıcı girişi soralım.

1. <xref:System.Console.WriteLine%2A> Yöntemine yapılan çağrıdan hemen sonra aşağıdaki kodu ekleyin:

   ```vb
   Console.Write("Press any key to continue...")
   Console.ReadKey(true)
   ```

    Bu, bir tuşa basarak programı duraklatır.

2. Menü çubuğunda Build**Build Solution**öğesini > seçin.

   Bu, programınızı bir tam zamanında (JıT) derleyicisi tarafından ikili koda dönüştürülen bir ara dile (IL) derler.

## <a name="run-the-application"></a>Uygulamayı çalıştırma

1. Araç çubuğundaki **HelloWorld** düğmesine tıklayın.

   ![Programı araç çubuğundan çalıştırmak için Merhaba Dünya düğmesine tıklayın](../ide/media/vb-console-hello-world-button.png)

2. Konsol penceresini kapatmak için herhangi bir tuşa basın.

   ![Merhaba Dünya gösteren konsol penceresi ve devam etmek için herhangi bir tuşa basın](../ide/media/vb-console-hello-world-press-any-key.png)

## <a name="next-steps"></a>Sonraki adımlar

Bu hızlı başlangıcı tamamladığınızda Tebrikler! Visual Basic ve Visual Studio IDE hakkında biraz öğrenilen umuyoruz. Daha fazla bilgi edinmek için aşağıdaki öğreticiye geçin.

> [!div class="nextstepaction"]
> [Visual Studio 'da Visual Basic kullanmaya başlama](../get-started/visual-basic/tutorial-console.md)
