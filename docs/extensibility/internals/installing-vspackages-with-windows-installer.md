---
title: Windows Installer ile VSPackage yükleme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- installation [Visual Studio SDK], with Windows Installer
- VSPackages, deploying
ms.assetid: 41d2c72c-0a97-4fcd-b3aa-33a8d3aa962a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9cd5f25e1e87ba3db360b328b4f5a245697cba45
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56600434"
---
# <a name="installing-vspackages-with-windows-installer"></a>Windows Installer ile VSPackage Yükleme
İçinde VSPackage'ı tümleştirme [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] daha fazlasını bir kullanıcının bilgisayarına dosyaları kopyalama gerektirir. VSPackage'nın yükleyici gerekir VSPackage'ı ve onun bağımlı dosyaları yüklemek ve kaydettirmek ve bunları tümleştirmek [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. VSPackage'ı bir simge görüntülemek gibi tümleştirme özellikleri yararlanabilirsiniz [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] tanıtım ekran ve hakkında kutusu.

 Microsoft Windows Installer dosyaları, VSPackage'ları dağıtmak için önerilen yoldur. Kullanımı kolay Windows Installer paketleri tarafından desteklenen tüm Windows işletim sistemlerinde çalışabilir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Daha fazla bilgi için [Windows Installer](https://msdn.microsoft.com/library/121be21b-b916-43e2-8f10-8b080516d2a0).

## <a name="in-this-section"></a>Bu Bölümde
- [Temel Windows Installer Bilgileri](../../extensibility/internals/windows-installer-basics.md)

 Windows Installer genel bir bakış sağlar.

- [VSPackage Kurulum Senaryoları](../../extensibility/internals/vspackage-setup-scenarios.md)

 Yan yana yüklemeleri, her iki VSPackages destekleyebilir farklı yolları açıklanmaktadır ve [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- [Windows Installer Paketi Yazma](../../extensibility/internals/authoring-a-windows-installer-package.md)

 Yükleyicilerini uygulayın doğru bir şekilde yüklemek ve VSPackages uygulamasına tümleştirmek için tipik adımları genel bir bakış sağlar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- [Sistem Gereksinimlerini Algılama](../../extensibility/internals/detecting-system-requirements.md)

 Bir yükleyici nasıl algılayabilir açıklar [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve bileşenleri ve iptal VSPackage gereksinimler karşılanmazsa ayarlayın.

- [Bileşen Yönetimi](../../extensibility/internals/component-management.md)

 Önceki ürün sürümleri bütünlüğünü bir yükleyici geliştirme konusunda anlatılmaktadır.

- [VSPackage için Yükleme Dizinini Seçme](../../extensibility/internals/choosing-the-installation-directory-for-a-vspackage.md)

 VSPackage bulmak için seçenekler özetlenmektedir.

- [VSPackage Kaydı](../../extensibility/internals/vspackage-registration.md)

 VSPackage yükleme sırasında nasıl kayıtlı açıklanır ve kendi kendine kayıt neden hatalı bir uygulamadır.

- [Proje Türlerini Dağıtma](../../extensibility/internals/deploying-project-types.md)

 Yönetilen kod proje türleri için yeni proje türü Toplayıcısı'nı kullanmayı açıklar.

- [Nasıl yapılır: Bir yükleyicinin kayıt defteri bilgilerini oluşturma](../../extensibility/internals/how-to-generate-registry-information-for-an-installer.md)

 Yönetilen bir VSPackage için bir kayıt bildirim oluşturmak üzere RegPkg.exe kullanmayı açıklar.

- [Yükleme Sonrasında çalıştırılması Gereken Komutlar](../../extensibility/internals/commands-that-must-be-run-after-installation.md)

 VSPackage'ları ile tümleştirme için yükleme sonrası komutları çalıştırılması açıklanmaktadır [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

- [Windows Installer ile VSPackage Kaldırma](../../extensibility/internals/uninstalling-a-vspackage-with-windows-installer.md)

 Kullanıcılar, VSPackage'ı kaldırdığınızda, yükleyici gerçekleştirmeniz gereken adımlar açıklanmaktadır.