---
title: Kod stili seçenekleri ve kod temizleme
ms.date: 04/25/2019
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.CSharp.Code_Style.General
- VS.ToolsOptionsPages.Text_Editor.Basic.Code_Style.General
ms.workload:
- multiple
ms.openlocfilehash: 6144e5bf26436e7010e773fa7ac03ad24ad7c490
ms.sourcegitcommit: b593bb889f049fcbdff502c30b73178ed17dbdf0
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/20/2019
ms.locfileid: "67291003"
---
# <a name="code-style-preferences"></a>Kod stili tercihleri

Kod stili ayarları her proje kullanarak tanımladığınız bir [EditorConfig dosya](#code-styles-in-editorconfig-files), veya metin düzenleyicide Visual Studio'da Düzenle tüm kodlar için [ **seçenekleri** sayfa](#code-styles-in-the-options-dialog-box). İçin C# kod, Visual Studio kullanarak bu kod stili Tercihleri uygulamak için de yapılandırabilirsiniz **kod Temizleme** (Visual Studio 2019) ve **belgeyi Biçimlendir** (Visual Studio 2017) komutları.

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio'daki Düzenleyici davranışı](/visualstudio/mac/editor-behavior).

## <a name="code-styles-in-editorconfig-files"></a>EditorConfig dosyaları kod stilleri

[Kod stili ayarları](../ide/editorconfig-code-style-settings-reference.md) ekleyerek .NET belirtilebilir için bir [EditorConfig](create-portable-custom-editor-options.md) projenize bir dosya. EditorConfig dosyaları, Visual Studio kişiselleştirme hesabı yerine bir kod temeli ile ilişkilidir. EditorConfig dosyasındaki ayarları önceliklidir belirtilen kod stilleri **seçenekleri** iletişim kutusu. Depo veya proje tüm katkıda bulunanlar için kodlama stilleri uygulamak istediğinizde bir EditorConfig dosyasını kullanın.

::: moniker range=">=vs-2019"

EditorConfig dosyanızı el ile doldurabilirsiniz ya da Visual Studio'da ayarlayın kod stili ayarları temel dosya otomatik olarak oluşturabilirsiniz **seçenekleri** iletişim kutusu için C# veya Visual Basic metin düzenleyicisi. Bu seçenekler sayfası kullanılabilir **Araçları** > **seçenekleri** > **metin düzenleyici** > [**C#** veya  **Temel**] > **kod stili** > **genel**.
Tıklayın **ayarlarından .editorconfig dosyası oluştur** kodlama stili otomatik olarak oluşturulacak *.editorconfig* dosya tabanlı ayarlara göre bu **seçenekleri** sayfası.

![Visual Studio 2019 ayarlarından editorconfig dosyası oluştur](media/vs-2019/generate-editorconfig-file-small.png)

::: moniker-end

## <a name="code-styles-in-the-options-dialog-box"></a>Seçenekler iletişim kutusundaki kod stilleri

Kod stili tercihleri tüm için ayarlanabilir, C# ve Visual Basic projeleri açarak **seçenekleri** iletişim kutusundan **Araçları** menüsü. İçinde **seçenekleri** iletişim kutusunda **metin düzenleyici** > [**C#** veya **temel**] > **kod stili**  >  **Genel**.

Listedeki her bir öğe seçildiğinde tercih önizlemesini sunar:

::: moniker range="vs-2017"

![Kod stili seçenekleri](media/code-style-quick-actions-dialog.png)

::: moniker-end

::: moniker range=">=vs-2019"

![Kod stili seçenekleri](media/vs-2019/code-style-quick-actions-dialog.png)

::: moniker-end

Bu pencerede seçenekleri Visual Studio kişiselleştirme hesabınız için geçerli olan ve belirli bir proje ile ilişkili olmayan veya kod tabanı. Ayrıca, bunlar sürekli tümleştirme (CI) derlemeleri dahil olmak üzere, derleme zamanında zorunlu değildir. İstiyorsanız kod stili tercihleri projenizle ilişkilendirmek ve derleme sırasında uygulanan stili vardır, tercihlerini belirtin bir [.editorconfig dosyasındaki](#code-styles-in-editorconfig-files) projeyle ilişkili.

### <a name="preference-and-severity"></a>Tercihi ve önem derecesi

Bu sayfadaki her kod stili ayarı için belirlediğiniz **tercih** ve **önem derecesi** açılan listeler, her satırda kullanarak değerleri. Önem derecesi ayarlanabilir **hiçbiri**, **öneri**, **uyarı**, veya **hata**. Etkinleştirmek istiyorsanız [hızlı Eylemler](../ide/quick-actions.md) emin olmak için bir kod stili **önem derecesi** ayarı için bir şey dışında **hiçbiri**. **Hızlı Eylemler** ampul ![ampul](media/light-bulb-dropdown.png), hata ampul ![hata ampul](media/error-bulb.png), veya tornavida ![tornavida](media/screwdriver.png) simgesi görünür bir tercih edilmeyen stili kullanılır ve bir seçenek seçebileceğiniz **hızlı Eylemler** listeye otomatik olarak tercih edilen stili kodu yeniden yazın.

## <a name="apply-code-styles"></a>Kod stilleri Uygula

::: moniker range="vs-2017"

Yapılandırabileceğiniz **belgeyi Biçimlendir** komut (**Düzenle** > **Gelişmiş** > **belgeyi Biçimlendir**) için kod stili ayarlarınızı Uygula (EditorConfig dosyasından veya **kod stili** seçenekleri) birlikte normal (Girinti gibi) gerçekleştiren biçimlendirme. Varsa bir *.editorconfig* dosyası mevcut proje için bu ayarlara göre önceliklidir.

> [!NOTE]
> Kod stilleri kullanarak uygulama **belgeyi Biçimlendir** komutu, yalnızca kullanılabilir C# kod dosyaları. Bu Deneysel bir özelliğidir.

Hangi yapılandırmak istediğiniz **belgeyi Biçimlendir** uygulamak için [biçimlendirme seçenekleri sayfasında](reference/options-text-editor-csharp-formatting.md#format-document-settings).

![Kod stili ayarları için Visual Studio 2017'de belgeyi Biçimlendir](media/format-document-settings-experiment.png)

> [!TIP]
> Önem derecesi ile yapılandırılan kural **hiçbiri** kod temizleme katılmak yoktur ancak tek tek aracılığıyla uygulanabilir **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

Tetiklenen ilk kez **belgeyi Biçimlendir** komutu, bir sarı bir bilgi çubuğu kod temizleme ayarlarınızı yapılandırmak ister.

::: moniker-end

::: moniker range=">=vs-2019"

İçin C# kod dosyaları, Visual Studio 2019 sahip bir **kod Temizleme** düzenleyicisinin alt düğmesini (klavye: **CTRL**+**K**, **Ctrl**+**E**) EditorConfig dosyadaki veya kod stilleri uygulamak için **kod stili**  seçenekler sayfası. Varsa bir *.editorconfig* dosyası mevcut proje için öncelikli ayarları olanlardır.

![Visual Studio 2019 temizleme kodu yürütme](media/execute-code-cleanup.png)

> [!TIP]
> Önem derecesi ile yapılandırılan kural **hiçbiri** kod temizleme katılmak yoktur ancak tek tek aracılığıyla uygulanabilir **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

İlk olarak, hangi kod stilleri (birinde iki profilleri) de uygulamak istediğiniz yapılandırma **yapılandırma kod Temizleme** iletişim kutusu. Bu iletişim kutusunu açmak için kod temizleme broom simgesinin yanındaki genişletici oka tıklayın ve ardından **yapılandırma kod Temizleme**.  

![Visual Studio 2019 içinde kod temizleme yapılandırın](media/configure-code-cleanup.png)

Broom simgesine tıklayın veya basın kod temizleme yapılandırıldıktan sonra yapabilecekleriniz **Ctrl**+**K**, **Ctrl**+**E** kod temizleme çalıştırılacak. Tüm proje veya çözümünüzdeki arasında kod temizleme de çalıştırabilirsiniz. İçinde proje veya çözüm adına sağ tıklayın **Çözüm Gezgini**seçin **analiz ve kod Temizleme**ve ardından **çalıştırma kod Temizleme**.


![Tüm proje veya çözüm arasında kod temizleme işlemi çalıştırın](media/run-code-cleanup-project-solution.png)

Her zaman uygulanacak kod stili ayarlarınızı istiyorsanız bir dosyaya kaydedin, istediğiniz gibi [kod temizleme kaydederken](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.CodeCleanupOnSave) uzantısı.

::: moniker-end

## <a name="see-also"></a>Ayrıca bkz.

- [Hızlı Eylemler](../ide/quick-actions.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](../ide/editorconfig-code-style-settings-reference.md)
- [Düzenleyici davranışı (Mac için Visual Studio)](/visualstudio/mac/editor-behavior)