---
title: Bakım temeli sırasında Visual Studio’yu güncelleştirme
titleSuffix: ''
description: Hizmet bir taban çizgisine göre kalsanız Visual Studio güncelleştirme hakkında bilgi edinin.
ms.date: 05/22/2019
ms.custom: seodec18
ms.topic: conceptual
ms.assetid: ''
author: doughall
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 36bbec66e822d7e1daebcadbeeba30e166747368
ms.sourcegitcommit: aeb1a1135dd789551e15aa5124099a5fe3f0f32b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66501126"
---
# <a name="update-visual-studio-while-on-a-servicing-baseline"></a>Bakım temeli sırasında Visual Studio’yu güncelleştirme

Visual Studio 2019 sık güncelleştirmeler sırasında olacaktır, [ürün yaşam döngüsü](/visualstudio/productinfo/release-rhythm#release-channel-updates). Bu, her iki alt sürüm güncelleştirmeleri dahil edilir (örneğin: 16,0 16.1 için) yeni özellikleri ve bileşenleri ve hizmet güncelleştirmeleri içerebilir (örneğin: 16.0.4 için 16.0.5) içeren, yalnızca kritik sorunlar için düzeltmeler hedeflenen. 

Kuruluş Yöneticileri, sonraki bakım temel sürümü geçen yıl boyunca güncelleştirmelerin uygulanması ile desteklenen bir bakım taban istemcileri korumak seçebilirsiniz. Bu yeni özellikler, hata düzeltmeleri veya yeni ikincil güncelleştirmelerinde bileşenleri benimsemek, geliştiriciler ve Yöneticiler için daha fazla esneklik sağlar. İlk hizmet temel 16.0.x ' dir. Bkz: [Kurumsal ve profesyonel müşterileri için destek seçenekleri](https://docs.microsoft.com/visualstudio/releases/2019/servicing#support-options-for-enterprise-and-professional-customers) daha fazla bilgi için.

## <a name="how-to-get-onto-a-servicing-baseline"></a>Bir hizmet temeli alma

Hizmet temel kullanmaya başlamak için gelen bir sabit sürümü Visual Studio yükleyicisi önyükleyici indirme [My.VisualStudio.com](https://my.visualstudio.com/Downloads?q=visual%20studio%202019%20version%2016.0). Bu Önyükleyiciler ile bağlantılar ürün yapılandırmaları, iş yükleri ve bileşenleri için belirli bir sürüm var. 

> [!NOTE]
> Düzeltilmiş sürümü önyükleyici ve normal Önyükleyiciler ile ayırt etmek dikkatli olun. Visual Studio'nun en son sürümü kullanmak için normal Önyükleyiciler ile yapılandırılır. Bunlar dosya adında bir sayıya sahip (örneğin: vs_enterprise__123456789 123456789.exe) my.visualstudio.com yüklendiğinde.

Yükleme sırasında kuruluş yöneticileri istemcileri en son sürüme güncelleştirilmesini önlemek için yapılandırmanız gerekir. Bunu aşağıdaki yöntemlerle yapabilirsiniz [yanıt yapılandırma dosyasındaki Channelurı ayarı değiştirmeden](update-servicing-baseline.md#install-a-servicing-baseline-on-a-network) düzeni veya yerel klasör, kanal bildiriminde tarafından kullanılacak [komut satırı yürütmearacılığıylaChannelurıdeğiştirme](update-servicing-baseline.md#install-a-servicing-baseline-via-the-internet)bir mevcut olmayan dosyasını kullanmak için ya da [güncelleştirmeleri devre dışı bırakmak için İstemci sisteminde ilkelerini ayarlama](update-servicing-baseline.md#use-policy-settings-to-disable-clients-from-updating) istemcilerin kendi kendini güncelleştirme önlemek için. 

### <a name="install-a-servicing-baseline-on-a-network"></a>Hizmet temel bir ağ üzerinde yükleme

Yöneticiler ağ düzeni kullanarak yüklemek için Channelurı değerinde değişiklik `response.json` aynı klasörde bulunan channelmanifest.json kullanılacak düzeni. Bkz: [ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetlemek](controlling-updates-to-visual-studio-deployments.md) yönelik adım adım yönergeler. Channelurı'nin değiştirme güncelleştirmeleri düzeni konumunda aramak istemcileri etkinleştirir. 

### <a name="install-a-servicing-baseline-via-the-internet"></a>İnternet üzerinden hizmet temel yükleme

Bir Internet tabanlı yükleme ise, ekleme `--channelUri` kurulumu başlatmak için komut satırı için bildirimi var olmayan kanalıyla kullanılan. Bu Visual Studio kullanarak en son kullanılabilir sürüm için güncelleştirme devre dışı bırakır. Aşağıda bir örnek verilmiştir:

  ```cmd
   vs_enterprise.exe --channelUri c:\doesnotexist.chman 
  ```

### <a name="use-policy-settings-to-disable-clients-from-updating"></a>İlke ayarları güncelleştiriliyor ve istemcilerin devre dışı bırakma

Bir istemci güncelleştirmeleri denetlemek için başka bir seçenek [güncelleştirme bildirimleri kapatmak](controlling-updates-to-visual-studio-deployments.md). Channelurı'nin değeri yükle değiştirilmedi varsa bu seçeneği kullanın. İstemci bağlantıları için sunulan en son sürüme almasını devre dışı bırakır. Düzeltilmiş sürümü önyükleyici istemci belirli bir sürüme güncelleştirmek hala gereklidir.

## <a name="how-to-stay-on-a-servicing-baseline"></a>Hizmet bir taban çizgisine göre kalmak nasıl

Hizmet bir taban çizgisi için bir güncelleştirme olduğunda, sabit sürüm önyükleyici dosyalarını bakım güncelleştirmeyi için kullanılabilir hale getirilir [My.VisualStudio.com](https://my.visualstudio.com/Downloads?q=visual%20studio%202019%20version%2016.0). Bunlar, çeşitli senaryolarda kullanılabilir.

Yöneticiler ağ düzeni dağıtma yüklemek için yönetici güncelleştirmek isteyebilirsiniz [yerleşimi konumu](update-a-network-installation-of-visual-studio.md). Konum yüklü istemcileri güncelleştirme bildirimlerini alır. Güncelleştirme istemcilere dağıtılması gerekiyorsa izleyin [bu yönergeleri](update-a-network-installation-of-visual-studio.md#how-to-deploy-an-update-to-client-machines). Bir güncelleştirme için 'response.json' değiştirirken ek iş yüklerinin, bileşenleri ve dil eklemeyin. Ürün güncelleştirildikten sonra bu ayarları yönetme 'Değiştir' dağıtım olarak yapılmalıdır. 

Bir Internet tabanlı yükleme ise, yeni sabit sürüm önyükleyici ile çalıştırma `--channelUri` istemci var olmayan kanal bildiriminde işaret eden bir parametre. Güncelleştirme Sessiz ya da pasif modunda dağıtılmış olan iki ayrı komutları kullanın:

1. İlk olarak, Visual Studio Yükleyicisi güncelleştirmesi: <br>```vs_enterprise.exe --quiet --update```
2. Ardından, Visual Studio uygulamasını güncelleştirin: <br>```vs_enterprise.exe update --installPath "C:\Program Files (x86)\Microsoft Visual Studio\2019\Enterprise" --quiet --wait --norestart --channelUri c:\doesnotexist.chman```

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleyin](install-visual-studio.md)
* [Visual Studio Yönetici Kılavuzu](visual-studio-administrator-guide.md)
* [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
* [Visual Studio örneklerini algılamaya ve yönetmeye yönelik araçlar](tools-for-managing-visual-studio-instances.md)
* [Yanıt dosyasında ayarları tanımlama](automated-installation-with-response-file.md)
* [Ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md)
* [Visual Studio ürün yaşam döngüsü ve Bakım](/visualstudio/releases/2019/servicing/)
