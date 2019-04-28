---
title: Uzantıları Windows Installer dağıtımı için hazırlama | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- vsix msi
ms.assetid: 5ee2d1ba-478a-4cb7-898f-c3b4b2ee834e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9466d067cd144f009f9c0a37d4ace5bacc12f8a2
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62433467"
---
# <a name="prepare-extensions-for-windows-installer-deployment"></a>Uzantıları Windows Installer dağıtımı için hazırlama
Bir Windows Installer paketi (MSI), bir VSIX paketi dağıtmak için kullanamazsınız. Ancak, bir VSIX paketi MSI dağıtım içeriğini ayıklayabilirsiniz. Bu belge, bir kurulum projesi eklenmek üzere bir VSIX paketi varsayılan çıktısı bir projesini Hazırlama işlemi gösterilmektedir.

## <a name="prepare-an-extension-project-for-windows-installer-deployment"></a>Uzantı projesini Windows Installer dağıtımı için hazırlama
 Bu adımları bir kurulum projesi için eklemeden önce yeni uzantı projelerde gerçekleştirin.

### <a name="to-prepare-an-extension-project-for-windows-installer-deployment"></a>Uzantı projesini Windows Installer dağıtımı için hazırlama

1. VSPackage, MEF Bileşeni, düzenleyici kenarlığı veya bir VSIX bildirimi içeren başka bir genişletilebilirlik projesi türü oluşturun.

2. VSIX bildirimi Kod Düzenleyicisi'nde açın.

3. Ayarlama `InstalledByMsi` öğesi için VSIX bildiriminin `true`. VSIX bildirimi hakkında daha fazla bilgi için bkz: [VSIX Uzantı Şeması 2.0 başvurusu](../extensibility/vsix-extension-schema-2-0-reference.md).

     Bu VSIX yükleyicisi bileşeni yüklemek üzere çalışmadan engeller.

4. Projeye sağ **Çözüm Gezgini** tıklatıp **özellikleri**.

5. Seçin **VSIX** sekmesi.

6. Başlıklı kutuyu işaretleyin **kopyalama VSIX içeriğini aşağıdaki konuma** ve Kurulum projesi dosyaları burada çeker yolunu yazın.

## <a name="extract-files-from-an-existing-vsix-package"></a>Var olan bir VSIX paketinden dosyaları ayıklayın
 Kaynak dosyalar olmadığında bir kurulum projesi için mevcut bir VSIX paketinin içeriği eklemek için aşağıdaki adımları gerçekleştirin.

### <a name="to-extract-files-from-an-existing-vsix-package"></a>Varolan bir VSIX paketi dosyalarını ayıklamak için

1. Yeniden adlandırma *. VSIX* dosya uzantısını içeren *filename.vsix* için *filename.zip*.

2. İçeriğini kopyalayın *.zip* bir dizine dosya.

3. Silme *[Content_types] .xml* dosyası.

4. VSIX bildirimi, önceki yordamda gösterildiği gibi düzenleyin.

5. Kalan dosyaları kurulum projenize ekleyin.

## <a name="see-also"></a>Ayrıca bkz.
- [Visual Studio Installer dağıtımı](https://msdn.microsoft.com/library/121be21b-b916-43e2-8f10-8b080516d2a0)
- [İzlenecek yol: Özel Eylem oluştur](/previous-versions/visualstudio/visual-studio-2010/d9k65z2d(v=vs.100))