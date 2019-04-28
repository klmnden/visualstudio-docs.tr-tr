---
title: Paket önbelleğini devre dışı bırakma veya taşıma
description: Devre dışı bırakma, etkinleştirme veya Visual Studio dağıtımlar için paket önbelleğini taşıma konusunda bilgi edinin.
ms.date: 04/14/2017
ms.custom: seodec18
ms.topic: conceptual
f1_keywords:
- cache
- nocache
helpviewer_keywords:
- '{{PLACEHOLDER}}'
- '{{PLACEHOLDER}}'
ms.assetid: 2429993A-3F0E-41C5-9562-FEA6AE994440
author: heaths
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 47793cff733d84634c79355fb7639dbdad1cd82f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62974250"
---
# <a name="disable-or-move-the-package-cache"></a>Paket önbelleğini devre dışı bırakma veya taşıma

Visual Studio veya Internet bağlantısı yok sahip olduğu durumlarda ilgili diğer ürünleri onarmak gerektiği durumlarda paket önbelleğini yüklü paketleri kaynağı sağlar. Bazı sürücüler veya sistem ile çıkarır, ancak değil isteyebilirsiniz bu paketleri geçici olarak tutun.
Yükleyici, bunları kaydetme veya disk alanını kurtarmak istiyorsanız, devre dışı bırakın veya paket önbelleğini taşıma, gerektiğinde indirir.

## <a name="disable-the-package-cache"></a>Paket önbelleğini devre dışı bırak

Yükleme, değiştirme veya Visual Studio ya da diğer ürünlerle yeni yükleyici onarmak için önce Yükleyici ile başlayabilirsiniz `--nocache` Yükleyici'ye geçiş yapın.

```cmd
"%ProgramFiles(x86)%\Microsoft Visual Studio\Installer\vs_installer.exe" --nocache
```

Herhangi bir ürün üzerinde yaptığınız herhangi bir işlem bunlar yüklendikten sonra herhangi bir paket kaydetme kaçınır ve bu ürünün mevcut tüm paketler kaldırılır. Değiştirdiğinizde ya da Visual Studio'yu onarmak ve paketleri gereklidir, bunlar otomatik olarak indirilir ve bunlar yüklendikten sonra kaldırıldı.

Önbellek yeniden etkinleştirmek istiyorsanız, `--cache` yerine. Tüm paketleri geri yüklemeniz gerekirse, ağınızdan bağlantısını kesmeden önce Visual Studio'yu onarmak böylece gerekli olan paketleri önbelleğe alınır.

```cmd
"%ProgramFiles(x86)%\Microsoft Visual Studio\Installer\vs_installer.exe" repair --passive --norestart --cache
```

Ayrıca `KeepDownloadedPayloads` [kayıt defteri ilke](set-defaults-for-enterprise-deployments.md) yükleme, değiştirme veya Visual Studio'yu onarmak için önce önbellek devre dışı bırakmak için.

## <a name="move-the-package-cache"></a>Paket önbelleğini taşıma

Ortak bir sistem yapılandırması, bir SSD ile daha geniş bir sabit diske (veya daha fazla) yüklü Windows geliştirmesi için kaynak kodu, program ikili dosyaları ve daha fazlası gibi olmalıdır değil. Çevrimdışı çalışmak istiyorsanız, bunun yerine paket önbelleğini taşıyabilirsiniz.

Yalnızca şu anda, bunu yapabilirsiniz `CachePath` [kayıt defteri ilke](set-defaults-for-enterprise-deployments.md) yükleme, değiştirme veya Visual Studio'yu onarmak için önce.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleyin](install-visual-studio.md)
* [Kuruluş dağıtımları için varsayılanları ayarlama](set-defaults-for-enterprise-deployments.md)
* [Komut satırı parametrelerini kullanarak Visual Studio'yu yükleme](use-command-line-parameters-to-install-visual-studio.md)
