---
title: 'Nasıl yapılır: VSIX paketine bağımlılık ekleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- package reference
- package assembly
- package dll
- vsix reference
ms.assetid: 8f20177b-dab9-43a3-b959-81a591b451d6
caps.latest.revision: 13
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 97118134106614e1e04cd2bc328ad31480618116
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54765448"
---
# <a name="how-to-add-a-dependency-to-a-vsix-package"></a>Nasıl yapılır: VSIX Paketine Bağımlılık Ekleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Zaten hedef bilgisayarda mevcut olmayan herhangi bir bağımlılığın yükleyen bir VSIX paketi dağıtımı ayarlayabilirsiniz. Bunu yapmak için VSIX bağımlılıklarını nde source.extension.vsixmanifest dosyası içerir.  
  
#### <a name="to-add-a-dependency"></a>Bir bağımlılık eklemek için  
  
1.  Source.extension.vsixmanifest dosyasını açın **tasarım** görünümü. Git **bağımlılıkları** sekmesine **yeni**.  
  
2.  Yüklü uzantı eklemek için: içinde **yeni bağımlılık Ekle** iletişim kutusunda **uzantısı yüklü** ve ardından **adı**, listedeki bir uzantı seçin.  
  
3.  Yüklü başka bir VSIX eklemek için:: içinde **yeni bağımlılık Ekle** iletişim kutusunda **dosya sisteminde dosya** ve ardından **Gözat** düğmesine VSIX'i seçin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSIX Uzantı Şeması 1.0 başvurusu](http://msdn.microsoft.com/76e410ec-b1fb-4652-ac98-4a4c52e09a2b)   
 [Bir VSIX paketinin anatomisi](../extensibility/anatomy-of-a-vsix-package.md)   
 [Uzantıları Windows Installer Dağıtımı için Hazırlama](../extensibility/preparing-extensions-for-windows-installer-deployment.md)
