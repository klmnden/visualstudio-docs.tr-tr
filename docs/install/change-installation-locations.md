---
title: Yükleme konumlarını seçme
description: Sistem sürücünüzdeki yükleme ayak izini Visual Studio'nun konumunu indirme önbelleğini, paylaşılan bileşenler, SDK'ları ve araçları farklı sürücülere değiştirerek azaltmak öğrenin. Örneğin, bazı dosyalar C sürücüsündeki D sürücüye taşıyın.
ms.date: 03/30/2019
ms.custom: seodec18
ms.topic: conceptual
helpviewer_keywords:
- change installation locations for Visual Studio
- select an installation location for Visual Studio files
- move installation files to different drives
- use the D drive
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 651295d94a8125e26caa96b71ab438c62841ac10
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62974386"
---
# <a name="select-the-installation-locations-in-visual-studio"></a>Visual Studio'da yükleme konumları seçin

::: moniker range="vs-2019"

Bazı dosyalar için konumun değiştirerek sistem sürücünüzde Visual Studio yükleme ayak izini azaltabilir. Özellikle, indirme önbelleğini, paylaşılan bileşenler, SDK'lar ve Araçlar dosyaları için farklı bir konum kullanabilirsiniz.

::: moniker-end

::: moniker range="vs-2017"

**15.7 sürümündeki yeni**: Bazı dosyalar için konumun değiştirerek sistem sürücünüzde Visual Studio yükleme ayak izini azaltabilir. Özellikle, indirme önbelleğini, paylaşılan bileşenler, SDK'lar ve Araçlar dosyaları için farklı bir konum kullanabilirsiniz.

::: moniker-end

   > [!NOTE]
   > Bazı araçlar ve bunlar yüklenebileceği ile ilgili farklı kurallara sahip bir SDK'ları vardır. Başka bir konum seçin bile gibi araçları ve SDK'lar sistem sürücünüzde yüklenir.

Başlamaya hazır mısınız? İşte nasıl.

::: moniker range="vs-2017"

1. Visual Studio'yu yüklediğinizde seçin **yükleme konumlarını** sekmesi.

   ![Visual Studio 2017 - yükleme konumu seçin](media/vs-installation-locations.png "yükleme konumunu seçin.")

1. İçinde **Visual Studio IDE** bölümünde, varsayılanı kabul edin. Visual Studio temel ürünü yükler ve Visual Studio'nun bu sürümüne özgü dosyaları içerir.

   ![Yükleme konumlarını sekmesinde Visual Studio IDE bölümünü](media/vs-installation-locations-ide.png "yüklemeleri Konum sekmesini Visual Studio IDE bölümü için varsayılan değeri kabul edin.")

   > [!TIP]
   > Sistem sürücünüzdeki bir katı hal sürücüsü (SSD) ise, sistem sürücünüzde varsayılan konumu kabul etmenizi öneririz. Nedeni nedir? Visual Studio ile geliştirme yaptığınızda, okuma ve disk g/ç etkinliği artıran çok sayıda dosya, için yazma. Yükü işlemek için hızlı sürücünüze seçmek idealdir.

1. İçinde **indirme önbelleğini** bölümünde, indirme önbelleğini Tut ve kendi dosyalarını depolamak istediğiniz yere karar istediğinize karar verin.

     ![İndirme yükleme konumlarını sekmesinin önbellek bölümündeki](media/vs-installation-locations-cache.png "isteyip istemediğinizi belirleyin yüklemeden sonra indirme önbelleğini Tut ve ardından dosyaları depolamak istediğiniz sürücüyü belirtin.")

    1. İşaretleyin veya işaretini kaldırın **yüklemeden sonra indirme önbelleğini tut**.

       İndirme önbelleğini tutmamaya karar verirseniz, konum yalnızca geçici olarak kullanılır. Bu eylem kalmaz etkileyebilir veya önceki yüklemelerinden dosyaları silin.

    1. Yükleme dosyaları ve indirme önbelleğini bildirimlerinden depolamak istediğiniz sürücüyü belirtin.

        "C++ ile masaüstü geliştirme" iş yükünü seçin, örneğin, geçici olarak gereken boyut 1.58 yüklemesi tamamlandıktan hemen sonra serbest bırakılır sistem sürücüsünde GB'dir.

       > [!IMPORTANT]
       > Bu konum, ilk yükleme ile ayarlanır ve yükleyicisi kullanıcı arabirimini daha sonra değiştirilemez. Bunun yerine, şunları yapmalısınız [komut satırı parametrelerini](use-command-line-parameters-to-install-visual-studio.md) indirme önbelleğini taşınır.

1. İçinde **paylaşılan bileşenler, Araçlar ve SDK'lar** bölümünde, yan yana Visual Studio yüklemeleri tarafından paylaşılan dosyaları depolamak istediğiniz sürücüyü belirtin. SDK'lar ve araçlar da bu dizinde depolanır.

   ![Paylaşılan bileşenler, Araçlar ve SDK'lar bölümü yükleme konumlarını sekmesinin](media/vs-installation-locations-shared.png "paylaşılan bileşenler, Araçlar ve SDK'lar depolamak istediğiniz konumu belirtin.")

::: moniker-end

::: moniker range="vs-2019"

1. Visual Studio'yu yüklediğinizde seçin **yükleme konumlarını** sekmesi.

   ![Visual Studio 2019 - yükleme konumu seçin](media/vs-2019/vs-installer-installation-locations.png "yükleme konumunu seçin.")

1. İçinde **Visual Studio IDE** bölümünde, varsayılanı kabul edin. Visual Studio temel ürünü yükler ve Visual Studio'nun bu sürümüne özgü dosyaları içerir.

   > [!TIP]
   > Sistem sürücünüzdeki bir katı hal sürücüsü (SSD) ise, sistem sürücünüzde varsayılan konumu kabul etmenizi öneririz. Nedeni nedir? Visual Studio ile geliştirme yaptığınızda, okuma ve disk g/ç etkinliği artıran çok sayıda dosya, için yazma. Yükü işlemek için hızlı sürücünüze seçmek idealdir.

1. İçinde **indirme önbelleğini** bölümünde, indirme önbelleğini Tut ve kendi dosyalarını depolamak istediğiniz yere karar istediğinize karar verin.

    * İşaretleyin veya işaretini kaldırın **yüklemeden sonra indirme önbelleğini tut**.

       İndirme önbelleğini tutmamaya karar verirseniz, konum yalnızca geçici olarak kullanılır. Bu eylem kalmaz etkileyebilir veya önceki yüklemelerinden dosyaları silin.

    * Yükleme dosyaları ve indirme önbelleğini bildirimlerinden depolamak istediğiniz sürücüyü belirtin.

        "C++ ile masaüstü geliştirme" iş yükünü seçin, örneğin, geçici olarak gereken boyut 1.58 yüklemesi tamamlandıktan hemen sonra serbest bırakılır sistem sürücüsünde GB'dir.

       > [!IMPORTANT]
       > Bu konum, ilk yükleme ile ayarlanır ve yükleyicisi kullanıcı arabirimini daha sonra değiştirilemez. Bunun yerine, şunları yapmalısınız [komut satırı parametrelerini](use-command-line-parameters-to-install-visual-studio.md) indirme önbelleğini taşınır.

1. İçinde **paylaşılan bileşenler, Araçlar ve SDK'lar** bölümünde, "indirme önbelleği" bölümünde seçtiğiniz sürücüye kullandığına dikkat edin. Visual Studio yan yana Visual Studio yüklemeleri tarafından paylaşılan dosyaları depoladığı \Microsoft\VisualStudio\Shared dizindir. SDK'lar ve araçlar da bu dizinde depolanır.

::: moniker-end

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleyin](install-visual-studio.md)
* [Visual Studio’yu güncelleştirme](update-visual-studio.md)
* [Visual Studio’yu değiştirme](update-visual-studio.md)
* [Visual Studio'yu kaldırma](uninstall-visual-studio.md)
