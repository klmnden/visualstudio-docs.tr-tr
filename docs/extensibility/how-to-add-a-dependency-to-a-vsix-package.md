---
title: 'Nasıl Yapılır: VSIX paketine bağımlılık ekleme | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- package reference
- package assembly
- package dll
- vsix reference
ms.assetid: 8f20177b-dab9-43a3-b959-81a591b451d6
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 7ce21c10f1a64bf8edad9181d66b83291d0405c4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53902486"
---
# <a name="how-to-add-a-dependency-to-a-vsix-package"></a>Nasıl Yapılır: VSIX paketine bağımlılık ekleme

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

 [VSIX Uzantı Şeması 1.0 başvurusu](https://msdn.microsoft.com/library/76e410ec-b1fb-4652-ac98-4a4c52e09a2b)   
 [Bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md)   
 [Uzantıları Windows Installer dağıtımı için hazırlama](../extensibility/preparing-extensions-for-windows-installer-deployment.md)
