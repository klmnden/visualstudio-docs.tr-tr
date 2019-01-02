---
title: CreatePkgDef yardımcı programı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- package definition
- create pkgdef
- pkgdef
- createpkgdef
ms.assetid: c745cb76-47a6-49ff-9eed-16af0f748e35
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: c5c18e77405cd4e48c89d3b481937c7d837488cd
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53910941"
---
# <a name="createpkgdef-utility"></a>CreatePkgDef yardımcı programı
Bir .dll dosyası için bir Visual Studio uzantısı bir parametre olarak alır ve oluşturur bir *.pkgdef* eşlik eden dosya *.dll* dosya. *.Pkgdef* dosya uzantısı yüklü olduğunda, sistem kayıt defterine yazılması tüm bilgileri içerir.  
  
> [!NOTE]
>  Çoğu Visual Studio SDK'yı otomatik olarak dahil edilen proje şablonları oluşturma *.pkgdef* dosyaları yapı işleminin bir parçası olarak. Bu belge paketleri el ile oluşturmanız veya kullanmak için mevcut paketleri dönüştürmek istediğiniz olanlar için tasarlanmıştır *.pkgdef* dağıtım.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
CreatePkgDef /out=<FileName> [/codebase] [/assembly] <AssemblyPath>  
```  
  
## <a name="arguments"></a>Arguments  
 **/ out =&lt;dosya adı&gt;**  
 Gerekli. Adını ayarlar *.pkgdef* çıktı dosyasına &lt;FileName&gt;.  
  
 **/ codebase**  
 İsteğe bağlı. Kayıt işlemine zorlar **CodeBase** yardımcı programı.  
  
 **/ Assembly**  
 Kayıt işlemine zorlar **derleme** yardımcı programı.  
  
 **&lt;AssemblyPath&gt;**  
 Yolu *.dll* oluşturmak istediğiniz dosya *.pkgdef*.  
  
## <a name="remarks"></a>Açıklamalar  
 Uzantı dağıtımı kullanarak *.pkgdef* dosyaları Visual Studio'nun önceki sürümleri kayıt defteri gereksinimlerini değiştirir.  
  
 *.Pkgdef* dosyaları aşağıdaki konumlardan birinde yüklenmelidir: 

- *%LocalAppData%\Microsoft\Visual Studio\14.0\Extensions\\* 
 
- *%vsinstalldir%\Common7\IDE\Extensions\\*
    
  Yükleme klasörünü ise *%localappdata%\Microsoft\Visual Studio\14.0\Extensions\\*, uzantı, Visual Studio tarafından tanınan ancak varsayılan olarak devre dışı bırakılır. Kullanıcı uzantıyı kullanarak etkinleştirebilirsiniz **Uzantılar ve güncelleştirmeler**. 
   
  Yükleme klasörünü ise *%vsinstalldir%\Common7\IDE\Extensions\\*, uzantı varsayılan olarak etkindir.  
  
> [!NOTE]
>  **Uzantılar ve güncelleştirmeler** aracı, bir VSIX paketinin bir parçası yüklü olduğu sürece bir uzantı erişmek için kullanılamaz.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Createexpınstance yardımcı programı](../../extensibility/internals/createexpinstance-utility.md)