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
ms.openlocfilehash: a7a478e8d3575e70a11ec776d59337ae93e7a677
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57873366"
---
# <a name="code-style-preferences"></a>Kod stili tercihleri

Kod stili tercihleri ayarlanabilir C# ve Visual Basic projeleri için açarak **seçenekleri** iletişim kutusundan **Araçları** menüsü. İçinde **seçenekleri** iletişim kutusunda **metin düzenleyici** > [**C#** veya **temel**] > **kod stili**  >  **Genel**. Listedeki her bir öğe seçildiğinde tercih önizlemesini sunar:

![Kod stili seçenekleri](media/code-style-quick-actions-dialog.png)

Bu pencerede seçenekleri Visual Studio kişiselleştirme hesabınız için geçerli olan ve belirli bir proje ile ilişkili olmayan veya kod tabanı. Ayrıca, bunlar sürekli tümleştirme (CI) derlemeleri dahil olmak üzere, derleme zamanında zorunlu değildir. İstiyorsanız kod stili tercihleri projenizle ilişkilendirmek ve derleme sırasında uygulanan stili vardır, tercihlerini belirtin bir [.editorconfig dosyasındaki](#editorconfig-files).

> [!NOTE]
> Bu konu, Windows üzerinde Visual Studio için geçerlidir. Mac için Visual Studio için bkz: [Mac için Visual Studio'daki Düzenleyici davranışı](/visualstudio/mac/editor-behavior).

## <a name="preference-and-severity"></a>Tercihi ve önem derecesi

Her öğe için ayarladığınız **tercih** ve **önem derecesi** açılan listeler, her satırda kullanarak değerleri. Önem derecesi ayarlanabilir **hiçbiri**, **öneri**, **uyarı**, veya **hata**. Etkinleştirmek istiyorsanız [hızlı Eylemler](../ide/quick-actions.md) emin olmak için bir kod stili **önem derecesi** ayarı için bir şey dışında **hiçbiri**. **Hızlı Eylemler** ampul ![ampul](media/light-bulb-dropdown.png), hata ampul ![hata ampul](media/error-bulb.png), veya tornavida ![tornavida](media/screwdriver.png) simgesi görünür bir tercih edilmeyen stili kullanılır ve bir seçenek seçebileceğiniz **hızlı Eylemler** listeye otomatik olarak tercih edilen stili kodu yeniden yazın.

## <a name="editorconfig-files"></a>EditorConfig dosyaları

.NET ekleyerek de belirtilebilir için kod stili ayarları bir [EditorConfig](../ide/editorconfig-code-style-settings-reference.md) projenize bir dosya. Bu dosyaları, Visual Studio kişiselleştirme hesabı yerine bir kod temeli ile ilişkilidir. EditorConfig dosyasındaki ayarları önceliklidir seçili Seçenekler **seçenekleri** iletişim kutusu. Depo veya proje tüm katkıda bulunanlar için kodlama stilleri uygulamak istediğinizde bir EditorConfig dosyasını kullanın.

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