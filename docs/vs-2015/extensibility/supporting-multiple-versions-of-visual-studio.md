---
title: Visual Studio 2015 birden çok sürümünü destekleme | Microsoft Docs
titleSuffix: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio, supporting multiple versions
- VSPackages, side-by-side compatibility
ms.assetid: 0047aa90-1ed4-40d3-8772-622b2719a4b1
caps.latest.revision: 21
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 377a7eceff134211371c17ac14903cba0fb8daa6
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60042146"
---
# <a name="supporting-multiple-versions-of-visual-studio"></a>Visual Studio'nun Birden Çok Sürümünü Destekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Terim *yan yana* yükleyin ve birden çok sürümünü aynı bilgisayarda bir ürün tutmak anlamına gelir. VSPackage'ları için birden fazla Visual Studio sürümleri aynı bilgisayarda yüklü bir kullanıcısı olabilir anlamına gelir. Ancak, tek bir Visual Studio sürümüne yüklenen, VSPackages sürümlerini yan yana sahip olamaz.

 Visual Studio sürümlerini yan yana yüklenmiş olabilir, VSPackage yapmadan önce aşağıdakileri dikkate alın:

- İzlemek istediğiniz hangi yan yana uygulama stratejisi belirlemeniz gerekir.

     Daha fazla bilgi için [seçme arasında paylaşılan ve sürümü tutulan Vspackage'lar](../extensibility/choosing-between-shared-and-versioned-vspackages.md).

- Çözüm ve proje dosya biçimleri uygulaması stratejinizi sığması gerekir.

     Daha fazla bilgi için [özel projeleri yükseltme](../misc/upgrading-custom-projects.md) ve [yan yana dağıtımlar için dosya adı uzantılarını kaydetme](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md).

- Böylece sürümlenmiş bileşenler ve tüm sürümler arasında paylaşılan bileşenleri doğru yüklü ve kayıtlı olan yükleyicinizi uygulaması stratejinizi işlemesi gerekir.

     Daha fazla bilgi için [yükleme VSPackage'ları ile Windows Installer](../extensibility/internals/installing-vspackages-with-windows-installer.md) ve ayrıca [bileşen Yönetim](../extensibility/internals/component-management.md).

    > [!NOTE]
    >  Visual Studio sürümünü yüklemek de ilgili sürümünü yükler [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]. Örneğin, Visual Studio 2010 ve Visual Studio 2012 aynı bilgisayara yüklenmesi de 4.0 ve 4.5 sürümlerini yükler [!INCLUDE[dnprdnshort](../includes/dnprdnshort-md.md)]sırasıyla.

## <a name="in-this-section"></a>Bu Bölümde
 [Sürümü tutulan Vspackage'lar arasında paylaşılan seçme ve](../extensibility/choosing-between-shared-and-versioned-vspackages.md) , VSPackage'ı, yan yana sorunların nasıl giderileceğini açıklar.

 [Yan yana dağıtımlar için dosya adı uzantılarını kaydetme](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md) , VSPackage dosya ilişkilendirmeleri yan yana senaryoda nasıl kaydedebilirsiniz açıklar.

## <a name="related-sections"></a>İlgili Bölümler
 [VSPackage yükleme](../misc/installing-vspackages.md) nasıl oluşturacağınızı ve VSPackages yükleyin ve Visual Studio'nun birden çok sürümünü aynı anda çalıştıran kullanıcılar desteklemek nasıl ele alınmaktadır.
