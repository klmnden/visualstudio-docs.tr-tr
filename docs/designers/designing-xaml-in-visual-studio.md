---
title: Visual Studio 'da XAML tasarlama ve Blend
titleSuffix: ''
ms.date: 08/05/2019
ms.topic: conceptual
ms.assetid: 288e2415-9fcf-408e-bc35-9848315e14fd
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: cd0ff12b141a50872d586764d2b33bd68f3224fb
ms.sourcegitcommit: 90c3187d804ad7544367829d07ed4b47d3f8a72d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/06/2019
ms.locfileid: "68821874"
---
# <a name="design-xaml-in-visual-studio-and-blend-for-visual-studio"></a>Visual Studio ve Visual Studio için Blend XAML tasarlama

Visual Studio ve Visual Studio için Blend kullanıcı arabirimlerinin ilgi çekici yapı için görsel araçların sağlanmasına ve çeşitli uygulama türleri için XAML ile zengin medya deneyimlerini. Tümleşik geliştirme ortamları (IDE), Visual XAML Düzenleyicisi (Tasarımcı) dahil olmak üzere ortak bir özellikler kümesini paylaşır. WPF ve UWP platformlarını destekleyen Visual Studio için Blend, görsel durumlar tasarlamak ve animasyonlar oluşturmak için ek araçlar sağlar.

Visual Studio ile Visual Studio için Blend arasında geri dönebilir ve aynı projede her iki Ides içinde de aynı projeyi açabilmenize de sahip olabilirsiniz. Bir IDE 'deki XAML dosyalarına kaydedilen değişiklikler, diğer IDE 'ye geçtiğinizde otomatik yeniden yükleme yoluyla uygulanabilir. Her iki IDE 'deki **Araçlar** > **seçenekleri** > **ortam** > **belgeleri** ' ne giderek yeniden yükleme davranışını kontrol edebilirsiniz.

## <a name="installation"></a>Yükleme

- WPF uygulamaları oluşturmak için, Visual Studio 'da **.net masaüstü geliştirme** iş yükünü yüklemek. Visual Studio için Blend de yüklenecektir.
- UWP uygulamaları oluşturmak için, Visual Studio 'da **Evrensel Windows platformu geliştirme** iş yükünü yüklersiniz. Visual Studio için Blend de yüklenecektir.
- Xamarin. Forms uygulamaları oluşturmak için, Visual Studio 'da .NET iş yüküne **sahip mobil geliştirme** 'yı yüklersiniz. Visual Studio için Blend yüklü *değil* ; Blend, Xamarin. Forms uygulamalarını desteklemez.

## <a name="shared-capabilities"></a>Paylaşılan yetenekler

Çoğu temel geliştirme görevi için, Visual Studio ve Visual Studio için Blend, bazı hafif farklılıklar ile aynı Windows ve özellik kümesini paylaşır. Bazı önemli noktalar şunlardır:

- **IntelliSense** Her iki Ides de ifade tamamlama gibi IntelliSense özelliklerini destekler.

- **Hata ayıklama:** Çalışan bir uygulamada hata ayıklamak için kod noktalarını ayarlama ve uygulama çalışırken XAML kodunuzu değiştirmek için [sık yeniden yükleme](../debugger/xaml-hot-reload.md) kullanma dahil olmak üzere, [Visual Studio](../debugger/inspect-xaml-properties-while-debugging.md) ve [Visual Studio için Blend](../debugger/debug-xaml-in-blend.md)hata ayıklaması yapabilirsiniz. Visual Studio ile hata ayıklama tutarlı bir deneyim sağlamak için Visual Studio için Blend çoğu Visual Studio hata ayıklama windows ve araç çubuklarını içerir.

- **Dosya yeniden yükleme:** XAML dosyalarınızı, Visual Studio veya Visual Studio için Blend düzenleyebilirsiniz. Değiştirilmiş dosyalar, Ides 'ler arasında geçiş yaparken otomatik olarak yeniden yüklenir. Her iki IDE 'deki **Araçlar** > **seçenekleri** > **ortam** > **belgeleri** ' ne giderek yeniden yükleme davranışını kontrol edebilirsiniz.

- **Eşitlenmiş düzenler ve Ayarlar:** Visual Studio veya Visual Studio için Blend için özelleştirilmiş araç penceresi düzenleri ve ayarları tercihleri, aynı kişiselleştirme hesabıyla oturum açtığınızda cihazlarınız ve sürümleriniz arasında eşitlenir. Bkz: [birden fazla bilgisayara ayarları senkronize](../ide/synchronized-settings-in-visual-studio.md).

## <a name="advanced-capabilities-in-blend-for-visual-studio"></a>Visual Studio için Blend gelişmiş özellikleri

Üretkenliğinizi artırmak için aşağıdaki görevler için Visual Studio için Blend kullanarak göz önünde bulundurun. Bunlar, Visual Studio için Blend Visual Studio Tasarımcısı veya yalnızca koddan daha fazla işlevsellik sunduğu alanlardır.

| Görev | Visual Studio | Visual Studio için Blend | Daha fazla bilgi |
| - | - | - | - |
| **Görsel durumları tasarlama** | Görsel durumları tasarlamanıza yardımcı olacak bir araç yoktur; bunları programlı olarak oluşturmanız gerekir. | Bir denetimin görünüşünü durumuna göre değiştirmek için tasarım araçları 'nı kullanın. | [Görsel durumlar](modify-the-style-of-objects-in-blend.md#visual-states) |
| **Animasyonlar oluşturma** |Animasyon için tasarım aracı yoktur; bunları programlı olarak oluşturmanız gerekir. Bu, animasyon ve zamanlama sistemine WPF ve kodlama kapsamlı uzmanlığını'nın bilinmesini gerektirir.|Görsel animasyonlar oluşturur ve bunları Visual Studio için blend'de önizlemesini görebilirsiniz. Bu daha hızlı ve kod içinde animasyonları oluşturmak daha kesin değildir. Kullanıcı etkileşimi işlemek için Tetikleyiciler ekleyebilir ve olay işleyicileri ve diğer işlevler eklemek için kod geçiş yapabilirsiniz.|[Nesnelere animasyon ekleme](../designers/animate-objects-in-xaml-designer.md)|
|**Şekil ve metinler yolları daha kolay düzenlemesi için dönüştürün**|Desteklenmez.|Daha iyi düzenleme denetimi sağlayan yollar dönüştürerek (örneğin, dikdörtgenler ve elipsler) şekillere ince veya çarpıcı değişiklikler yapabilirsiniz. Şekillendirmek veya yolları birleştirme ve birden çok şekillerden bileşik yollar oluşturabilir.<br /><br />Ayrıca metin blokları vektör görüntüleri yönetileceğini yolları dönüştürebilirsiniz.|[Şekiller ve yollar çizme](../designers/draw-shapes-and-paths.md)|
|**Denetimleri, şablonlar ve stiller Düzenle**|Kodlama ve WPF stilleri ve şablonları bilinmesini gerektirir.|Herhangi bir görüntü denetime açın.<br /><br />Denetimleri, stilleri ve şablonları ile yalnızca birkaç tıklamayla değişiklik yapmak için şablon düzenleme araçlarını kullanın.<br /><br />Örneğin, Visual Studio stili kaynak için Blend (örneğin, düğmeler, liste kutuları, kaydırma çubukları, menüler, vb.) ortak WPF denetimleri uygulayın ve bunların renk, stil veya doğrudan Visual Studio için blend'de temel alınan şablonu değiştirmek için kullanabilirsiniz. İsterseniz daha sonra Son dokunuşları kodunu geçiş yapabilirsiniz.|[Nesnelerin stilini değiştirme](../designers/modify-the-style-of-objects-in-blend.md)|
|**Kullanıcı Arabirimi verilere bağlanma**|SQL Server veritabanı, WCF veya Web hizmeti, nesne veya SharePoint listesi gibi kaynaklardan bir veri kaynağı oluşturabilir ve ardından veri kaynağını UI denetimleriniz ile bağlayabilirsiniz.<br /><br />Tasarım zamanı veri bir etkileşimli bir tasarımı deneyimi için el ile oluşturulması gerekir.|.NET Framework uygulamalar için, Prototipleme ve test için kolayca örnek veriler oluşturun. Hazır olduğunuzda Canlı verilere geçme.<br /><br />Visual Studio'nun veri oluşturma özellikleri bekleyen için Blend (adlar, sayılar, URL'ler ve fotoğraf kolayca anında ekleyebilirsiniz), çok zaman tasarruf edebilirsiniz.<br /><br />Canlı verileri için bir XML dosyasına veya herhangi bir CLR veri kaynağı için kullanıcı Arabirimi denetimleri bağlayabilirsiniz.|[Verileri görüntüleme](../designers/display-data-in-blend.md)|

Gelişmiş XAML tasarımı hakkında daha fazla bilgi için bkz. [Visual Studio için Blend'i kullanarak kullanıcı Arabirimi oluşturma](../designers/creating-a-ui-by-using-blend-for-visual-studio.md).
