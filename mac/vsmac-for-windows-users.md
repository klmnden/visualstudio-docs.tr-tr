---
title: Windows kullanıcıları için Mac için Visual Studio
description: Mac için Visual Studio erişilebilirlik özelliklerinin ve bunların nasıl etkinleştiribilecekleri hakkında giriş.
author: alclark
ms.author: alcl
ms.date: 09/25/2019
ms.assetid: 61CB6883-08CE-470F-8599-6F7570DB756E
ms.openlocfilehash: 3306cdec93b501ad2006bbee2ceca3bf42514fe9
ms.sourcegitcommit: 7739f36507b4762eea83c692102bdc5188460f28
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/26/2019
ms.locfileid: "71314488"
---
# <a name="visual-studio-for-mac-for-windows-users"></a>Windows kullanıcıları için Mac için Visual Studio

Bir işletim sisteminden diğerine geçiş yapmak çok fazla olabilir. Platformlar arası uygulamalarda, kullanıcı arabiriminden menü öğelerinin kategorilere ayrılması arasında genellikle daha hafif farklılıklar vardır. Ayrıca, kullanıcıların yeni işletim sisteminin kullanıcı arabirimine aclım öğrenme eğrisi vardır. Burada, Windows için Mac için Visual Studio ve Visual Studio arasındaki en yaygın farklılıkları öğreneceksiniz. Ayrıca, macOS ve Windows arasında birkaç farklı kural öğreneceksiniz.

## <a name="keyboard-shortcuts"></a>Klavye kısayolları

Geliştirici olarak, sizin görevleriniz ve gezinileriniz için klavyeyi kullanmaya alışkın olursunuz. Klavyedeki bazı anahtarlar, Mac ve Windows bilgisayarları arasında ortaktır. Kopyalama ve yapıştırma gibi klavye eylemlerinin aynı anahtar birleşimlerini kullanmasını düşünmeye yönelik bir anlayışın. Bu her zaman durum değildir. Neyse ki, Windows 'daki Visual Studio ile yakından eşleştirmek için Mac için Visual Studio içindeki anahtar bağlamalarınızı değiştirebilirsiniz.

Mac için Visual Studio ilk kez çalıştırdığınızda klavye kısayolları seçim penceresini görürsünüz: ![Anahtar bağlamaları penceresi](media/ide-tour-2019-keyboard-shortcut.png)

Anahtar bağlamalarını daha sonra değiştirmek istiyorsanız, bu ayarı tercihlerinde bulabilirsiniz: ![Anahtar bağlamaları tercihleri](media/customizing-the-ide-image10a.png)

MacOS 'un Windows için farklı sistem genelinde kısayollar kullandığını unutmayın. Anahtar bağlama tercihlerini değiştirmek, Mac için Visual Studio tanıdık Windows kısayollarını kullanmanıza izin verir. Ancak, macOS 'un diğer alanlarında macOS kısayollarıyla ilgili bilgi sahibi olmanız gerekir.

MacOS komutu (⌘) değiştirici tuşu, genellikle Windows 'daki denetim anahtarının yerini alabilir. Aşağıda bazı örnekler ve diğer yaygın olarak kullanılan kısayollar verilmiştir:

|Görev                   |Windows kısayolu         |macOS kısayolu      |
|-----------------------|-------------------------|--------------------|
|Kopyala                   |`Ctrl + C`               |`⌘ + C`             |
|Yapıştır                  |`Ctrl + V`               |`⌘ + V`             |
|Kes                    |`Ctrl + X`               |`⌘ + X`             |
|Geri alma                   |`Ctrl + Z`               |`⌘ + Z`             |
|Yinele                   |`Ctrl + Shift + Z`       |`⌘ + Shift + Z`     |
|İmleci sağ Sil |`Delete`                 |`fn + Backspace`    |
|Kelimeyi Sil            |`Ctrl + Delete`          |`fn + ⌥ + Backspace`|

> [!TIP]
> [Apple Support Web sitesinde](https://support.apple.com/en-us/HT201236)MacOS kısayollarının kapsamlı bir listesini bulabilirsiniz.

## <a name="menus"></a>Menüler

MacOS menüleri Windows 'daki menülerden farklı şekilde düzenlenmiştir. Mac için Visual Studio özel durum değildir. En yaygın menü seçeneklerinden bazılarını buradan bulabilirsiniz:

|Görev                   |Visual Studio (Windows)                                              |Mac için Visual Studio                |
|-----------------------|---------------------------------------------------------------------|-------------------------------------|
|Tercihler (Seçenekler)  |Araçlar > seçenekleri...                                                   |Visual Studio > tercihleri...       |
|Uzantılar             |Uzantılar > Uzantıları Yönetme                                       |Visual Studio > uzantıları...        |
|Düzenler                |Pencere > pencere düzeni uygula > [Düzen Seç]                       |Görüntüleme > [Düzen Seç]               |
|Güncelleştirmeler                |Güncelleştirme > için yardım denetimi                                             |Visual Studio güncelleştirmeleri denetle >... |
|NuGet Paket Yöneticisi  |NuGet Paket Yöneticisi > Araçlar > NuGet paketlerini veya çözümünü Yönet... |Proje > NuGet Paketlerini Yönet...   |
|Pad/Windows         |Görünüm > [panel/pencere Seç]                                         |> Bölmeleri görüntüleme > [panel/pencere seçin]  |
|Araç bul             |Düzenle > bul ve Değiştir > [araç seçin]                              |Arama > [Araç seçme]               |
|Visual Studio Hakkında    |Microsoft Visual Studio hakkında Yardım >                                 |Visual Studio > Visual Studio hakkında  

> [!NOTE]
> [IDE turundan](ide-tour.md) Mac için Visual Studio en yaygın özelliklere genel bakış bulabilirsiniz