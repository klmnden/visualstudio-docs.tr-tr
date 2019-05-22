---
title: Visual Studio yönetici kılavuzu
titleSuffix: ''
description: Visual Studio bir kuruluş ortamında dağıtma hakkında daha fazla bilgi edinin.
ms.date: 05/22/2019
ms.custom: seodec18
ms.topic: conceptual
helpviewer_keywords:
- network installation, Visual Studio
- administrator guide, Visual Studio
- installing Visual Studio, administrator guide
ms.assetid: 4af353f5-6cfd-4ebe-bcfb-f42306e451a0
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 61b3a2dfae667bac7c3a6a62682cdbd5b1a5feb4
ms.sourcegitcommit: cd21b38eefdea2cdefb53e68e7a30b868e78dd6b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/22/2019
ms.locfileid: "66037505"
---
# <a name="visual-studio-administrator-guide"></a>Visual Studio yönetici kılavuzu

Kurumsal ortamlarda, sistem yöneticileri genellikle yüklemeleri için son kullanıcıların bir ağ paylaşımından veya sistem yönetim yazılımının kullanarak dağıtın. Sistem yöneticileri yükleme işlemi sırasında ürün anahtarlarını dağıtmak için yükleme Varsayılanları, önceden yapılandırmak için bir ağ yükleme konumuna oluşturma olanağı sağlayarak kurumsal dağıtım desteklemek için Visual Studio Kurulum altyapısı tasarladık ve başarılı bir dağıtımı sonrasında ürün güncelleştirmelerini yönetmek için.

Bu Yönetici Kılavuzu, ağa bağlı ortamlarda kurumsal dağıtım için senaryo tabanlı rehberlik sağlar.

## <a name="before-you-begin"></a>Başlamadan önce

Kuruluşunuz genelinde Visual Studio dağıtmadan önce almanız gereken karar ve görevlerinin tamamlanması için birkaç vardır:

::: moniker range="vs-2019"

* Her hedef bilgisayar karşıladığından emin olun [minimum yükleme gereksinimlerini](/visualstudio/releases/2019/system-requirements/).

* Bakım gereksinimlerinizi karar verin.

  Şirketiniz açık kalmasını gerektiriyorsa iş artık ancak hala ayarlanmış bir özelliği düzenli bakım güncelleştirmeleri almak için hizmet temel kullanmayı planlıyorsanız istiyor. Daha fazla bilgi için ***Kurumsal ve profesyonel müşterilere yönelik destek seçenekleri*** bölümünü [Visual Studio ürün yaşam döngüsü ve Bakım](/visualstudio/releases/2019/servicing#support-options-for-enterprise-and-professional-customers) sayfası.

  Ardından toplu özellik güncelleştirmeleri ile birlikte hizmet güncelleştirmeleri uygulamayı planlıyorsanız, en yeni güncelleştirmeleri seçebilirsiniz.

* Bir güncelleştirme modeli karar verin.

  Burada tek tek istemci makinelerin güncelleştirmeleri almak istiyor musunuz? Özellikle, internet'ten veya şirket geneli yerel paylaşımından güncelleştirmeleri almak istediğinize karar verin. Ardından, yerel paylaşımına kullanmayı seçerseniz, bireysel kullanıcılar kendi istemcileri güncelleştirilip güncelleştirilemeyeceğini veya istemcilerini programlı bir şekilde güncelleştirmek için bir yönetici isteyip istemediğinizi karar verin.

* Karar [iş yüklerinin ve bileşenlerin](workload-and-component-ids.md?view=vs-2019) şirketinizin gereksinimlerine.

* Kullanmak için bir [yanıt dosyası](automated-installation-with-response-file.md?view=vs-2019) (Bu betiğin yönetme ayrıntılarında basitleştirir).

* Grup İlkesi'ni etkinleştirmek istiyorsanız ve tek tek bilgisayarlarda müşteri geri bildirimleri devre dışı bırakmak için Visual Studio yapılandırmak istiyorsanız karar verin.

::: moniker-end

::: moniker range="vs-2017"

* Her hedef bilgisayar karşıladığından emin olun [minimum yükleme gereksinimlerini](/visualstudio/productinfo/vs2017-system-requirements-vs/).

* Bakım gereksinimlerinizi karar verin.

  Şirketiniz açık kalmasını gerektiriyorsa iş artık ancak hala ayarlanmış bir özelliği düzenli bakım güncelleştirmeleri almak için hizmet temel kullanmayı planlıyorsanız istiyor. Daha fazla bilgi için ***Visual Studio'nun eski sürümleri için destek*** bölümünü [Visual Studio ürün yaşam döngüsü ve Bakım](/visualstudio/releases/2019/servicing#support-for-older-versions-of-visual-studio) sayfası.

  Ardından toplu özellik güncelleştirmeleri ile birlikte hizmet güncelleştirmeleri uygulamayı planlıyorsanız, en yeni güncelleştirmeleri seçebilirsiniz.

* Bir güncelleştirme modeli karar verin.

  Burada tek tek istemci makinelerin güncelleştirmeleri almak istiyor musunuz? Özellikle, internet'ten veya şirket geneli yerel paylaşımından güncelleştirmeleri almak istediğinize karar verin. Ardından, yerel paylaşımına kullanmayı seçerseniz, bireysel kullanıcılar kendi istemcileri güncelleştirilip güncelleştirilemeyeceğini veya istemcilerini programlı bir şekilde güncelleştirmek için bir yönetici isteyip istemediğinizi karar verin.

* Karar [iş yüklerinin ve bileşenlerin](workload-and-component-ids.md?view=vs-2017) şirketinizin gereksinimlerine.

* Kullanmak için bir [yanıt dosyası](automated-installation-with-response-file.md?view=vs-2017) (Bu betiğin yönetme ayrıntılarında basitleştirir).

* Grup İlkesi'ni etkinleştirmek istiyorsanız ve tek tek bilgisayarlarda müşteri geri bildirimleri devre dışı bırakmak için Visual Studio yapılandırmak istiyorsanız karar verin.

::: moniker-end

::: moniker range="vs-2019"

## <a name="step-1---download-visual-studio-product-files"></a>1. adım - Visual Studio ürün dosyalarını indirme

* [İş yüklerinin ve bileşenlerin seçin](workload-and-component-ids.md?view=vs-2019) yüklemek istediğiniz.

* [Visual Studio ürün dosyaları için bir ağ paylaşımı oluşturmanız](create-a-network-installation-of-visual-studio.md?view=vs-2019).

## <a name="step-2---build-an-installation-script"></a>2. adım - bir yükleme komut dosyası derleme

* Yapı kullanan bir yükleme betiği [komut satırı parametreleri](use-command-line-parameters-to-install-visual-studio.md?view=vs-2019) yükleme denetlemek için.

  >[!NOTE]
  > Betikleri kullanarak basitleştirebilirsiniz bir [yanıt dosyası](automated-installation-with-response-file.md?view=vs-2019). Varsayılan yükleme seçeneğini içeren bir yanıt dosyası oluşturduğunuzdan emin olun.

* (İsteğe bağlı) [Bir toplu lisans ürün anahtarını uygulayan](automatically-apply-product-keys-when-deploying-visual-studio.md?view=vs-2019) yüklemesinin bir parçası olarak kullanıcılar yazılım ayrı olarak etkinleştirmeniz gerekmez, komut dosyası.

* (İsteğe bağlı) Güncelleştirmek için ağ düzeni [ne zaman ve nerede ürün güncelleştirmeleri kullanıcılarınıza dağıtılır denetim](controlling-updates-to-visual-studio-deployments.md?view=vs-2019).

* (İsteğe bağlı) Visual Studio gibi diğer sürümleri veya örnekleri ile paylaşılan bazı paketler yüklendiği dağıtımını etkileyen kayıt defteri ilkeler ayarlama [paketlerin önbelleğe](set-defaults-for-enterprise-deployments.md?view=vs-2019) veya [paketleri önbelleğe alınmışolup](disable-or-move-the-package-cache.md?view=vs-2019).

* (İsteğe bağlı) Grup İlkesi ayarlama. Ayrıca [müşteri geri bildirimleri devre dışı bırakmak için Visual Studio'yu yapılandırma](../ide/visual-studio-experience-improvement-program.md) tek tek bilgisayarlarda.

## <a name="step-3---deploy"></a>3. adım - dağıtma

* Betiğinizi, hedef Geliştirici iş istasyonları üzerinde yürütmek için tercih ettiğiniz dağıtım teknolojiyi kullanın.

## <a name="step-4---deploy-updates"></a>4. adım - güncelleştirmeleri dağıtma

* [En son güncelleştirmeleri içeren ağ konumunuza Yenile](update-a-network-installation-of-visual-studio.md?view=vs-2019) Visual Studio, kullandığınız komutunu çalıştırarak güncelleştirilmiş bileşenleri eklemek için düzenli olarak adım 1.

  Visual Studio güncelleştirme betiğini kullanarak güncelleştirebilirsiniz. Bunu yapmak için [ `update` ](use-command-line-parameters-to-install-visual-studio.md?view=vs-2019) komut satırı parametresi.

## <a name="step-5---optional-use-visual-studio-tools"></a>5. adım - (isteğe bağlı) kullanın, Visual Studio Araçları

Yardımcı olacak çeşitli araçlar sunuyoruz [algılamak ve yüklü Visual Studio Örnekleri yönetme](tools-for-managing-visual-studio-instances.md?view=vs-2019) istemci makinelerinde.

::: moniker-end

::: moniker range="vs-2017"

## <a name="step-1---download-visual-studio-product-files"></a>1. adım - Visual Studio ürün dosyalarını indirme

* [İş yüklerinin ve bileşenlerin seçin](workload-and-component-ids.md?view=vs-2017) yüklemek istediğiniz.

* [Visual Studio ürün dosyaları için bir ağ paylaşımı oluşturmanız](create-a-network-installation-of-visual-studio.md?view=vs-2017).

## <a name="step-2---build-an-installation-script"></a>2. adım - bir yükleme komut dosyası derleme

* Yapı kullanan bir yükleme betiği [komut satırı parametreleri](use-command-line-parameters-to-install-visual-studio.md?view=vs-2017) yükleme denetlemek için.

  >[!NOTE]
  > Betikleri kullanarak basitleştirebilirsiniz bir [yanıt dosyası](automated-installation-with-response-file.md?view=vs-2017). Varsayılan yükleme seçeneğini içeren bir yanıt dosyası oluşturduğunuzdan emin olun.

* (İsteğe bağlı) [Bir toplu lisans ürün anahtarını uygulayan](automatically-apply-product-keys-when-deploying-visual-studio.md?view=vs-2017) yüklemesinin bir parçası olarak kullanıcılar yazılım ayrı olarak etkinleştirmeniz gerekmez, komut dosyası.

* (İsteğe bağlı) Güncelleştirmek için ağ düzeni [ne zaman ve nerede ürün güncelleştirmeleri kullanıcılarınıza dağıtılır denetim](controlling-updates-to-visual-studio-deployments.md?view=vs-2017).

* (İsteğe bağlı) Visual Studio gibi diğer sürümleri veya örnekleri ile paylaşılan bazı paketler yüklendiği dağıtımını etkileyen kayıt defteri ilkeler ayarlama [paketlerin önbelleğe](set-defaults-for-enterprise-deployments.md?view=vs-2019) veya [paketleri önbelleğe alınmışolup](disable-or-move-the-package-cache.md?view=vs-2017).

* (İsteğe bağlı) Grup İlkesi ayarlama. Ayrıca [müşteri geri bildirimleri devre dışı bırakmak için Visual Studio'yu yapılandırma](../ide/visual-studio-experience-improvement-program.md) tek tek bilgisayarlarda.

## <a name="step-3---deploy"></a>3. adım - dağıtma

* Betiğinizi, hedef Geliştirici iş istasyonları üzerinde yürütmek için tercih ettiğiniz dağıtım teknolojiyi kullanın.

## <a name="step-4---deploy-updates"></a>4. adım - güncelleştirmeleri dağıtma

* [En son güncelleştirmeleri içeren ağ konumunuza Yenile](update-a-network-installation-of-visual-studio.md?view=vs-2017) Visual Studio, kullandığınız komutunu çalıştırarak güncelleştirilmiş bileşenleri eklemek için düzenli olarak adım 1.

  Visual Studio güncelleştirme betiğini kullanarak güncelleştirebilirsiniz. Bunu yapmak için [ `update` ](use-command-line-parameters-to-install-visual-studio.md?view=vs-2019) komut satırı parametresi.

## <a name="step-5---optional-use-visual-studio-tools"></a>5. adım - (isteğe bağlı) kullanın, Visual Studio Araçları

Yardımcı olacak çeşitli araçlar sunuyoruz [algılamak ve yüklü Visual Studio Örnekleri yönetme](tools-for-managing-visual-studio-instances.md?view=vs-2017) istemci makinelerinde.

::: moniker-end

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Komut satırı parametresi örnekleri](command-line-parameter-examples.md)
* [Visual Studio'yu çevrimdışı yükleme için gerekli sertifikaları yükleme](install-certificates-for-visual-studio-offline.md)
* [İçeri veya dışarı aktarmayı Yükleme Yapılandırması](import-export-installation-configurations.md)
* [Visual Studio Kurulum arşivleri](https://devblogs.microsoft.com/setup/tag/vs2017/)
* [Visual Studio ürün yaşam döngüsü ve Bakım](/visualstudio/releases/2019/servicing/)
* [Zaman uyumlu otomatik yükleme ayarları](../extensibility/synchronously-autoloaded-extensions.md)
