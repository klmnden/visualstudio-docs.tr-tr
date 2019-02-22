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
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 96b0343cd088a8d608cd3503162bf7fa737b79f4
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56602448"
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
 **/ out =&lt;FileName&gt;**  gerekli. Adını ayarlar *.pkgdef* çıktı dosyasına &lt;FileName&gt;.

 **/ codebase** isteğe bağlı. Kayıt işlemine zorlar **CodeBase** yardımcı programı.

 **/ Assembly** zorlar kaydı **derleme** yardımcı programı.

 **&lt;AssemblyPath&gt;**  yolunu *.dll* oluşturmak istediğiniz dosya *.pkgdef*.

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
- [Createexpınstance yardımcı programı](../../extensibility/internals/createexpinstance-utility.md)