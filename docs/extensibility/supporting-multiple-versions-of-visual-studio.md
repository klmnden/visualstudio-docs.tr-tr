---
title: Visual Studio'nun birden çok sürümünü destekleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio, supporting multiple versions
- VSPackages, side-by-side compatibility
ms.assetid: 0047aa90-1ed4-40d3-8772-622b2719a4b1
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: f7212445cd507a0d7d185bbd73fa2292e5b783f4
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66745999"
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
  > Visual Studio sürümünü yüklemek, karşılık gelen bir .NET Framework sürümünü yükler. Örneğin, Visual Studio 2010 ve Visual Studio 2012 aynı bilgisayara yüklenmesi de sürüm 4.0 ve 4.5 .NET Framework'ün sırasıyla yükler.

## <a name="in-this-section"></a>Bu Bölümde
- [Sürümü tutulan Vspackage'lar arasında paylaşılan seçme ve](../extensibility/choosing-between-shared-and-versioned-vspackages.md) , VSPackage'ı, yan yana sorunların nasıl giderileceğini açıklar.

- [Yan yana dağıtımlar için dosya adı uzantılarını kaydetme](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md) , VSPackage dosya ilişkilendirmeleri yan yana senaryoda nasıl kaydedebilirsiniz açıklar.

## <a name="related-sections"></a>İlgili Bölümler
- [Windows Installer ile VSPackage Yükleme](../extensibility/internals/installing-vspackages-with-windows-installer.md)
