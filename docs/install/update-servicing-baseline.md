---
title: Bakım temeli sırasında Visual Studio’yu güncelleştirme
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
ms.openlocfilehash: bf167c46e9b7dd9317278c7ce388977c4cc9428a
ms.sourcegitcommit: f369ff7e84b0216f01570a486c7be80ca6d0e61a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/16/2019
ms.locfileid: "68250325"
---
# <a name="update-visual-studio-while-on-a-servicing-baseline"></a>Bakım temeli sırasında Visual Studio’yu güncelleştirme

Visual Studio 2019 sık güncelleştirmeler sırasında olacaktır, [ürün yaşam döngüsü](/visualstudio/productinfo/release-rhythm#release-channel-updates). Yeni özellikler ve bileşenler eklemeleri her iki alt sürüm güncelleştirmeleri (örneğin, gelen 16,0 16.1 için) güncelleştirmelerini içerir ve kritik sorunlar için düzeltmeler hedeflenen hizmet yalnızca içeren güncelleştirmeleri (örneğin, 16.0.4 16.0.5 için).

Kuruluş Yöneticileri, hizmet bir taban çizgisine göre istemcileri tutmak seçebilirsiniz. Hizmet temel sonraki bakım temel sürümü geçen yıl boyunca güncelleştirmelerin uygulanması ile desteklenir.

Hizmet temel seçeneği, geliştiricilerin ve yöneticilerin yeni özellikler, hata düzeltmeleri veya yeni ikincil güncelleştirmelerinde bileşenleri benimsemek için daha fazla esneklik sunar. İlk hizmet temel 16.0.x ' dir. Daha fazla bilgi için [Kurumsal ve profesyonel müşterileri için destek seçenekleri](https://docs.microsoft.com/visualstudio/releases/2019/servicing#support-options-for-enterprise-and-professional-customers).

## <a name="how-to-get-onto-a-servicing-baseline"></a>Bir hizmet temeli alma

Hizmet temel kullanmaya başlamak için gelen bir sabit sürümü Visual Studio yükleyicisi önyükleyici indirme [My.VisualStudio.com](https://my.visualstudio.com/Downloads?q=visual%20studio%202019%20version%2016.0). Önyükleyiciler ile bağlantılar ürün yapılandırmaları, iş yükleri ve bileşenleri için belirli bir sürüm var.

> [!NOTE]
> Sabit sürüm önyükleyici ve standart Önyükleyiciler ile ayırt etmek dikkatli olun. Visual Studio'nun en son sürümü kullanmak için standart Önyükleyiciler ile yapılandırılır. Standart boostrappers birkaç dosya adı (örneğin, vs_enterprise__123456789-123456789.exe) sahip olduğunda karşıdan My.VisualStudio.com.

Yükleme sırasında kurumsal yöneticiler, istemcilerin en son sürümüne güncelleştirmesini engellemek için istemcileri yapılandırmanız gerekir. İstemciler birden çok yolla yapılandırabilirsiniz:
- [Değişiklik `channelUri` yanıt yapılandırma dosyasında ayarı](update-servicing-baseline.md#install-a-servicing-baseline-on-a-network) düzeni veya yerel klasör kanal bildiriminde kullanılacak.
- [Komut satırı yürütme aracılığıyla Channelurı değiştirme](update-servicing-baseline.md#install-a-servicing-baseline-via-the-internet) varolmayan bir dosyayı kullanmak için.
- [İstemci sisteminde güncelleştirmeler devre dışı bırakmak için ilkeler ayarlama](update-servicing-baseline.md#use-policy-settings-to-disable-clients-from-updating), istemciler kendi kendini güncelleştirme önlemek için.

### <a name="install-a-servicing-baseline-on-a-network"></a>Hizmet temel bir ağ üzerinde yükleme

Bir ağ düzeni yükleme yöneticileri değiştirme `channelUri` değerini *response.json* düzenin dosyasında *channelmanifest.json* aynı klasörde bulunan dosya. Adımlar için bkz: [ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetlemek](controlling-updates-to-visual-studio-deployments.md). Değiştirme `channelUri` değeri güncelleştirmeleri düzeni konumunda aramak istemcileri etkinleştirir.

### <a name="install-a-servicing-baseline-via-the-internet"></a>İnternet üzerinden hizmet temel yükleme

İnternet tabanlı bir yükleme için ekleme `--channelUri` kurulumu başlatmak için komut satırı için bildirimi var olmayan kanalıyla kullanılan. Bu Visual Studio kullanarak en son kullanılabilir sürüm için güncelleştirme devre dışı bırakır. Örnek buradadır:

```cmd
vs_enterprise.exe --channelUri c:\doesnotexist.chman
```

### <a name="use-policy-settings-to-disable-clients-from-updating"></a>İlke ayarları güncelleştiriliyor ve istemcilerin devre dışı bırakma

Bir istemci güncelleştirmeleri denetlemek için başka bir seçenek [güncelleştirme bildirimleri kapatmak](controlling-updates-to-visual-studio-deployments.md). Channelurı'nin değeri yüklemesinde değiştirilmedi varsa bu seçeneği kullanın. İstemci bağlantıları için sunulan en son sürüme almasını devre dışı bırakır. Bir sabit sürüm önyükleyici istemci belirli bir sürüme güncelleştirmek hala gereklidir.

## <a name="how-to-stay-on-a-servicing-baseline"></a>Hizmet bir taban çizgisine göre kalmak nasıl

Hizmet bir taban çizgisi için bir güncelleştirme kullanılabilir olduğunda, sabit sürüm önyükleyici dosyalarını bakım güncelleştirme için kullanılabilir hale getirilir [My.VisualStudio.com](https://my.visualstudio.com/Downloads?q=visual%20studio%202019%20version%2016.0).

Yöneticiler ağ düzeni dağıtma yüklemek için yönetici güncelleştirmek isteyebilirsiniz [yerleşimi konumu](update-a-network-installation-of-visual-studio.md). Konum yüklü istemcileri güncelleştirme bildirimlerini alır. Güncelleştirme istemcilere dağıtılması gerekiyorsa izleyin [bu yönergeleri](update-a-network-installation-of-visual-studio.md#how-to-deploy-an-update-to-client-machines). Bir güncelleştirme için 'response.json' değiştirirken ek iş yüklerinin, bileşenleri ve dil eklemeyin. Ürün güncelleştirildikten sonra bu ayarları yönetme 'Değiştir' dağıtım olarak yapılmalıdır.

Yeni sabit sürüm önyükleyici ile internet üzerinden yükleme için çalıştırma `--channelUri` istemci var olmayan kanal bildiriminde işaret eden bir parametre. Güncelleştirme Sessiz ya da pasif modunda dağıtılmış olan iki ayrı komutları kullanın:

1. Visual Studio Yükleyicisi güncelleştirmesi:

    ```cmd
    vs_enterprise.exe --quiet --update
    ```

2. Visual Studio uygulamasını güncelleştirin:

    ```cmd
    vs_enterprise.exe update --installPath "C:\Program Files (x86)\Microsoft Visual Studio\2019\Enterprise" --quiet --wait --norestart --channelUri c:\doesnotexist.chman
    ```

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleyin](install-visual-studio.md)
* [Visual Studio Yönetici Kılavuzu](visual-studio-administrator-guide.md)
* [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
* [Visual Studio örneklerini algılamaya ve yönetmeye yönelik araçlar](tools-for-managing-visual-studio-instances.md)
* [Yanıt dosyasında ayarları tanımlama](automated-installation-with-response-file.md)
* [Ağ tabanlı Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md)
* [Visual Studio ürün yaşam döngüsü ve Bakım](/visualstudio/releases/2019/servicing/)
