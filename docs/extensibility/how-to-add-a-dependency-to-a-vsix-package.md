---
title: 'Nasıl yapılır: VSIX paketine bağımlılık ekleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- package reference
- package assembly
- package dll
- vsix reference
ms.assetid: 8f20177b-dab9-43a3-b959-81a591b451d6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ee6ebeb776e6aa85d5fba200ac357a7375fa2b99
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66341054"
---
# <a name="how-to-add-a-dependency-to-a-vsix-package"></a>Nasıl yapılır: VSIX paketine bağımlılık ekleme

Zaten hedef bilgisayarda mevcut olmayan herhangi bir bağımlılığın yükleyen bir VSIX paketi dağıtımı ayarlayabilirsiniz. Bunu yapmak için VSIX bağımlılıklarını içeren *source.extension.vsixmanifest* dosya.

## <a name="to-add-a-dependency"></a>Bir bağımlılık eklemek için

1. Açık *source.extension.vsixmanifest* dosyası **tasarım** görünümü. Git **bağımlılıkları** sekmesine **yeni**.

2. Yüklü uzantı eklemek için: içinde **yeni bağımlılık Ekle** iletişim kutusunda **uzantısı yüklü** ve ardından **adı**, listedeki bir uzantı seçin.

3. Yüklü başka bir VSIX eklemek için: içinde **yeni bağımlılık Ekle** iletişim kutusunda **dosya sisteminde dosya** ve ardından **Gözat** düğmesine VSIX'i seçin.

## <a name="require-a-specific-visual-studio-release"></a>Belirli bir Visual Studio sürüm gerektir

Uzantınızı belirli bir Visual Studio 2017 sürümünü gerektiriyorsa, örneğin, 15.3 sürümünde kullanıma sunulan bir özelliği bağımlı, VSIX'İNİZE yapı numarasını belirtebilirsiniz **InstallationTarget**. Örneğin, bir derleme sayısı '15.0.26730.3' sürüm 15.3 vardır. Yapı numaralarını sürümlerinin eşleme gördüğünüz [burada](../install/visual-studio-build-numbers-and-release-dates.md). Sürüm numarasını '15.3' kullanarak doğru çalışmayacağını unutmayın.

Uzantınızı 15.3 gerektirir ya da üzeri bildirirsiniz **InstallationTarget sürüm** olarak [15.0.26730.3, 16.0):

```xml
<Installation>
  <InstallationTarget Id="Microsoft.VisualStudio.Community" Version="[15.0.26730.3, 16.0)" />
</Installation>
```

Vsıxınstaller Visual Studio'nun önceki sürümleri algılamak ve daha yeni bir güncelleştirme gerekli olduğunu kullanıcıya bildirin.

## <a name="see-also"></a>Ayrıca bkz.

- [VSIX Uzantı Şeması 1.0 başvurusu](https://msdn.microsoft.com/library/76e410ec-b1fb-4652-ac98-4a4c52e09a2b)
- [Bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md)
- [Uzantıları Windows Installer dağıtımı için hazırlama](../extensibility/preparing-extensions-for-windows-installer-deployment.md)
