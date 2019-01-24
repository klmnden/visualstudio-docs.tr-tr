---
title: CreatePkgDef yardımcı programı | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- package definition
- create pkgdef
- pkgdef
- createpkgdef
ms.assetid: c745cb76-47a6-49ff-9eed-16af0f748e35
caps.latest.revision: 14
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 5f450453ce8e336fecb401e30bc777c7b9c8ef7d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54775132"
---
# <a name="createpkgdef-utility"></a>CreatePkgDef Yardımcı Programı
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir .dll dosyası için bir Visual Studio uzantısı bir parametre olarak alır ve .dll eşlik eden .pkgdef dosyası oluşturur. .Pkgdef dosyası uzantısı yüklü olduğunda, sistem kayıt defterine yazılması tüm bilgileri içerir.  
  
> [!NOTE]
>  Çoğu Visual Studio SDK'yı otomatik olarak dahil edilen proje şablonları, .pkgdef dosyaları oluşturma işleminin bir parçası oluşturun. Bu belge paketleri el ile oluşturmanız veya .pkgdef dağıtımını kullanmak için mevcut paketleri dönüştürmek istediğiniz olanlar için tasarlanmıştır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
CreatePkgDef /out=FileName [/codebase] [/assembly] AssemblyPath  
```  
  
## <a name="arguments"></a>Arguments  
 / out =`FileName`  
 Gerekli. .pkgdef çıkış dosya adını ayarlar`FileName`.  
  
 /codebase  
 İsteğe bağlı. Kod temeli yardımcı programı ile kayıt zorlar.  
  
 / Assembly  
 Derleme yardımcı programı ile kayıt zorlar.  
  
 `AssemblyPath`  
 .pkgdef oluşturmak istediğiniz .dll dosyasının yolu.  
  
## <a name="remarks"></a>Açıklamalar  
 .Pkgdef dosyaları kullanarak uzantı dağıtımı, Visual Studio'nun önceki sürümleri kayıt defteri gereksinimlerini yerine geçer.  
  
 .Pkgdef dosyaları aşağıdaki konumlardan birinde yüklü olmalıdır: %localappdata%\Microsoft\Visual Studio\14.0\Extensions\ veya %vsinstalldir%\Common7\IDE\Extensions\\. Yükleme klasörünü %localappdata%\Microsoft\Visual Studio\14.0\Extensions ise\\, uzantı, Visual Studio tarafından tanınan ancak varsayılan olarak devre dışı bırakılır. Kullanıcı uzantıyı kullanarak etkinleştirebilirsiniz **Uzantılar ve güncelleştirmeler**. Yükleme klasörünü %vsinstalldir%\Common7\IDE\Extensions ise\\, uzantı varsayılan olarak etkindir.  
  
> [!NOTE]
>  **Uzantılar ve güncelleştirmeler** aracı, bir VSIX paketinin bir parçası yüklü olduğu sürece bir uzantı erişmek için kullanılamaz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CreateExpInstance Yardımcı Programı](../../extensibility/internals/createexpinstance-utility.md)
