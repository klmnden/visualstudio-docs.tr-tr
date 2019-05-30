---
title: Hello World uzantısı Öğreticisi | Microsoft Docs
ms.date: 03/14/2019
ms.topic: conceptual
ms.assetid: f74e1ad1-1ee5-4360-9bd5-d82467b884ca
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4c3bbafcf138c60b65940bcee73c74f56cf6e2fd
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66342856"
---
# <a name="create-your-first-extension-hello-world"></a>İlk uzantınızı oluşturun: Merhaba Dünya

Bu Hello World örnek, Visual Studio için ilk uzantınızı oluşturmada size yol gösterir. Bu öğreticide Visual Studio için yeni bir komut eklerseniz gösterilmektedir.

Bu süreçte şunları öğreneceksiniz nasıl yapılır:

* **[Bir genişletilebilirlik projesi oluşturma](#create-an-extensibility-project)**
* **[Özel komut ekleme](#add-a-custom-command)**
* **[Kaynak kodu değiştirin](#modify-the-source-code)**
* **[Çalıştırın](#run-it)**

Bu örnekte, Visual C# özel menü düğmesi "Deyin. Hello World!" adlı eklemek için kullanacağınız şöyle görünür:

![Hello World komutu](media/hello-world-say-hello-world.png)

> [!NOTE]
> Bu makale, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio genişletilebilirlik kılavuzda](/visualstudio/mac/extending-visual-studio-mac-walkthrough).

## <a name="prerequisites"></a>Önkoşullar

Başlamadan önce yüklediğinizden emin olun **Visual Studio uzantısı geliştirme** ihtiyacınız ve örnek kod VSIX şablonu içeren iş yükü.

> [!NOTE]
> Visual Studio (Community, Professional veya Enterprise) Visual Studio genişletilebilirlik projesi oluşturmak için herhangi bir sürümünü kullanabilirsiniz.

## <a name="create-an-extensibility-project"></a>Bir genişletilebilirlik projesi oluşturma

::: moniker range="vs-2017"

Adım 1. Gelen **dosya** menüsünde **yeni** > **proje**.

Adım 2. Sağ üst köşedeki arama kutusuna "VSIX" yazın ve görseli seçin C# **VSIX projesi**. "HelloWorld" girin **adı** seçin ve iletişim alt kısmındaki **Tamam**.

![Yeni Proje](media/hello-world-new-project.png)

Başlarken sayfası ve bazı örnek kaynaklar görmelisiniz.

Bu öğreticide bırakın ve kendisine döndürülmesini gerekiyorsa, yeni HelloWorld projeniz bulabileceğiniz **başlangıç sayfası** içinde **son** bölümü.

::: moniker-end

::: moniker range=">=vs-2019"

Adım 1. Gelen **dosya** menüsünde **yeni** > **proje**. Görseli seçin ve "VSIX" için arama C# **VSIX projesi** ardından **sonraki**.

Adım 2. "HelloWorld" girin **proje adı** seçip **Oluştur**.

![Yeni Proje](media/hello-world-new-project-2019.png)

HelloWorld projede görmelisiniz **Çözüm Gezgini**.

::: moniker-end

## <a name="add-a-custom-command"></a>Özel komut ekleme

Adım 1. Seçerseniz *.vsixmanifest* bildirim dosyası, hangi seçenekleri ayarlarken, açıklama, yazar ve sürümü gibi olduğunu görebilirsiniz.

Adım 2. ' % S'projesi (çözümü değil) sağ tıklayın. Bağlam menüsünde **Ekle**, ardından **yeni öğe**.

Adım 3. Seçin **genişletilebilirlik** bölümüne ve ardından **özel komut**.

4. adımı. İçinde **adı** altındaki alan, bir dosya adı girmeniz *Command.cs*.

![özel komut](media/hello-world-custom-command.png)

Yeni komut dosyanızı görülebilir **Çözüm Gezgini**. Altında **kaynakları** düğümü, komutunuza ilgili diğer dosyaları bulabilirsiniz. Örneğin, görüntüyü değiştirmek isterseniz, PNG dosyası aşağıda verilmiştir.

## <a name="modify-the-source-code"></a>Kaynak kodu değiştirin

Bu noktada, otomatik olarak oluşturulan komut ve düğme metni olan ve çok ilginç. Değişiklik yapmak istiyorsanız VSCT dosyasını ve CS dosyasını değiştirebilirsiniz.

* VSCT Burada, Komutlarınızın yeniden adlandırma, yapabilir Visual Studio komut sistemde nereye tanımlamak dosyasıdır. VSCT dosya keşfederken VSCT kod denetimleri her hangi bir bölümü açıklayan yorumlar fark edeceksiniz.

* Tıklama işleyicisi gibi eylemler burada tanımlarsınız CS dosyasıdır.

::: moniker range="vs-2017"

Adım 1. İçinde **Çözüm Gezgini**, yeni komutunuz için VSCT dosyası bulunamıyor. Bu durumda, çağrılacak *CommandPackage.vsct*.

![komut paket vsct](media/hello-world-command-package-vsct.png)

::: moniker-end

::: moniker range=">=vs-2019"

Adım 1. İçinde **Çözüm Gezgini**, VS uzantısı paketiniz için VSCT dosyası bulunamıyor. Bu durumda, çağrılacak *HelloWorldPackage.vsct*.

::: moniker-end

Adım 2. Değişiklik `ButtonText` parametresi `Say Hello World!`.

```xml
  ...
  <Button guid="guidCommandPackageCmdSet" id="CommandId" priority="0x0100" type="Button">
     <Parent guid="guidCommandPackageCmdSet" id="MyMenuGroup" />
     <Icon guid="guidImages" id="bmpPic1" />
     <Strings>
        <ButtonText>Say Hello World!</ButtonText>
     </Strings>
  </Button>
  ...
```

Adım 3. Geri Git **Çözüm Gezgini** ve bulma *Command.cs* dosya. İçinde `Execute` yöntemi, dize değiştirme `message` gelen `string.Format(..)` için `Hello World!`.

```csharp
  ...
  private void Execute(object sender, EventArgs e)
  {
    ThreadHelper.ThrowIfNotOnUIThread();
    string message = "Hello World!";
    string title = "Command";

    // Show a message box to prove we were here
    VsShellUtilities.ShowMessageBox(
        this.ServiceProvider,
        message,
        title,
        OLEMSGICON.OLEMSGICON_INFO,
        OLEMSGBUTTON.OLEMSGBUTTON_OK,
        OLEMSGDEFBUTTON.OLEMSGDEFBUTTON_FIRST);
  }
  ...
```

Her dosya için değişikliklerinizi kaydettiğinizden emin olun.

## <a name="run-it"></a>Çalıştırın

Bu gibi durumlarda, kaynak kodu artık Visual Studio deneysel örneğinde çalıştırabilirsiniz.

Adım 1. Tuşuna **F5** çalıştırılacak **hata ayıklamayı Başlat** komutu. Bu komut, projeyi derler ve Visual Studio adlı yeni bir örneğini başlatarak, hata ayıklayıcıyı başlatır **deneysel örneğinde**.

::: moniker range="vs-2017"

Sözcükleri göreceğiniz **deneysel örneğinde** Visual Studio başlık çubuğunda.

![deneysel örneği başlık çubuğu](media/hello-world-exp-instance.png)

::: moniker-end

Adım 2. Üzerinde **Araçları** menüsü **deneysel örneğinde**, tıklayın **Say Hello World!** .

![Son Sonuç](media/hello-world-final-result.png)

Yeni özel komuttan bir çıktı görmeniz gerekir, bu durumda ekranın ortasında iletişim sağlayan **Merhaba Dünya!** İleti.

## <a name="next-steps"></a>Sonraki adımlar

Visual Studio genişletilebilirliği ile çalışmanın temel bilgileri artık bildiğinize göre İşte burada daha fazla bilgi edinebilirsiniz:

* [Visual Studio uzantılarını geliştirmeye başlamak](starting-to-develop-visual-studio-extensions.md) -örnekler, öğreticiler. ve uzantınızı yayımlama
* [Visual Studio 2017 SDK'daki yenilikler](what-s-new-in-the-visual-studio-2017-sdk.md) -Visual Studio 2017'de yeni genişletilebilirlik özellikleri
* [Visual Studio 2019 SDK'da yenilikler](whats-new-visual-studio-2019-sdk.md) -Visual Studio 2019 yeni genişletilebilirlik özellikleri
* [Visual Studio SDK içinde](internals/inside-the-visual-studio-sdk.md) -Visual Studio genişletilebilirlik ayrıntılarını öğrenin