---
title: 'Nasıl yapılır: Üçüncü taraf birim test çerçevelerini yükleme'
ms.date: 04/01/2019
ms.topic: conceptual
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 9f61b52f72474a8ecd8fac4c30265dcd7cf36a5e
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58857708"
---
# <a name="install-unit-test-frameworks"></a>Birim testi çerçevelerini yükleme

Visual Studio Test Gezgini'yle, herhangi bir birimi için bir bağdaştırıcı arabirimi geliştirdi test çerçevesi testleri çalıştırabilirsiniz. Framework'ü yükleme ikili dosyaları kopyalar ve onu destekleyen diller için Visual Studio Proje şablonları ekler. Framework şablonu içeren bir proje oluşturduğunuzda, Test Gezgini ile kayıtlı.

Visual Studio çözüm, farklı çerçeveler kullanan ve farklı dil hedeflenen birim testi projelerini içerebilir.

[MSTest](getting-started-with-unit-testing.md) olan Visual Studio tarafından sağlanan test çerçevesi ve varsayılan olarak yüklenir.

## <a name="acquire-frameworks"></a>Çerçeveler Al

Üçüncü taraf birim testi çerçevelerini kullanarak yükleme **NuGet Paket Yöneticisi**.

1. Seçin ve test kodunuzu içeren projeye sağ tıklayın **NuGet paketlerini Yönet**.

2. İçinde **NuGet Paket Yöneticisi**, yükleyin ve ardından istediğiniz test çerçevesi için arama **yükleme**.

   ![Visual Studio'da NuGet Paket Yöneticisi](media/vs-2019/nuget-package-manager.png)

## <a name="update-to-the-latest-test-adapters"></a>İçin en son test bağdaştırıcısı güncelleştirme

Test bulma ve yürütme için daha iyi bir deneyim için en son kararlı test bağdaştırıcısı güncelleştirme. MSTest, NUnit ve xUnit test bağdaştırıcısı güncelleştirmeleri hakkında daha fazla bilgi için bkz. [Visual Studio blogu](https://devblogs.microsoft.com/visualstudio/test-experience-improvements/).

### <a name="to-update-to-the-latest-stable-test-adapter-version"></a>En son kararlı test bağdaştırıcısı sürümüne güncelleştirmek için

1. Çözümünüz için Nuget Paket Yöneticisi giderek açın **Araçları** > **NuGet Paket Yöneticisi** > **ÇözümiçinNuGetpaketleriniYönet**.

2. Tıklayarak **güncelleştirmeleri** sekmesinde ve arama MSTest, NUnit veya xUnit test yüklenen bağdaştırıcıları.

3. Her test bağdaştırıcısı seçin ve ardından açılan menüde en son kararlı sürümünü seçin.

4. Seçin **yükleme** düğmesi.

   ![Test bağdaştırıcısı yükseltme](media/install-adapter-upgrade.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Birim testi kod](../test/unit-test-your-code.md)
