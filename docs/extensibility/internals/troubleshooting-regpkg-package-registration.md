---
title: RegPkg paket kaydı sorunlarını giderme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- RegPkg
ms.assetid: f33f822f-697a-4bad-9c10-554b4c8f6246
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6db6421d3d0a62f8a50df2301689b638ac42d4df
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56611938"
---
# <a name="troubleshooting-regpkg-package-registration"></a>RegPkg Paket Kaydı Sorunlarını Giderme
> [!NOTE]
>  Visual Studio'da paketleri kaydetmek için tercih edilen yol, .pkgdef dosyaları kullanmaktır. Bu uzantı dağıtım için sistem kayıt defterine erişmek zorunda kalmadan sağlar. Pkgdef dosyaları kullanılarak oluşturulan [CreatePkgDef yardımcı programı](../../extensibility/internals/createpkgdef-utility.md).

 Bir paket içinde RegPkg kullanarak kaydetmek için [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)], paketiniz için uygun olan RegPkg sürümünü kullanmanız gerekir.

## <a name="regpkg-versions-related-to-package-versions"></a>Paket sürümleri için ilgili RegPkg sürümleri
 RegPkg iki sürümü vardır. Bir sürüm eklenir [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]. Bu sürüm aşağıdaki derlemeleri kullanarak oluşturulan paketler kaydetmek için kullanın:

1. Microsoft.VisualStudioShell.9.0.dll

2. Microsoft.VisualStudioShell.10.0.dll

3. Microsoft.VisualStudioShell.11.0.dll

   Bu, önceki Microsoft.VisualStudio.Shell.dll derlemeyi kullanarak oluşturulan paketler kaydedilemiyor.

   RegPkg önceki sürümünü Microsoft.VisualStudio.Shell.dll derlemeyi kullanarak oluşturulan paketler kaydedebilirsiniz. Ancak, bu derlemenin daha yeni sürümleri kullanılarak oluşturulan paketler kayda alınamıyor.

## <a name="see-also"></a>Ayrıca Bkz.
- [VSPackage’lar](../../extensibility/internals/vspackages.md)