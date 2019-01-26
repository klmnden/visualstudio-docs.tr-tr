---
title: VSPackage için yükleme dizinini seçme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSPackages, installation directory
ms.assetid: 01fbbb5b-f747-446c-afe0-2a081626a945
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e452523c8789214d35281840cb307d329e485ada
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54978548"
---
# <a name="choose-the-installation-directory-for-a-vspackage"></a>VSPackage için yükleme dizinini seçin
VSPackage ve Tamamlayıcı dosyaları, bir kullanıcının dosya sisteminde olması gerekir. Konumu olup VSPackage'ı yönetilen veya yönetilmeyen, yan yana sürüm oluşturma düzeni ve kullanıcı seçenek bağlıdır.  
  
## <a name="unmanaged-vspackages"></a>Yönetilmeyen VSPackage'ları  
 Yönetilmeyen bir VSPackage'ı, herhangi bir konuma yüklenebilen bir COM sunucusudur. Kayıt bilgileri konumuna doğru şekilde yansıtmalıdır. Varsayılan konum olarak bir alt yükleyicisi kullanıcı arabirimi (UI) sağlamalıdır `ProgramFilesFolder` Windows Installer özellik değeri. Örneğin:  
  
*&lt;ProgramFilesFolder&gt;\\&lt;MyCompany&gt;\\&lt;MyVSPackageProduct&gt;\V1.0\\*
  
 Kullanıcı küçük önyükleme bölümü tutmak kullanıcılar uyum sağlamak için varsayılan dizinini değiştirme ve uygulama ve araçların başka bir birimde yüklemeyi tercih izin verilmelidir.  
  
 Yan yana düzeninizi tutulan VSPackage kullanıyorsa, farklı sürümlerini depolamanıza gerek alt dizinleri kullanabilirsiniz. Örneğin:

 *&lt;ProgramFilesFolder&gt;\\&lt;Şirketim&gt;\\&lt;MyVSPackageProduct&gt;\\V1.0\\2002\\*
  
 *&lt;ProgramFilesFolder&gt;\\&lt;Şirketim&gt;\\&lt;MyVSPackageProduct&gt;\\V1.0\\2003\\*
  
 *&lt;ProgramFilesFolder&gt;\\&lt;Şirketim&gt;\\&lt;MyVSPackageProduct&gt;\\V1.0\\2005\\*
  
## <a name="managed-vspackages"></a>Yönetilen VSPackage'ları  
 Yönetilen VSPackage'ları herhangi bir konumda da yüklenebilir. Ancak, genel derleme önbelleğine (GAC) derleme yükleme sürelerini kısaltmak için her zaman yüklemeden düşünmelisiniz. Yönetilen VSPackages tanımlayıcı adlı derlemeler her zaman olduğundan GAC'de yüklemeden, tanımlayıcı ad imzası doğrulaması yalnızca yükleme sırasında sürdüğü anlamına gelir. Başka bir dosya sisteminde yüklü tanımlayıcı adlandırılmış derlemeler yüklü oldukları her zaman doğrulanmış imzaları olması gerekir. Regpkg Aracı'nın GAC'de yönetilen VSPackage yükleme sırasında kullanmak **/Assembly** derlemenin tanımlayıcı adına işaret eden bir kayıt defteri girdilerini Yaz geç.  
  
 GAC dışında bir konumda yönetilen VSPackage yükleme yapıyorsanız, önceki yönetilmeyen Vspackage'lar için dizin hiyerarşileri seçmek için verilen tavsiye izleyin. Regpkg Aracı'nın kullanın **/ codebase** VSPackage derlemesinin yolunu işaret eden bir kayıt defteri girdilerini Yaz geç.  
  
 Daha fazla bilgi için [kaydetmek ve VSPackage kaydı](../../extensibility/registering-and-unregistering-vspackages.md).  
  
## <a name="satellite-dlls"></a>Uydu DLL'leri  
 Kural gereği, VSPackage Uydu DLL'leri, belirli bir yerel ayar için kaynakları içeren bulunur dizinlerde *VSPackage* dizin. Dizinler, yerel ayar kimliği (LCID) değerine karşılık gelir.  
  
 [VSPackage'ları yönetme](../../extensibility/managing-vspackages.md) makale belirten kayıt defteri girişleri nerede denetim [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] uydu DLL'den gerçekten VSPackage'nın arar. Ancak, [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] aşağıdaki sırayla bir LCID değeri adlı bir alt dizinde bir uydu DLL'yi yüklemeye çalışır:  
  
1.  Varsayılan LCID (Visual Studio LCID; Örneğin, *\1033* İngilizce için)  
  
2.  Varsayılan alt dili ile varsayılan LCID.  
  
3.  Sistem varsayılan LCID.  
  
4.  Varsayılan alt dili ile sistem varsayılan LCID.  
  
5.  ABD İngilizce (*. \1033* veya *. \0x409*).  
  

VSPackage DLL'niz kaynaklar içeriyorsa ve **SatelliteDll\DllName** kayıt defteri girişi, işaret [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] yukarıdaki sırayla yüklemeye çalışır.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Paylaşılan ve sürümü tutulan Vspackage'lar arasında seçin](../../extensibility/choosing-between-shared-and-versioned-vspackages.md)   
 [VSPackage'ları yönetme](../../extensibility/managing-vspackages.md)   
 [Paket kaydı yönetme](https://msdn.microsoft.com/library/f69e0ea3-6a92-4639-8ca9-4c9c210e58a1)