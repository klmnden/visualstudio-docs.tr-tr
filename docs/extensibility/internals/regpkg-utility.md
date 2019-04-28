---
title: RegPkg yardımcı programı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- regpkg, registration utility
- registration, regpkg utility
ms.assetid: 1683ee18-59d1-4bab-a674-dd00dd960de3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e37125f8098d854d887c7bc5d209b30af2d12222
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63409681"
---
# <a name="regpkg-utility"></a>RegPkg Yardımcı Programı
> [!NOTE]
> Visual Studio'da paketleri kaydetmek için tercih edilen yol, .pkgdef dosyaları kullanmaktır. Bu uzantı dağıtım için VSIX dağıtımı için bir gerekliliktir sistem kayıt defterine erişmek zorunda kalmadan sağlar. Pkgdef dosyaları kullanılarak oluşturulan [CreatePkgDef yardımcı programı](../../extensibility/internals/createpkgdef-utility.md). Visual Studio Paket dağıtımı hakkında daha fazla bilgi için bkz. [sevkiyat Visual Studio uzantıları](../../extensibility/shipping-visual-studio-extensions.md).

 RegPkg.exe yardımcı programı ile VSPackage kaydeder [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] ve dağıtım için hazırlar. Bu yardımcı program arka planda VSPackage geliştirme sırasında kullanılır. Oluşturabilir ve Deneysel kovanında VSPackage çalıştırma yapı işleminin bir parçası olarak çalışır.

 RegPkg çeşitli biçimlerde sistem kayıt defteri betikleri oluşturabilirsiniz. .Msi projeleri veya Windows Installer XML araç takımı dosyaları gibi dağıtım projeleri bu betiklerde birleştirebilirsiniz.

 RegPkg.exe genellikle \< *Visual Studio SDK yükleme yolunu*> \VisualStudioIntegration\Tools\Bin\RegPkg.exe. RegPkg bu söz dizimi aşağıdaki gibidir:

```
RegPkg [/root:<root>] [/regfile:<regfile>] [/rgsfile:<rgsfile> [/rgm]] [/vrgfile:<vrgfile>] [/codebase | /assembly] [/unregister] AssemblyPath
```

 Belirtilen adla /root:root gerçekleştirir kayıt

 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] kök dizini.

 /regfile:filename güncelleyerek yerine .reg dosyasını oluşturur.  /Vrgfile veya /rgsfile veya /wixfile ile kullanılamaz.

 /rgsfile:filename güncelleyerek yerine .rgs dosyası oluşturur.  /Vrgfile veya/regfile veya /wixfile ile kullanılamaz.

 /vrgfile:filename güncelleyerek yerine .vrg dosyası oluşturur.  / Regfile veya /rgsfile veya /wixfile ile kullanılamaz.

 /rgm rgs dosyası yanı sıra bir .rgm dosyası oluşturur.  /Rgsfile ile birleştirilmelidir.

 /wixfile:filename güncelleyerek yerine Windows Installer XML araç takımı ile uyumlu bir dosya oluşturur.  / Regfile veya /rgsfile veya /vrgfile ile kullanılamaz.

 / codebase derleme yerine kod temeli ile kayıt zorlar.

 kod temeli yerine derleme/Assembly zorlar kaydı.

 / Unregisters bu paket kaydını silin.  Kullanılamaz

 / regfile veya /vrgfile veya /rgsfile veya /wixfile ile.

## <a name="see-also"></a>Ayrıca Bkz.
- [VSPackage’lar](../../extensibility/internals/vspackages.md)
- [RegPkg Paket Kaydı Sorunlarını Giderme](../../extensibility/internals/troubleshooting-regpkg-package-registration.md)