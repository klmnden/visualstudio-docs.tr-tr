---
title: Genel, Ortam, Seçenekler İletişim Kutusu
ms.date: 03/28/2019
ms.topic: reference
f1_keywords:
- VS.Message.0x800a002e
- VS.ToolsOptionsPages.Environment.General
- VS.Environment.General
helpviewer_keywords:
- MRU lists
- windows, customizing
- MDI, environment options
- speed, environment animation
- File menu
- menus, customizing
- Windows menu customizing
- status bars, displaying
- IDE, startup options
- editors, autocompletion
- Options dialog box, General Environment
- General Environment Options dialog box
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4fdbd8c64514854aa77c358145badbf6583996f1
ms.sourcegitcommit: b14b7a938a2aba9fcce4d5e813aadf2040b0dcda
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58647277"
---
# <a name="options-dialog-box-environment--general"></a>Seçenekler iletişim kutusu: Ortam \> genel

Renk temaları, durum çubuğu ayarları ve tümleşik geliştirme ortamı (IDE) için diğer seçenekler arasında dosya uzantısı ilişkilendirmelerini değiştirmek için bu sayfayı kullanın. Erişebileceğiniz **seçenekleri** iletişim kutusunu açarak **Araçları** menüsünde, seçme **seçenekleri**açarak **ortam** klasörünü ve ardından seçme **genel** sayfası. Bu sayfa, listede görünmüyorsa, seçin **tüm ayarları göster** onay kutusuna **seçenekleri** iletişim kutusu.

## <a name="visual-experience"></a>Görsel deneyim

**Renk teması**

Seçin **mavi**, **ışık**, **koyu**, veya **mavi (ekstra kontrast)** IDE renk teması.

Ek önceden tanımlı Temalar yükleyebilir ve özel temalar indirip yükleyerek oluşturma **Visual Studio Color Theme Editor** gelen [Visual Studio Market](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.VisualStudio2017ColorThemeEditor). Bu aracı yükledikten sonra ek renk temaları görünür **renk teması** liste kutusu.

**İlk harfler büyük menü çubuğuna stilini Uygula**

Menüleri, ilk harfler büyük stilini varsayılan olarak kullanın. Tüm büyük harfli stil oluşturma yerine kullanmak için bu seçeneği temizleyin.

::: moniker range=">=vs-2019"

**İşleme farklı piksel densities ekranlar için en iyi duruma getirme (yeniden başlatma gerektirir)**

Bu seçeneği etkinleştirir veya İzleyici başına nokta / inç (DPI) tanıma devre dışı bırakır (veya *PMA*). Visual Studio kullanıcı arabirimi, PMA etkinleştirildiğinde, canlı bir izleyici görünen ölçek faktörü ve DPI yapılandırma, birden fazla monitöre dahil olmak üzere görünür. Windows ihtiyacınız PMA etkinleştirmek için 10 Nisan 2018 güncelleştirmesi veya üstü ve .NET Framework 4,8 veya üzeri. (Bu iki Önkoşullar karşılanmadı varsa bu seçeneği gri renkte görünür.)

::: moniker-end

**İstemci performansına dayalı görsel deneyimi otomatik olarak ayarla**

Görsel deneyimi için düzeltme Visual Studio otomatik olarak ayarlar ya da düzeltme açık olarak belirtir. Düz renkler için bu ayarı renkleri görüntülenmesini gradyanlar değişebilir veya menüleri veya açılır pencereleri içinde animasyon kullanımını kısıtlayabilirsiniz.

**Zengin istemci deneyimini etkinleştir**

Visual Studio, gradyanlar ve animasyonlar içeren tam görsel deneyimi sağlar. Bu özellikler, bu gibi durumlarda kötü performans olabileceği için bu seçeneği kullanırken Uzak Masaüstü bağlantılarında veya eski grafik bağdaştırıcıları temizleyin. Bu seçenek yalnızca, temizlediğinizde kullanılabilir **istemcide dayalı görsel deneyimi otomatik olarak ayarla** seçeneği.

**Donanım grafik ivmesi kullan**

Yazılım hızlandırma yerine varsa donanım grafik hızlandırması kullanır.

## <a name="other"></a>Diğer

**Pencere menüsünde gösterilecek öğeler**

Windows listesinde görünen pencerelerinin sayısını özelleştirir **penceresi** menüsü. 1 ile 24 arasında bir sayı girin. Varsayılan değer 10'dur.

**Son kullanılan listesinde gösterilen öğeler**

En son kullanılan projeler ve görünen dosyaları sayısı özelleştirir **dosya** menüsü. 1 ile 24 arasında bir sayı girin. Varsayılan değer 10'dur. Alma son kullanılan projeler ve dosyalar için kolay bir yolu budur.

**Durum çubuğunu göster**

Durum çubuğu görüntüler. Durum çubuğu, IDE pencerenin alt kısmında bulunur ve devam eden işlemler ilerleme durumu hakkında bilgileri görüntüler.

**Kapat düğmesi sadece etkin araç penceresini etkiler**

Belirtir **Kapat** düğmesine tıklandığında, odaklanmış araç penceresi yalnızca kapalı ve tüm yerleşik kümesindeki aracı Windows. Varsayılan olarak, bu seçenek seçilidir.

**Otomatik Gizle düğmesi sadece etkin araç penceresini etkiler**

Belirtir **Otomatik Gizle** düğmesine tıklandığında, odaklanmış araç penceresi otomatik olarak ve değil gizli tüm yerleştirilmiş kümesindeki aracı pencereleri. Bu seçenek varsayılan olarak, seçili değil.

## <a name="see-also"></a>Ayrıca bkz.

- [Ortam Seçenekleri İletişim Kutusu](../../ide/reference/environment-options-dialog-box.md)
- [Pencere düzenlerini özelleştirme](../../ide/customizing-window-layouts-in-visual-studio.md)