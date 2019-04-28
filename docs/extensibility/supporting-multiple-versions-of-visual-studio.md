---
title: Visual Studio'nun birden çok sürümünü destekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio, supporting multiple versions
- VSPackages, side-by-side compatibility
ms.assetid: 0047aa90-1ed4-40d3-8772-622b2719a4b1
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 566407f4d15fdaedaf9a89eb50648e555a370750
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63434534"
---
# <a name="supporting-multiple-versions-of-visual-studio"></a>Visual Studio'nun Birden Çok Sürümünü Destekleme
Terim *yan yana* yükleyin ve birden çok sürümünü aynı bilgisayarda bir ürün tutmak anlamına gelir. VSPackage'ları için birden fazla Visual Studio sürümleri aynı bilgisayarda yüklü bir kullanıcısı olabilir anlamına gelir. Ancak, tek bir Visual Studio sürümüne yüklenen, VSPackages sürümlerini yan yana sahip olamaz.

 Visual Studio sürümlerini yan yana yüklenmiş olabilir, VSPackage yapmadan önce aşağıdakileri dikkate alın:

- İzlemek istediğiniz hangi yan yana uygulama stratejisi belirlemeniz gerekir.

   Daha fazla bilgi için [seçme arasında paylaşılan ve sürümü tutulan Vspackage'lar](../extensibility/choosing-between-shared-and-versioned-vspackages.md).

- Çözüm ve proje dosya biçimleri uygulaması stratejinizi sığması gerekir.

   Daha fazla bilgi için [özel projeleri yükseltme](../extensibility/internals/upgrading-projects.md#upgrading-custom-projects) ve [yan yana dağıtımlar için dosya adı uzantılarını kaydetme](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md).

- Böylece sürümlenmiş bileşenler ve tüm sürümler arasında paylaşılan bileşenleri doğru yüklü ve kayıtlı olan yükleyicinizi uygulaması stratejinizi işlemesi gerekir.

   Daha fazla bilgi için [yükleme VSPackage'ları ile Windows Installer](../extensibility/internals/installing-vspackages-with-windows-installer.md) ve ayrıca [bileşen Yönetim](../extensibility/internals/component-management.md).

  > [!NOTE]
  > Visual Studio sürümünü yüklemek de ilgili sürümünü yükler [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)]. Örneğin, Visual Studio 2010 ve Visual Studio 2012 aynı bilgisayara yüklenmesi de 4.0 ve 4.5 sürümlerini yükler [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)]sırasıyla.

## <a name="in-this-section"></a>Bu Bölümde
- [Sürümü tutulan Vspackage'lar arasında paylaşılan seçme ve](../extensibility/choosing-between-shared-and-versioned-vspackages.md) , VSPackage'ı, yan yana sorunların nasıl giderileceğini açıklar.

- [Yan yana dağıtımlar için dosya adı uzantılarını kaydetme](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md) , VSPackage dosya ilişkilendirmeleri yan yana senaryoda nasıl kaydedebilirsiniz açıklar.

## <a name="related-sections"></a>İlgili Bölümler
- [Windows Installer ile VSPackage Yükleme](../extensibility/internals/installing-vspackages-with-windows-installer.md)
