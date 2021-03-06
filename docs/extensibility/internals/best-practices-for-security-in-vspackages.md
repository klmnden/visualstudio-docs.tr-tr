---
title: Vspackage'larda güvenlik için en iyi uygulamalar | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- security [Visual Studio SDK]
- security best practices, VSPackages
- best practices, security
ms.assetid: 212a0504-cf6c-4e50-96b0-f2c1c575c0ff
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 144bc62176ebc552e7070b29088acf70329a84d4
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66309151"
---
# <a name="best-practices-for-security-in-vspackages"></a>Vspackage'larda güvenlik için en iyi uygulamalar
Yüklenecek [!INCLUDE[vsipsdk](../../extensibility/includes/vsipsdk_md.md)] bilgisayarınızda yönetici kimlik bilgilerine sahip bir bağlamda çalıştırıyor olmalısınız. Güvenliği ve dağıtımı temel birimini bir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] uygulama [VSPackage](../../extensibility/internals/vspackages.md). Bir VSPackage'ı kullanarak kaydedilmelidir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], gerektiren yönetici kimlik bilgileri.

 Yöneticiler, kayıt defteri ve dosya sistemine yazma ve herhangi bir kodu çalıştırmak için tam izinleri vardır. Geliştirme, dağıtma veya bir VSPackage'ı yüklemek için bu izinlere sahip olmalıdır.

 VSPackage yüklendikten hemen sonra tam olarak güvenilirdir. VSPackage'ı ile ilişkili izin nedeniyle bu yüksek düzeyde farkında olmadan kötü amaçlı olan bir VSPackage'ı yüklemek mümkündür.

 Kullanıcılar VSPackages yalnızca güvenilir kaynaklardan gelen yükleme emin olmanız gerekir. VSPackage geliştirme şirketler kesin ad ve oturumunu, kullanıcı söz konusu oynama güvence altına almak için engellenir. VSPackage geliştirme şirketler, web hizmetleri ve değerlendirmek ve güvenlik sorunları düzeltmek için uzaktan yükleme gibi dış bağımlılıklarını incelemeniz gerekir.

 Daha fazla bilgi için [güvenli kodlama yönergeleri için .NET Framework](/previous-versions/visualstudio/visual-studio-2008/d55zzx87(v=vs.90)).

## <a name="see-also"></a>Ayrıca bkz.
- [Eklenti güvenliği](https://msdn.microsoft.com/Library/44a5c651-6246-4310-b371-65378917c799)
- [DDEX güvenlik](https://msdn.microsoft.com/library/44a52a70-5c98-450e-993d-4a3b32f69ba8)