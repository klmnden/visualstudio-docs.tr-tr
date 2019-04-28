---
title: RegPkg paket kaydı sorunlarını giderme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: troubleshooting
helpviewer_keywords:
- RegPkg
ms.assetid: f33f822f-697a-4bad-9c10-554b4c8f6246
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 241975e475252a18d5e5a91c6e8c4fb40c067a95
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63441175"
---
# <a name="troubleshooting-regpkg-package-registration"></a>RegPkg Paket Kaydı Sorunlarını Giderme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

> [!NOTE]
> Visual Studio'da paketleri kaydetmek için tercih edilen yol, .pkgdef dosyaları kullanmaktır. Bu uzantı dağıtım için sistem kayıt defterine erişmek zorunda kalmadan sağlar. Pkgdef dosyaları kullanılarak oluşturulan [CreatePkgDef yardımcı programı](../../extensibility/internals/createpkgdef-utility.md).  
  
 Bir paket içinde RegPkg kullanarak kaydetmek için [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)], paketiniz için uygun olan RegPkg sürümünü kullanmanız gerekir.  
  
## <a name="regpkg-versions-related-to-package-versions"></a>Paket sürümleri için ilgili RegPkg sürümleri  
 RegPkg iki sürümü vardır. Bir sürüm eklenir [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)]. Bu sürüm aşağıdaki derlemeleri kullanarak oluşturulan paketler kaydetmek için kullanın:  
  
1. Microsoft.VisualStudioShell.9.0.dll  
  
2. Microsoft.VisualStudioShell.10.0.dll  
  
3. Microsoft.VisualStudioShell.11.0.dll  
  
   Bu, önceki Microsoft.VisualStudio.Shell.dll derlemeyi kullanarak oluşturulan paketler kaydedilemiyor.  
  
   RegPkg önceki sürümünü Microsoft.VisualStudio.Shell.dll derlemeyi kullanarak oluşturulan paketler kaydedebilirsiniz. Ancak, bu derlemenin daha yeni sürümleri kullanılarak oluşturulan paketler kayda alınamıyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Bir ürün serbest bırakma](../../misc/releasing-a-visual-studio-integration-product.md)
