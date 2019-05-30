---
title: Bir menü komutuyla uzantı oluşturma | Microsoft Docs
ms.date: 3/16/2019
ms.topic: conceptual
helpviewer_keywords:
- write a vspackage
- vspackage
- tutorials
- visual studio package
ms.assetid: f97104c8-2bcb-45c7-a3c9-85abeda8df98
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: fb18792e2d0d357bb131af6c12e97425cd72fd05
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66345365"
---
# <a name="create-an-extension-with-a-menu-command"></a>Bir menü komutuyla uzantı oluşturma

Bu izlenecek yol, Not Defteri başlatan bir menü komutuyla uzantı oluşturma işlemini gösterir.

## <a name="prerequisites"></a>Önkoşullar

Visual Studio 2015'ten başlayarak, size Visual Studio SDK İndirme Merkezi'nden yüklemeyin. Visual Studio kurulumunda isteğe bağlı bir özellik olarak eklenmiştir. VS SDK'yi daha sonra yükleyebilirsiniz. Daha fazla bilgi için [Visual Studio SDK'yı yükleme](../extensibility/installing-the-visual-studio-sdk.md).

## <a name="create-a-menu-command"></a>Bir menü komutu oluşturun

1. Adlı bir VSIX projesi oluşturun **FirstMenuCommand**. VSIX proje şablonunda bulabilirsiniz **yeni proje** iletişim "VSIX" için arama yapın.

2. Projeyi açtığında, adlı bir özel komut öğesi şablonu ekleme **FirstCommand**. İçinde **Çözüm Gezgini**, proje düğümüne sağ tıklayıp **Ekle** > **yeni öğe**. İçinde **Yeni Öğe Ekle** iletişim kutusunda, Git **Visual C#**  > **genişletilebilirlik** seçip **özel komut**. İçinde **adı** alan penceresinin en altında komut dosyası adı için değiştirme *FirstCommand.cs*.

3. Projeyi oluşturmak ve hata ayıklamaya başlayın.

    Visual Studio'nun deneysel örneğinde görünür. Deneysel örnek hakkında daha fazla bilgi için bkz. [deneysel örneğinde](../extensibility/the-experimental-instance.md).

::: moniker range="vs-2017"

4. Deneysel örneğinde açın **Araçları** > **Uzantılar ve güncelleştirmeler** penceresi. Görmelisiniz **FirstMenuCommand** uzantıyı şurada. (Açarsanız **Uzantılar ve güncelleştirmeler** Visual Studio, çalışma örneğinde göremezsiniz **FirstMenuCommand**).

::: moniker-end

::: moniker range=">=vs-2019"

4. Deneysel örneğinde açın **uzantıları** > **uzantıları yönetme** penceresi. Görmelisiniz **FirstMenuCommand** uzantıyı şurada. (Açarsanız **uzantıları yönetme** Visual Studio, çalışma örneğinde göremezsiniz **FirstMenuCommand**).

::: moniker-end

Artık Git **Araçları** Deneysel örneğinin menü. Görmelisiniz **çağırma FirstCommand** komutu. Bu noktada, komut bildiren bir ileti kutusu getirir **FirstCommandPackage içinde FirstMenuCommand.FirstCommand.MenuItemCallback()** . Sonraki bölümde bu komut aslında Not defteri başlangıç nasıl göreceğiz.

## <a name="change-the-menu-command-handler"></a>Menü komut işleyici değiştirme

Şimdi komut işleyicinin Not Defteri'ni başlatın güncelleştirelim.

1. Hata ayıklamayı Durdur ve çalışma Örneğiniz için Visual Studio geri dönün. Açık *FirstCommand.cs* dosya ve aşağıdaki deyimi kullanarak:

    ```csharp
    using System.Diagnostics;
    ```

2. Özel FirstCommand Oluşturucusu bulun. Burada komutu için komut hizmeti ölçekledikçe ve komut işleyici belirtilen budur. Komut işleyici adı StartNotepad için aşağıdaki gibi değiştirin:

    ```csharp
    private FirstCommand(AsyncPackage package, OleMenuCommandService commandService)
    {
        this.package = package ?? throw new ArgumentNullException(nameof(package));
        commandService = commandService ?? throw new ArgumentNullException(nameof(commandService));

        CommandID menuCommandID = new CommandID(CommandSet, CommandId);
        // Change to StartNotepad handler.
        MenuCommand menuItem = new MenuCommand(this.StartNotepad, menuCommandID);
        commandService.AddCommand(menuItem);
    }
    ```

3. Kaldırma `MenuItemCallback` yöntemi ve ekleme bir `StartNotepad` not yalnızca başlayacak yöntemi:

    ```csharp
    private void StartNotepad(object sender, EventArgs e)
    {
        Process proc = new Process();
        proc.StartInfo.FileName = "notepad.exe";
        proc.Start();
    }
    ```

4. Şimdi deneyin. Ne zaman projesinde hata ayıklamaya başlama ve tıklayın **Araçları** > **çağırma FirstCommand**, Not Defteri gündeme örneğini görmeniz gerekir.

    Bir örneğini kullanabilir <xref:System.Diagnostics.Process> herhangi bir yürütülebilir dosya, yalnızca not defteri çalıştırmak için sınıf. İle deneyin `calc.exe`, örneğin.

## <a name="clean-up-the-experimental-environment"></a>Deneysel ortamını temizleyin

Birden fazla uzantı geliştirme veya yalnızca uzantı kodunuzu farklı sürümleriyle sonuçlarını araştırma, Deneysel ortamınızı, gerektiği gibi çalışmayı durdurabilir. Bu durumda, sıfırlama betiği çalıştırmanız gerekir. Çağrıldığı **Visual Studio Deneysel örneğini sıfırlama**, ve Visual Studio SDK'ın bir parçası olarak sunulur. Baştan başlamak üzere bu betik Deneysel ortamından uzantılarınızı için tüm başvuruları kaldırır.

Bu betik iki yoldan biriyle alabilirsiniz:

1. Masaüstü'nden Bul **Visual Studio Deneysel örneğini sıfırlama**.

2. Komut satırından şu komutu çalıştırın:

    ```xml
    <VSSDK installation>\VisualStudioIntegration\Tools\Bin\CreateExpInstance.exe /Reset /VSInstance=<version> /RootSuffix=Exp && PAUSE

    ```

## <a name="deploy-your-extension"></a>Uzantınızı dağıtmak

İstediğiniz gibi çalışan aracı uzantınızı olduğuna göre arkadaşlarınız ve iş arkadaşları ile paylaşma hakkında düşünmek için zaman var. Visual Studio 2015 yüklü sahip oldukları sürece bu kolay olmasıdır. Tüm yapmanız gereken göndermesini *.vsix* oluşturulan dosya. (Yayın modunda oluşturduğunuzdan emin olun.)

Bulabilirsiniz *.vsix* dosyasını bu uzantı *FirstMenuCommand* bin dizini. Özellikle, sürüm yapılandırmasını geliştirdim varsayıldığında, onu olacaktır:

*\<Kod dizini > \FirstMenuCommand\FirstMenuCommand\bin\Release\ FirstMenuCommand.vsix*

Uzantıyı yüklemek için Visual Studio tüm açık örneklerini kapatın ve ardından çift arkadaşınız gereken *.vsix* getirir dosyasını **VSIX yükleyicisi**. Dosyalar kopyalanır *%LocalAppData%\Microsoft\VisualStudio\<sürüm > \Extensions* dizin.

Arkadaş Visual Studio'yu yeniden getirirse, FirstMenuCommand uzantısı'nda bulabilirsiniz **Araçları** > **Uzantılar ve güncelleştirmeler**. Gidebilir **Uzantılar ve güncelleştirmeler** kaldırın veya uzantı çok devre dışı.

## <a name="next-steps"></a>Sonraki adımlar

Bu kılavuzda Visual Studio uzantısı ile neler yapabileceğinizi yalnızca küçük bir bölümün göstermiştir. Visual Studio uzantıları ile gerçekleştirebileceğiniz diğer (makul kolay) işlemlerden kısa bir listesi aşağıda verilmiştir:

1. Basit bir menü komutu ile pek çok şey yapabilirsiniz:

   1. Kendi simgesi ekleyin: [Menü komutlarına simge ekleme](../extensibility/adding-icons-to-menu-commands.md)

   2. Menü komutunun metnini değiştirme: [Menü komutunun metnini değiştirme](../extensibility/changing-the-text-of-a-menu-command.md)

   3. Bir komutu menüsü kısayolundan ekleyin: [Menü öğelerine klavye kısayolları bağlama](../extensibility/binding-keyboard-shortcuts-to-menu-items.md)

2. Farklı türde komutlar, menüler ve araç çubukları ekleyin: [Menüler ve komutlar genişletme](../extensibility/extending-menus-and-commands.md)

3. Araç pencereleri ekleyin ve yerleşik Visual Studio araç pencerelerini genişletme: [Genişletme ve özelleştirme araç pencereleri](../extensibility/extending-and-customizing-tool-windows.md)

4. IntelliSense, kod önerileri ve diğer özellikler için mevcut kod düzenleyicilerinden ekleyin: [Düzenleyici ve dil hizmetlerini genişletme](../extensibility/extending-the-editor-and-language-services.md)

5. Uzantınız için seçenekleri ve özellik sayfaları ve kullanıcı ayarlarını ekleyin: [Özellikler ve özellik penceresini genişletme](../extensibility/extending-properties-and-the-property-window.md) ve [kullanıcı ayarlarını ve seçeneklerini genişletme](../extensibility/extending-user-settings-and-options.md)

   Yeni türde bir proje oluşturma gibi daha fazla iş, diğer tür uzantıların gerektirir ([genişletme projeleri](../extensibility/extending-projects.md)), yeni türde bir düzenleyici oluşturma ([özel düzenleyiciler ve tasarımcılar oluşturma](../extensibility/creating-custom-editors-and-designers.md)), veya uygulama, bir yalıtılmış kabuk uzantısını: [Visual Studio yalıtılmış Kabuğu](/visualstudio/extensibility/shell/visual-studio-isolated-shell)
