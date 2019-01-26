---
title: Dosya adı uzantıları hakkında | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- file extensions
- file name extensions
ms.assetid: 99f4f9ff-fb84-4258-9787-6890f308a57f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1146c7ed7bfc0d3f09d6c1848bf52345661bf0c7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54995040"
---
# <a name="about-file-name-extensions"></a>Dosya adı uzantıları hakkında
VSPackage dosya uzantısına kaydolduğunuzda, bunu bir sürümü ile ilişkilendirirsiniz [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]. Bu sürümü, birden çok önemli ise, [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] bir bilgisayarda yüklü.  
  
 Vspackage'lar için dosya uzantıları altında kayıtlı **HKEY_CLASSES_ROOT** varsayılan değerle ilişkili program tanımlayıcısı (ProgID) için işaret eden bir anahtar.  
  
 Kayıt bilgileri için aşağıdaki örnekte *.vcproj* dosya uzantısı:  
  
```  
HKEY_CLASSES_ROOT\  
   .vcproj\  
      (default)=" VisualStudio.vcproj.8.0"   
```  
  
 İle ilişkili dosyaları [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] tutulan bir ProgID gibi olmalıdır `VisualStudio.vcproj.8.0`. Tutulan ProgID ürün sürümleri arasında dosya uzantısı ilişkilendirmeyi korumak için ürün yan yana yüklemesini sağlar. Sürüme özgü ProgID de açık düzenleme gibi ve benzeri üzerine yazmasını ya da diğer uygulamalar veya sürümleri tarafından üzerine yazılmasını kaygısı olmadan standart fiiller kullanmanıza olanak tanır [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].  
  
 Bazı durumlarda, bir dosya uzantısıyla ilişkili ProgID değiştirilmemelidir. Örneğin, program *.htm* dosya uzantısı (ProgID htmlfile =) çok sayıda işletim sisteminde yer sabit kodlanmış ve yaygın olarak bilinen ve kullanılan ilişkilendirmesini *.htm* ve *.html* dosyaları.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Yan yana dağıtımlar için dosya adı uzantılarını kaydetme](../extensibility/registering-file-name-extensions-for-side-by-side-deployments.md)   
 [Dosya adı uzantıları için dosya işleyicileri belirtme](../extensibility/specifying-file-handlers-for-file-name-extensions.md)