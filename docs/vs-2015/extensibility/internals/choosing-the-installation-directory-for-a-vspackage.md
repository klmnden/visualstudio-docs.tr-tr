---
title: VSPackage için yükleme dizinini seçme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, installation directory
ms.assetid: 01fbbb5b-f747-446c-afe0-2a081626a945
caps.latest.revision: 18
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: d8812ce6eef882f4f1b4effe97320492a34e0f2d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54755566"
---
# <a name="choosing-the-installation-directory-for-a-vspackage"></a>VSPackage için Yükleme Dizinini Seçme
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

VSPackage ve Tamamlayıcı dosyaları, bir kullanıcının dosya sisteminde olması gerekir. Konumu olup VSPackage'ı yönetilen veya yönetilmeyen, yan yana sürüm oluşturma düzeni ve kullanıcı seçenek bağlıdır.  
  
## <a name="unmanaged-vspackages"></a>Yönetilmeyen VSPackage'ları  
 Yönetilmeyen bir VSPackage'ı, herhangi bir konuma yüklenebilen bir COM sunucusudur. Kayıt bilgileri doğru konumunu yansıtır gerekir. Yükleyici kullanıcı arabirimi (UI) ProgramFilesFolder Windows Yükleyici özelliğinin bir alt dizini olarak bir varsayılan konumu sağlamanız gerekir. Örneğin:  
  
 [ProgramFilesFolder] MyCompany\MyVSPackageProduct\V1.0\  
  
 Kullanıcı küçük önyükleme bölümü tutmak kullanıcılar uyum sağlamak için varsayılan dizinini değiştirme ve uygulama ve araçların başka bir birimde yüklemeyi tercih izin verilmelidir.  
  
 Yan yana düzeninizi tutulan VSPackage kullanıyorsa, farklı sürümlerini depolamanıza gerek alt dizinleri kullanabilirsiniz. Örneğin:  
  
 [ProgramFilesFolder]MyCompany\MyVSPackageProduct\V1.0\2002\  
  
 [ProgramFilesFolder]MyCompany\MyVSPackageProduct\V1.0\2003\  
  
 [ProgramFilesFolder]MyCompany\MyVSPackageProduct\V1.0\2005\  
  
## <a name="managed-vspackages"></a>Yönetilen VSPackage'ları  
 Yönetilen VSPackage'ları herhangi bir konumda da yüklenebilir. Ancak, genel derleme önbelleğine (GAC) derleme yükleme sürelerini kısaltmak için her zaman yüklemeden düşünmelisiniz. Yönetilen VSPackages tanımlayıcı adlı derlemeler her zaman olduğundan GAC'de yüklemeden, tanımlayıcı ad imzası doğrulaması yalnızca yükleme sırasında sürdüğü anlamına gelir. Başka bir dosya sisteminde yüklü tanımlayıcı adlandırılmış derlemeler yüklü oldukları her zaman doğrulanmış imzaları olması gerekir. Regpkg Aracı'nın GAC'de yönetilen VSPackage yükleme sırasında kullanmak **/Assembly** derlemenin tanımlayıcı adına işaret eden bir kayıt defteri girdilerini Yaz geç.  
  
 GAC dışında bir konumda yönetilen VSPackage yükleme yapıyorsanız, önceki yönetilmeyen Vspackage'lar için dizin hiyerarşileri seçmek için verilen tavsiye izleyin. Regpkg Aracı'nın kullanın **/ codebase** VSPackage derlemesinin yolunu işaret eden bir kayıt defteri girdilerini Yaz geç.  
  
 Daha fazla bilgi için [kaydetme ve kaydını kaldırma VSPackages](../../extensibility/registering-and-unregistering-vspackages.md).  
  
## <a name="satellite-dlls"></a>Uydu DLL'leri  
 Kural gereği, VSPackage Uydu DLL'leri — belirli bir yerel ayar için kaynakları içerir; VSPackage dizininin bir alt dizinlerinde bulunur. Dizinler, yerel ayar kimliği (LCID) değerine karşılık gelir.  
  
 [VSPackage'ları yönetme](../../extensibility/managing-vspackages.md) belirten kayıt defteri girişleri nerede denetim [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] uydu DLL'den gerçekten VSPackage'nın arar. Ancak, [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] aşağıdaki sırayla bir LCID değeri adlı bir alt dizinde bir uydu DLL'yi yüklemeye çalışır:  
  
1. Varsayılan LCID (VS LCID örneğin \1033 İngilizce için)  
  
2. Varsayılan alt dili ile varsayılan LCID.  
  
3. Sistem varsayılan LCID.  
  
4. Varsayılan alt dili ile sistem varsayılan LCID.  
  
5. ABD İngilizce (. \1033 veya. \0x409).  
  
   VSPackage DLL'niz kaynakları ve ona SatelliteDll\DllName kayıt defteri giriş noktaları içeriyorsa [!INCLUDE[vsprvs](../../includes/vsprvs-md.md)] yukarıdaki sırayla yüklemeye çalışır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Paylaşılan ve sürümü tutulan Vspackage'lar arasında seçim yapma](../../extensibility/choosing-between-shared-and-versioned-vspackages.md)   
 [VSPackage'ları yönetme](../../extensibility/managing-vspackages.md)   
 [Yönetilen paket kaydı](http://msdn.microsoft.com/f69e0ea3-6a92-4639-8ca9-4c9c210e58a1)
