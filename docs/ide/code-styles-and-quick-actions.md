---
title: Kod stili tercihleri
ms.date: 03/12/2019
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Code_Style.General
- VS.ToolsOptionsPages.Text_Editor.Basic.Code_Style.General
ms.workload:
- multiple
ms.openlocfilehash: 689bdb62d5a4bc9aea21da67e8e5e844660756d6
ms.sourcegitcommit: b14b7a938a2aba9fcce4d5e813aadf2040b0dcda
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58647316"
---
# <a name="code-style-preferences"></a>Kod stili tercihleri

Kod stili tercihleri ayarlanabilir C# ve Visual Basic projeleri için açarak **seçenekleri** iletişim kutusundan **Araçları** menüsü. İçinde **seçenekleri** iletişim kutusunda **metin düzenleyici** > [**C#** veya **temel**] > **kod stili**  >  **Genel**.

Listedeki her bir öğe seçildiğinde tercih önizlemesini sunar:

::: moniker range="vs-2017"

![Kod stili seçenekleri](media/code-style-quick-actions-dialog.png)

::: moniker-end

::: moniker range=">=vs-2019"

![Kod stili seçenekleri](media/vs-2019/code-style-quick-actions-dialog.png)

::: moniker-end

Bu pencerede seçenekleri Visual Studio kişiselleştirme hesabınız için geçerli olan ve belirli bir proje ile ilişkili olmayan veya kod tabanı. Ayrıca, bunlar sürekli tümleştirme (CI) derlemeleri dahil olmak üzere, derleme zamanında zorunlu değildir. İstiyorsanız kod stili tercihleri projenizle ilişkilendirmek ve derleme sırasında uygulanan stili vardır, tercihlerini belirtin bir [.editorconfig dosyasındaki](#editorconfig-files).

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio'daki Düzenleyici davranışı](/visualstudio/mac/editor-behavior).

## <a name="editorconfig-files"></a>EditorConfig dosyaları

.NET ekleyerek de belirtilebilir için kod stili ayarları bir [EditorConfig](../ide/editorconfig-code-style-settings-reference.md) projenize bir dosya.

::: moniker range=">=vs-2019"

Tıklayın **ayarlarından .editorconfig dosyası oluştur** otomatik olarak bir kodlama stili .editorconfig dosyası oluşturmak için temel alan bu bildirimler'i seçenekleri **seçenekleri** sayfası.

![VS 2019 ayarlarından editorconfig dosyası oluştur](media/vs-2019/generate-editorconfig-file-small.png)

::: moniker-end

EditorConfig dosyaları, Visual Studio kişiselleştirme hesabı yerine bir kod temeli ile ilişkilidir. EditorConfig dosyasındaki ayarları önceliklidir seçili Seçenekler **seçenekleri** iletişim kutusu. Depo veya proje tüm katkıda bulunanlar için kodlama stilleri uygulamak istediğinizde bir EditorConfig dosyasını kullanın.

## <a name="preference-and-severity"></a>Tercihi ve önem derecesi

Bu sayfadaki her kod stili ayarı için belirlediğiniz **tercih** ve **önem derecesi** açılan listeler, her satırda kullanarak değerleri. Önem derecesi ayarlanabilir **hiçbiri**, **öneri**, **uyarı**, veya **hata**. Etkinleştirmek istiyorsanız [hızlı Eylemler](../ide/quick-actions.md) emin olmak için bir kod stili **önem derecesi** ayarı için bir şey dışında **hiçbiri**. **Hızlı Eylemler** ampul ![ampul](media/light-bulb-dropdown.png), hata ampul ![hata ampul](media/error-bulb.png), veya tornavida ![tornavida](media/screwdriver.png) simgesi görünür bir tercih edilmeyen stili kullanılır ve bir seçenek seçebileceğiniz **hızlı Eylemler** listeye otomatik olarak tercih edilen stili kodu yeniden yazın.

## <a name="format-document-command"></a>Biçim belgesi komutu

Yapılandırabileceğiniz **belgeyi Biçimlendir** komut (**Düzenle** > **Gelişmiş** > **belgeyi Biçimlendir**) için kullanımları Kaldır ve Sırala gibi bir dosya çubuğunda ek kod temizleme gerçekleştirebilir veya kod stili tercihleri uygulayın. İstediğiniz hangi ayarların tanımlayabilirsiniz **belgeyi Biçimlendir** uygulamak için [biçimlendirme seçenekleri sayfasında](reference/options-text-editor-csharp-formatting.md#format-document-settings).

Kod temizleme uyar yapılandırılan ayarları bir *.editorconfig* dosya veya bu kuralı veya bu kümesindeki dosya eksik **Araçları** > **seçenekleri**  >  **Metin düzenleyici**  >  **C#** > [**kod stili** veya **biçimlendirme**].

Tetiklenen ilk kez **belgeyi Biçimlendir** komutu Visual Studio'da bir sarı bir bilgi çubuğu kod temizleme ayarlarınızı yapılandırmak ister.

> [!TIP]
> Önem derecesi ile yapılandırılan kural **hiçbiri** kod temizleme katılmak yoktur, ancak ayrı ayrı aracılığıyla uygulanabilir **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

## <a name="see-also"></a>Ayrıca bkz.

- [Hızlı Eylemler](../ide/quick-actions.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](../ide/editorconfig-code-style-settings-reference.md)
- [Düzenleyici davranışı (Mac için Visual Studio)](/visualstudio/mac/editor-behavior)