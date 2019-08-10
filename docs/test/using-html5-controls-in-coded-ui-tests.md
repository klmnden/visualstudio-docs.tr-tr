---
title: Kodlanmış UI Testlerinde HTML5 Denetimleri Kullanma
ms.date: 11/04/2016
ms.topic: conceptual
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: c7087f08743e58426663734295339d9ca6550a0d
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926582"
---
# <a name="using-html5-controls-in-coded-ui-tests"></a>Kodlanmış UI testlerinde HTML5 denetimleri kullanma

Kodlanmış UI testleri, Internet Explorer 9 ve Internet Explorer 10 ' da bulunan HTML5 denetimlerinin bazılarına yönelik destek içerir.

[!INCLUDE [coded-ui-test-deprecation](includes/coded-ui-test-deprecation.md)]

**Gereksinimler**

- Visual Studio Enterprise

> [!WARNING]
> Internet Explorer 10 ' dan önceki sürümlerde, kodlanmış UI testlerini Internet Explorer süreciyle karşılaştırıldığında daha yüksek bir ayrıcalık düzeyinde çalıştırmak mümkün oldu. Internet Explorer 10 ' da kodlanmış UI testleri çalıştırılırken, hem kodlanmış UI testi hem de Internet Explorer işlemi aynı ayrıcalık düzeyinde olmalıdır. Bunun nedeni, Internet Explorer 10 ' da daha güvenli AppContainer özellikleri.

> [!WARNING]
> Internet Explorer 10 ' da kodlanmış UI testi oluşturursanız, Internet Explorer 9 veya Internet Explorer 8 kullanılarak çalışmayabilir. Bunun nedeni, Internet Explorer 10 ' un ses, video, ProgressBar ve kaydırıcı gibi HTML5 denetimlerini içermektir. Bu HTML5 denetimleri, Internet Explorer 9 veya Internet Explorer 8 tarafından tanınmaz. Benzer şekilde, Internet Explorer 9 kullanarak kodlanmış UI testleri, Internet Explorer 8 tarafından tanınmayacak bazı HTML5 denetimleri de içerebilir.

## <a name="audio-control"></a>Ses denetimi

**Ses denetimi:** HTML5 ses denetimindeki eylemler doğru şekilde kaydedilir ve kayıttan yürütülür.

![HTML5 ses denetimi](../test/media/codedui_html5_audio.png)

|Eylem|Yapılmıyor|Oluşturulan kod|
|-|---------------|-|
|**Ses çal**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|00:00:00 \<'den Ses > oynatma adı|Htmdefdio. Play (TimeSpan)|
|**Ses içinde belirli bir zamana arama**|> \<İçin ses arama adı 00:01:48|Htmdefdio. Seek (TimeSpan)|
|**Sesi Duraklat**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|00:01:53 \<konumunda > adlı sesi Duraklat|Htmdefdio. Pause (TimeSpan)|
|**Sesi sustur**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|Sessiz \<ad > Ses|Htmdefdio. Mute ()|
|**Sesi aç**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|> \<Sesi aç|Htmdefdio. aç ()|
|**Ses düzeyini Değiştir**|> Ses \<adı birimini% 79 olarak ayarlayın|Htmdefdio. SetVolume (float)|

Onaylama ekleyebileceğiniz özelliklerin listesi için bkz. [Htmdefdioelement](https://developer.mozilla.org/docs/Web/API/HTMLAudioElement) .

**Arama özellikleri:** İçin `HtmlAudio` arama özellikleri ve `Name` `Id` '`Title`dir.

**Filtre Özellikleri:** İçin `HtmlAudio` filtre özellikleri, `Src` `Class` ve`TagInstance`'dir. `ControlDefinition`

> [!NOTE]
> Arama ve duraklatma için zaman miktarı önemli olabilir. Kayıttan yürütme sırasında, kodlanmış UI testi sesi duraklatmadan önce içinde `(TimeSpan)` belirtilen zamana kadar bekler. Bazı özel durumlar tarafından, belirtilen süre duraklatma komutuna vurmadan önce geçmişse, bir özel durum oluşturulur.

## <a name="video-control"></a>Video denetimi
**Video denetimi:** HTML5 video denetimindeki eylemler doğru şekilde kaydedilir ve kayıttan yürütülür.

![HTML5 video denetimi](../test/media/codedui_html5_video.png)

|Eylem|Yapılmıyor|Oluşturulan kod|
|-|---------------|-|
|**Videoyu oynat**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|> \<Oynatma adı video 00:00:00|HtmlVideo. Play (TimeSpan)|
|**Videoda belirli bir zamana arama**|> \<Video ile 00:01:48 arasındaki arama adı|HtmlVideo. Seek (TimeSpan)|
|**Videoyu Duraklat**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|00:01:53 \<adresinde > videoyu Duraklat|HtmlVideo. Pause (TimeSpan)|
|**Videoyu sustur**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|Sessiz \<ad > videosu|HtmlVideo. Mute ()|
|**Videoyu aç**<br /><br /> Doğrudan denetimden veya denetimin sağ tıklama menüsünden.|Ad \<> videoyu aç|HtmlVideo. aç ()|
|**Video hacmini değiştirme**|Video > \<adı birimini% 79 olarak ayarlayın||

Onaylama ekleyebileceğiniz özelliklerin listesi için bkz. [Htmlvideoelement](https://developer.mozilla.org/docs/Web/HTML/Element/video) .

**Arama özellikleri:** İçin `HtmlVideo` arama özellikleri ve `Name` `Id` '`Title`dir.

**Filtre Özellikleri:** İçin `HtmlVideo` filtre özellikleri, `Src` `Poster` ,ve`TagInstance`'dir. `Class` `ControlDefinition`

> [!NOTE]
> -30s veya + 30s etiketlerini kullanarak videoyu geri sarın veya ileri sardıysanız, bu, uygun zamana göre arama yapmak için toplanır.

## <a name="progressbar"></a>ProgressBar
**ProgressBar denetimi:** ProgressBar, ınteractable olmayan bir denetimdir. Bu denetimin `Value` ve `Max` özelliklerine onay ekleyebilirsiniz. Daha fazla bilgi için bkz. [HTMLProgressElement](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/progress).

![HTML5 ProgressBar denetimi](../test/media/codedui_html5_progressbar.png)

## <a name="see-also"></a>Ayrıca bkz.

- [HTML öğeleri](https://developer.mozilla.org/docs/Web/HTML/Element)
- [UI otomasyonunu kullanarak kodunuzu test etme](../test/use-ui-automation-to-test-your-code.md)
- [Kodlanmış UI testleri oluşturma](../test/use-ui-automation-to-test-your-code.md)
- [Kodlanmış UI testleri ve eylem kayıtları için desteklenen yapılandırmalar ve platformlar](../test/supported-configurations-and-platforms-for-coded-ui-tests-and-action-recordings.md)
