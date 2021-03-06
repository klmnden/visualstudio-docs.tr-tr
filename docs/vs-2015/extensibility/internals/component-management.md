---
title: Bileşen Yönetimi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- installation [Visual Studio SDK], components
- installation [Visual Studio SDK], file management
ms.assetid: 029bffa2-6841-4caa-a41a-442467e1aedc
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 56a110f382d0b182eed0ea1a95cd4dabf2877037
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68191860"
---
# <a name="component-management"></a>Bileşen Yönetimi
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Windows Installer görevlerin birimleri (bazen WICs veya yalnızca bileşenleri olarak adlandırılır), Windows Yükleyici bileşenleri adlandırılır. Bir GUID, yükleme ve başvuru sayımı Windows Installer kullanan ayarları için temel birimdir her WIC tanımlar.  
  
 VSPackage yükleyicinizi oluşturmak için birden çok ürünlerin kullanabilirsiniz, ancak bu tartışma Windows Installer (.msi) dosyalarının kullanımını varsayar. Böylece her zaman doğru başvuru sayımı gerçekleşir yükleyicinizi oluştururken, dosyayı dağıtım doğru bir şekilde yönetmeniz gerekir. Sonuç olarak, farklı sürümlerini ürünü değil müdahale veya birbiriyle yükleme karışımında Kes ve senaryoları kaldırın.  
  
 Windows Yükleyicisi'nde başvuru sayımı, bileşen düzeyinde gerçekleşir. Kaynaklarınızı dikkatli bir şekilde düzenlemeniz gerekir — dosyaları, kayıt defteri girdileri ve benzeri — bileşenlere. Diğer kuruluş düzeyi vardır — modülleri, özellikler ve ürünleri gibi — farklı senaryolarda yardımcı olabilir. Daha fazla bilgi için [Windows Installer Temelleri](../../extensibility/internals/windows-installer-basics.md).  
  
## <a name="guidelines-of-authoring-setup-for-side-by-side-installation"></a>Yan yana yüklemesi için Kurulum yazma yönergeleri  
  
- Yazar dosyaları ve kayıt defteri anahtarlarını, kendi bileşenlerine sürümleri arasında paylaşılır.  
  
     Bu, bir sonraki sürümünde bunları kolayca kullanmasını sağlar. Örneğin, küresel olarak kayıtlı bir tür kitaplıklarını dosya uzantıları, kayıtlı HKEY_CLASSES_ROOT ve benzeri diğer öğeler.  
  
- Paylaşılan bileşenler ayrı birleştirme modülleri gruplayın.  
  
     Bu, yazar-ilerletme yan için doğru şekilde yardımcı olur.  
  
- Paylaşılan dosyaları ve kayıt defteri anahtarlarını sürümleri arasında aynı Windows Yükleyici bileşenlerini kullanarak yükleyin.  
  
     Farklı bir bileşen kullanırsanız, dosyaları ve kayıt defteri girdilerini tutulan bir VSPackage kaldırılır ancak başka bir VSPackage yüklüdür kaldırılır.  
  
- Oluşturulan ve paylaşılan öğeleri aynı bileşende karıştırmayın.  
  
     Bunun yapılması, genel bir konum ve yalıtılmış konumlara sürümlü öğeleri paylaşılan öğeleri yüklemek mümkün kılar.  
  
- Tutulan dosyalarının olduğu noktaya paylaşılan kayıt defteri anahtarlarını yok.  
  
     Bunu yaparsanız, başka bir sürümü tutulan VSPackage yüklendiğinde paylaşılan anahtarların üzerine yazılır. Dosyanın ikinci sürümü kaldırdıktan sonra anahtar işaret ettiği dosya kayboluyor.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Paylaşılan ve sürümü tutulan Vspackage'lar arasında seçim yapma](../../extensibility/choosing-between-shared-and-versioned-vspackages.md)   
 [VSPackage Kurulum Senaryoları](../../extensibility/internals/vspackage-setup-scenarios.md)
