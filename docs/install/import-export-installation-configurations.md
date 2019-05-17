---
title: Yükleme yapılandırmasını içeri veya dışarı aktarma
titleSuffix: ''
description: Başkalarıyla paylaşmak için .vsconfig dosyaya yükleme yapılandırmanızı dışarı aktarma ve kopyalamak için içeri aktarma öğrenin.
ms.date: 05/18/2019
ms.topic: conceptual
f1_keywords:
- vs.about
helpviewer_keywords:
- import installation configuration
- export installation configuration
- install Visual Studio
- Visual Studio installer
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.openlocfilehash: 8150aa3369eb385ebad865d261f9e8c2d71d7dbe
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65849031"
---
# <a name="import-or-export-installation-configurations"></a>Yükleme yapılandırmasını içeri veya dışarı aktarma

Visual Studio yükleme yapılandırma dosyaları ile kuruluşunuz genelinde yapılandırabilirsiniz. Bunu yapmak için yalnızca iş yükü ve bileşen bilgileri .vsconfig dosya Visual Studio Yükleyicisi'ni kullanarak dışarı aktarın. Ardından, yeni veya mevcut yüklemelerde yapılandırmayı içeri aktarmak ve çok diğerleri ile paylaşabilirsiniz.

İşte nasıl.

::: moniker range="vs-2017"

> [!NOTE]
> Bu işlev, yalnızca Visual Studio 2017 sürüm 15.9 kullanılabilir ve üzerinde desteklenir.

::: moniker-end

## <a name="export-a-configuration"></a>Bir yapılandırmayı Dışarı Aktar

Visual Studio'nun önceden yüklenmiş örnek veya şu anda yüklemekte olduğunuz bir yükleme yapılandırma dosyasını dışarı aktarmak seçebilirsiniz.

1. Visual Studio Yükleyicisi'ni açın.

1. Ürün kartında seçin **daha fazla** düğmesini ve ardından **dışarı aktarma Yapılandırması**.

   ![Visual Studio Yükleyicisi'nde ürün kartından dışarı aktarma yapılandırması](../install/media/vs-2019/vs-installer-export-config.png)

1. .Vsconfig dosyanızı kaydedin ve ardından istediğiniz konumu yazın veya gözatın **gözden geçirme ayrıntıları**.

   ![Visual Studio Yükleyicisi'nden yapılandırmayı Dışarı Aktar](../install/media/vs-2019/export-configuration-confirmation.png)

1. İstediğiniz bileşenleri ve iş yüklerini var olduğundan emin olun ve ardından **dışarı**.

## <a name="import-a-configuration"></a>Yapılandırma içeri aktarma

Bir yükleme yapılandırma dosyasını içeri aktarmak hazır olduğunuzda, aşağıdaki adımları izleyin.

1. Visual Studio Yükleyicisi'ni açın.

1. Ürün kartında seçin **daha fazla** düğmesini ve ardından **alma Yapılandırması**.

1. İçeri aktarma ve ardından istediğiniz .vsconfig dosyayı bulun **gözden geçirme ayrıntıları**.

1. İstediğiniz bileşenleri ve iş yüklerini var olduğundan emin olun ve ardından **Kapat**.

::: moniker range="vs-2019"

## <a name="automatically-install-missing-components"></a>Otomatik olarak eksik bileşenleri yükler

**Yeni Visual Studio 2019**: Çözüm kök dizininizde bir .vsconfig dosyasını kaydedin ve ardından bir çözüm açın, Visual Studio hangi bileşenlerin eksik ve bunları yüklemenizi ister otomatik olarak algılar.

![Çözüm Gezgini ek bileşenler önerir.](../install/media/vs-2019/solution-explorer-config-file.png)

Çözüm Gezgini'nden sağ .vsconfig dosyası da oluşturabilirsiniz.

1. Çözüm dosyanız sağ tıklayın.

1. Seçin **ekleme** > **yükleme yapılandırma dosyası**.

1. .Vsconfig dosyayı kaydedin ve ardından istediğiniz konuma onaylayın **gözden geçirme ayrıntıları**.

1. İstediğiniz bileşenleri ve iş yüklerini var olduğundan emin olun ve ardından **dışarı**.

::: moniker-end

> [!NOTE]
> Daha fazla bilgi için [Visual Studio'yu yapılandırma .vsconfig, kuruluşunuz genelinde](https://devblogs.microsoft.com/setup/configure-visual-studio-across-your-organization-with-vsconfig/) blog gönderisi.

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'nun bir ağ oluşturun](create-a-network-installation-of-visual-studio.md)
* [Visual Studio'nun ağ tabanlı yüklemesini güncelleştirme](update-a-network-installation-of-visual-studio.md)
* [Visual Studio dağıtımlarına yönelik güncelleştirmeleri denetleme](controlling-updates-to-visual-studio-deployments.md)
* [Kuruluş dağıtımları için varsayılanları ayarlama](set-defaults-for-enterprise-deployments.md)
