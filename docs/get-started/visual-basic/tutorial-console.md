---
title: 'Öğretici: Visual Basic ile çalışmaya başlama'
description: Visual Studio'da, adım adım Visual Basic konsol uygulamaları oluşturmayı öğrenin.
ms.custom: seodec18, get-started
ms.date: 03/23/2019
ms.technology: vs-ide-general
ms.prod: visual-studio-windows
ms.topic: tutorial
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: jillfra
dev_langs:
- vb
ms.workload:
- multiple
ms.openlocfilehash: 234a2d1070a39c0f9d9dbf5b0ae706b02b660abf
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59664966"
---
# <a name="tutorial-get-started-with-visual-basic-in-visual-studio"></a>Öğretici: Visual Studio'da Visual Basic ile çalışmaya başlama

Bu öğreticide Visual Basic (VB) oluşturmak ve birkaç farklı konsol uygulamaları çalıştırma ve bazı özellikleri incelemek için Visual Studio kullanacaksınız [Visual Studio tümleşik geliştirme ortamı (IDE)](visual-studio-ide.md) bunu yaparken.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

## <a name="create-a-project"></a>Proje oluşturma

İlk olarak, Visual Basic uygulama projesi oluşturacağız. Proje türü bile herhangi bir şey ekledik önce ihtiyacınız olacak tüm şablon dosyaları ile birlikte gelir!

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın.

2. Üstteki menü çubuğundan seçin **dosya** > **yeni** > **proje**.

3. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **Visual Basic**ve ardından **.NET Core**. Orta bölmede seçin **konsol uygulaması (.NET Core)**. Dosya adı *HelloWorld*.

   ![Konsol uygulaması (.NET Core) proje şablonunu yeni proje iletişim kutusunda Visual Studio IDE](media/new-project-vb-dotnetcore-whatisyourname-console-app.png)

### <a name="add-a-workload-optional"></a>(İsteğe bağlı) bir iş yükü Ekle

Görmüyorsanız **konsol uygulaması (.NET Core)** proje şablonu, alabilirsiniz, ekleyerek **.NET Core çoklu platform geliştirme** iş yükü. Bu iş yükü, makinenizde yüklü Visual Studio 2017 güncelleştirmeleri bağlı olarak iki aşağıdaki yollardan biriyle ekleyebilirsiniz.

#### <a name="option-1-use-the-new-project-dialog-box"></a>1. seçenek: Yeni Proje iletişim kutusunu kullanın

1. Tıklayın **açık Visual Studio yükleyicisi** sol bölmesinde bağlantıyı **yeni proje** iletişim kutusu.

   ![Yeni Proje iletişim kutusundan açık Visual Studio yükleyicisi bağlantısına tıklayın](../media/vs-open-visual-studio-installer-generic.png)

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

   ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../media/tutorial-aspnet-workload.png)

#### <a name="option-2-use-the-tools-menu-bar"></a>2. seçenek: Araçlar menü çubuğunu kullanın

1. / İptal **yeni proje** iletişim kutusu ve üst menü çubuğundan seçin **Araçları** > **araçları ve özellikleri Al**.

1. Visual Studio Yükleyicisi'ni başlatır. Seçin **.NET Core çoklu platform geliştirme** iş yükü ve ardından **Değiştir**.

::: moniker-end

::: moniker range="vs-2019"

> [!NOTE]
> Bu öğreticideki ekran görüntüleri bazıları, koyu tema kullanın. Koyu tema kullanmayan ancak öğrenmek istiyorsanız [Düzenleyicisi ve Visual Studio IDE'yi kişiselleştirme](../../ide/quickstart-personalize-the-ide.md) öğrenmek için sayfa nasıl.

1. Open Visual Studio 2019.

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**.

   !['Yeni Proje oluştur' penceresini görüntüleyin](../../get-started/media/vs-2019/create-new-project-dark-theme.png)

1. Üzerinde **yeni bir proje oluşturma** penceresinde girin veya yazın *konsol* arama kutusuna. Ardından, **Visual Basic** dilden listeleyin ve ardından **Windows** Platform listesinde. 

   Tüm dil ve platform filtreleri uyguladıktan sonra seçin **konsol uygulaması (.NET Core)** şablonu seçip **sonraki**.

   ![Konsol uygulaması (.NET Framework) için Visual Basic şablonu seçin](./media/vs-2019/vb-create-new-project-search-console-net-core-filtered.png)

   > [!NOTE]
   > Görmüyorsanız, **konsol uygulaması (.NET Core)** şablon yükleyebileceğiniz buradan **yeni bir proje oluşturma** penceresi. İçinde **aradığınızı bulamadınız?** message öğesini **daha fazla araçları ve özellikleri yükleme** bağlantı.
   >
   > !['Daha fazla araçları ve özellikleri yükleme' bağlantı 'Yeni Proje oluştur' penceresinde 'aradığınızı bulma yok' iletisi](../../get-started/media/vs-2019/not-finding-what-looking-for.png) 
   > 
   > Ardından, Visual Studio yükleyicisinde **.NET Core çoklu platform geliştirme** iş yükü.
   >
   > ![.NET core çoklu platform geliştirme iş yükünü Visual Studio yükleyicisi](../../get-started/media/dot-net-core-xplat-dev-workload.png)
   >
   > Bundan sonra seçin **Değiştir** Visual Studio Yükleyicisi'nde düğmesi. Çalışmanızı kaydetmek için istenebilir; Bu durumda, bunu yapın. Ardından, **devam** iş yükünü yüklemek için. Ardından, 2. adım bu dönün "[proje oluşturma](#create-a-project)" yordamı.

1. İçinde **yeni projenizi yapılandırın** penceresinde yazın veya girin *WhatIsYourName* içinde **proje adı** kutusu. Ardından, **Oluştur**.

   !['yeni projenizi yapılandırın' penceresinde 'WhatIsYourName' projenizi adlandırın](./media/vs-2019/vb-name-your-project-whatname.png)

   Yeni projeniz Visual Studio açılır.

::: moniker-end

## <a name="create-a-what-is-your-name-application"></a>"Ne olduğunu uygulamanızın adı" uygulaması oluşturma

Adınız için ister ve sonra tarih ve saat ile birlikte görüntüler bir uygulama oluşturalım. İşte nasıl:

 ::: moniker range="vs-2017"

1. Zaten açık değilse, ardından açın, *WhatIsYourName* proje.

1. Aşağıdaki Visual Basic kodu izleyen hemen ayraç sonra girin `Sub Main(args As String())` satır ve önce `End Sub` satırı:

     ```vb
     Console.WriteLine(vbCrLf + "What is your name? ")
     Dim name = Console.ReadLine()
     Dim currentDate = DateTime.Now
     Console.WriteLine($"{vbCrLf}Hello, {name}, on {currentDate:d} at {currentDate:t}")
     Console.Write(vbCrLf + "Press any key to exit... ")
     Console.ReadKey(True)
    ```

    Bu kodu varolan değiştirir <xref:System.Console.WriteLine%2A>, <xref:System.Console.Write%2A>, ve <xref:System.Console.ReadKey%2A> deyimleri.

   ![Ne olduğunu adınız kodu gösteren kod penceresi](./media/vs-2019/vb-codewindow-what-name-dark.png)

1. Konsol penceresi açıldığında, adınızı girin. Konsol penceresi aşağıdaki ekran görüntüsüne benzer görünmelidir:

   ![Konsol ne olduğunu uygulamanızın adı, saati ve tarihi gösteren penceresi ve ileti devam etmek için herhangi bir tuşa basın](media/vb-console-what-name.png)

1. Konsol penceresini kapatmak için herhangi bir tuşa basın.

::: moniker-end

::: moniker range="vs-2019"

1. İçinde *WhatIsYourName* projesi, şu Visual Basic kodu izleyen hemen ayraç sonra girin `Sub Main(args As String())` satır ve önce `End Sub` satırı:

     ```vb
     Console.WriteLine(vbCrLf + "What is your name? ")
     Dim name = Console.ReadLine()
     Dim currentDate = DateTime.Now
     Console.WriteLine($"{vbCrLf}Hello, {name}, on {currentDate:d} at {currentDate:t}")
     Console.Write(vbCrLf + "Press any key to exit... ")
     Console.ReadKey(True)
    ```

    Bu kodu varolan değiştirir <xref:System.Console.WriteLine%2A>, <xref:System.Console.Write%2A>, ve <xref:System.Console.ReadKey%2A> deyimleri.

   ![Ne olduğunu adınız kodu gösteren kod penceresi](./media/vs-2019/vb-codewindow-what-name-dark.png)

1. Konsol penceresi açıldığında, adınızı girin. Konsol penceresi aşağıdaki ekran görüntüsüne benzer görünmelidir:

   ![Konsol ne olduğunu uygulamanızın adı, saati ve tarihi gösteren penceresi ve ileti devam etmek için herhangi bir tuşa basın](media/vb-console-what-name.png)

1. Konsol penceresini kapatmak için herhangi bir tuşa basın.

 ::: moniker-end

## <a name="create-a-calculate-this-application"></a>"Bu Hesapla" bir uygulama oluşturma

::: moniker range="vs-2017"

1. Visual Studio 2017'yi açın ve ardından üstteki menü çubuğundan **dosya** > **yeni** > **proje**.

1. İçinde **yeni proje** iletişim kutusunun sol bölmesinde, **Visual Basic**ve ardından **.NET Core**. Orta bölmede seçin **konsol uygulaması (.NET Core)**. Dosya adı *CalculateThis*.

1. Arasına aşağıdaki kodu girin `Module Program` satır ve `End Module` satırı:

   ```vb
   Public num1 As Integer
   Public num2 As Integer
   Public answer As Integer
   Sub Main()
       Console.WriteLine("Type a number and press Enter")
       num1 = Console.ReadLine()
       Console.WriteLine("Type another number to add to it and press Enter")
       num2 = Console.ReadLine()
       answer = num1 + num2
       Console.WriteLine("The answer is " & answer)
       Console.ReadLine()
   End Sub
   ```

   Kod penceresi aşağıdaki ekran görüntüsüne benzer görünmelidir:

   ![CalculateThis kodu gösteren kod penceresi](media/vb-codewindow-calculate-this.png)

1. Tıklayın **CalculateThis** seçerek programınızı çalıştırın. Konsol penceresi aşağıdaki ekran görüntüsüne benzer görünmelidir:

    ![Konsol penceresi yönergeleri almak için hangi eylemleri içeren CalculateThis uygulama gösteriliyor.](media/vb-console-calculate-this.png)

::: moniker-end 

::: moniker range="vs-2019"

1. Pencerenin başlangıç seçin **yeni bir proje oluşturma**. 

1. Üzerinde **yeni bir proje oluşturma** penceresinde girin veya yazın *konsol* arama kutusuna. Ardından, **Visual Basic** dilden listeleyin ve ardından **Windows** Platform listesinde. 

1. Tüm dil ve platform filtreleri uyguladıktan sonra seçin **konsol uygulaması (.NET Core)** şablonu seçip **sonraki**.

   Ardından **yeni projenizi yapılandırın** penceresinde yazın veya girin *WhatIsYourName* içinde **proje adı** kutusu. Ardından, **Oluştur**.

1. Arasına aşağıdaki kodu girin `Module Program` satır ve `End Module` satırı:

   ```vb
   Public num1 As Integer
   Public num2 As Integer
   Public answer As Integer
   Sub Main()
       Console.WriteLine("Type a number and press Enter")
       num1 = Console.ReadLine()
       Console.WriteLine("Type another number to add to it and press Enter")
       num2 = Console.ReadLine()
       answer = num1 + num2
       Console.WriteLine("The answer is " & answer)
       Console.ReadLine()
   End Sub
   ```

   Kod penceresi aşağıdaki ekran görüntüsüne benzer görünmelidir:

   ![CalculateThis kodu gösteren kod penceresi](media/vb-codewindow-calculate-this.png)

1. Tıklayın **CalculateThis** seçerek programınızı çalıştırın. Konsol penceresi aşağıdaki ekran görüntüsüne benzer görünmelidir:

    ![Konsol penceresi yönergeleri almak için hangi eylemleri içeren CalculateThis uygulama gösteriliyor.](media/vb-console-calculate-this.png)

::: moniker-end

## <a name="quick-answers-faq"></a>Hızlı yanıtlar hakkında SSS

İşte bazı temel kavramları vurgulamak için hızlı bir SSS.

### <a name="what-is-visual-basic"></a>Visual Basic nedir?

Visual Basic öğrenin kolay olacak şekilde tasarlanan bir tür açısından güvenli bir programlama dilidir. Bu, anlamına gelir "Başlangıç çok amaçlı sembolik yönerge kodu" BASİC'ten elde edilir.

### <a name="what-is-visual-studio"></a>Visual Studio nedir?

Visual Studio geliştiricileri için üretkenlik aracından oluşan bir tümleşik geliştirme paketidir. Bunu, programları ve uygulamaları oluşturmak için kullanabileceğiniz bir program olarak düşünün.

### <a name="what-is-a-console-app"></a>Bir konsol uygulaması nedir?

Bir konsol uygulaması girdi alır ve çıktı olarak da bilinir bir komut satırı penceresinde görüntüler bir konsol.

### <a name="what-is-net-core"></a>.NET Core nedir?

.NET core .NET Framework'ün gelişime sonraki adımdır. Burada .NET Framework programlama dilleri arasında kod paylaşma izin .NET Core platformlar arasında kod paylaşma olanağı ekler. Daha da iyi açık kaynak olan. (.NET Framework ve .NET Core kodunuzu çalıştırmak için bir sanal makine olarak davranan bir ortak dil çalışma zamanı (CLR) yanı sıra önceden oluşturulmuş işlevselliği kitaplıkları içerir.)

## <a name="next-steps"></a>Sonraki adımlar

Bu öğreticiyi tamamlamak Tebrikler! Daha da fazla bilgi edinmek için aşağıdaki öğreticiye bakın.

> [!div class="nextstepaction"]
> [Visual Basic ve Visual Studio'da .NET Core SDK'sı ile bir kitaplığı derleme](/dotnet/core/tutorials/vb-library-with-visual-studio)

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Basic dili izlenecek yolu](/dotnet/visual-basic/walkthroughs)
* [Visual Basic Dil Başvurusu](/dotnet/visual-basic/language-reference/index)
* [Visual Basic kod dosyaları için IntelliSense](../../ide/visual-basic-specific-intellisense.md)
