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
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 6ab5866949d6ccfa9f3b1037abf7801ce40ace3d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66332278"
---
# <a name="createpkgdef-utility"></a>CreatePkgDef yardımcı programı
Bir .dll dosyası için bir Visual Studio uzantısı bir parametre olarak alır ve oluşturur bir *.pkgdef* eşlik eden dosya *.dll* dosya. *.Pkgdef* dosya uzantısı yüklü olduğunda, sistem kayıt defterine yazılması tüm bilgileri içerir.

> [!NOTE]
> Çoğu Visual Studio SDK'yı otomatik olarak dahil edilen proje şablonları oluşturma *.pkgdef* dosyaları yapı işleminin bir parçası olarak. Bu belge paketleri el ile oluşturmanız veya kullanmak için mevcut paketleri dönüştürmek istediğiniz olanlar için tasarlanmıştır *.pkgdef* dağıtım.

## <a name="syntax"></a>Sözdizimi

```
CreatePkgDef /out=<FileName> [/codebase] [/assembly] <AssemblyPath>
```

## <a name="arguments"></a>Arguments
**/ out =&lt;dosya adı&gt;** \
Gerekli. Adını ayarlar *.pkgdef* çıktı dosyasına &lt;FileName&gt;.

**/ codebase**\
İsteğe bağlı. Kayıt işlemine zorlar **CodeBase** yardımcı programı.

**/ Assembly**\
Kayıt işlemine zorlar **derleme** yardımcı programı.

**&lt;AssemblyPath&gt;** \
Yolu *.dll* oluşturmak istediğiniz dosya *.pkgdef*.

## <a name="remarks"></a>Açıklamalar
Uzantı dağıtımı kullanarak *.pkgdef* dosyaları Visual Studio'nun önceki sürümleri kayıt defteri gereksinimlerini değiştirir.

::: moniker range=">=vs-2019"

*.Pkgdef* dosyaları aşağıdaki konumlardan birinde yüklenmelidir:

- *%LocalAppData%\Microsoft\Visual Studio\16.0\Extensions\\*

- *%vsinstalldir%\Common7\IDE\Extensions\\*

Yükleme klasörünü ise *%localappdata%\Microsoft\Visual Studio\16.0\Extensions\\* , uzantı Visual Studio tarafından kabul edilir, ancak varsayılan olarak devre dışıdır. Kullanıcı uzantıyı kullanarak etkinleştirebilirsiniz **uzantıları yönetme**.

Yükleme klasörünü ise *%vsinstalldir%\Common7\IDE\Extensions\\* , uzantı varsayılan olarak etkindir.

> [!NOTE]
> **Uzantıları yönetme** aracı, bir VSIX paketinin bir parçası yüklü olduğu sürece bir uzantı erişmek için kullanılamaz.

::: moniker-end

::: moniker range="vs-2017"

*.Pkgdef* dosyaları aşağıdaki konumlardan birinde yüklenmelidir:

- *%LocalAppData%\Microsoft\Visual Studio\15.0\Extensions\\*

- *%vsinstalldir%\Common7\IDE\Extensions\\*

Yükleme klasörünü ise *%localappdata%\Microsoft\Visual Studio\15.0\Extensions\\* , uzantı Visual Studio tarafından kabul edilir, ancak varsayılan olarak devre dışıdır. Kullanıcı uzantıyı kullanarak etkinleştirebilirsiniz **Uzantılar ve güncelleştirmeler**.

Yükleme klasörünü ise *%vsinstalldir%\Common7\IDE\Extensions\\* , uzantı varsayılan olarak etkindir.

> [!NOTE]
> **Uzantılar ve güncelleştirmeler** aracı, bir VSIX paketinin bir parçası yüklü olduğu sürece bir uzantı erişmek için kullanılamaz.

::: moniker-end

## <a name="see-also"></a>Ayrıca bkz.
- [Createexpınstance yardımcı programı](../../extensibility/internals/createexpinstance-utility.md)
