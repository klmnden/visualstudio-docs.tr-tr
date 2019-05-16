---
title: Uzantıları Windows Installer dağıtımı için hazırlama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- vsix msi
ms.assetid: 5ee2d1ba-478a-4cb7-898f-c3b4b2ee834e
caps.latest.revision: 16
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 76d7f879fade99914bf3f56ade0ec1270e14f4c7
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694589"
---
# <a name="preparing-extensions-for-windows-installer-deployment"></a>Uzantıları Windows Installer Dağıtımı için Hazırlama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir Windows Installer paketi (MSI), bir VSIX paketi dağıtmak için kullanamazsınız. Ancak, bir VSIX paketi MSI dağıtım içeriğini ayıklayabilirsiniz. Bu belge, bir kurulum projesi eklenmek üzere bir VSIX paketi varsayılan çıktısı bir projesini Hazırlama işlemi gösterilmektedir.  
  
## <a name="preparing-an-extension-project-for-windows-installer-deployment"></a>Uzantı projesini Windows Installer dağıtımı için hazırlama  
 Bu adımları bir kurulum projesi için eklemeden önce yeni uzantı projelerde gerçekleştirin.  
  
#### <a name="to-prepare-an-extension-project-for-windows-installer-deployment"></a>Uzantı projesini Windows Installer dağıtımı için hazırlama  
  
1. VSPackage, MEF Bileşeni, düzenleyici kenarlığı veya bir VSIX bildirimi içeren başka bir genişletilebilirlik projesi türü oluşturun.  
  
2. VSIX bildirimi Kod Düzenleyicisi'nde açın.  
  
3. Ayarlamak için VSIX bildirimi Installedbymsı öğesi `true`. VSIX bildirimi hakkında daha fazla bilgi için bkz: [VSIX Uzantı Şeması 2.0 başvurusu](../extensibility/vsix-extension-schema-2-0-reference.md).  
  
     Bu VSIX yükleyicisi bileşeni yüklemek üzere çalışmadan engeller.  
  
4. Projeye sağ **Çözüm Gezgini** tıklatıp **özellikleri**.  
  
5. Seçin **VSIX** sekmesi.  
  
6. Başlıklı kutuyu işaretleyin **kopyalama VSIX içeriğini aşağıdaki konuma** ve Kurulum projesi dosyaları burada çeker yolunu yazın.  
  
## <a name="extracting-files-from-an-existing-vsix-package"></a>Varolan bir VSIX paketi dosyalar ayıklanıyor  
 Kaynak dosyalar olmadığında bir kurulum projesi için mevcut bir VSIX paketinin içeriği eklemek için aşağıdaki adımları gerçekleştirin.  
  
#### <a name="to-extract-files-from-an-existing-vsix-package"></a>Varolan bir VSIX paketi dosyalarını ayıklamak için  
  
1. Yeniden adlandırın. VSIX dosya uzantısını içeren *filename*.vsix *filename*.zip.  
  
2. .Zip dosyasının içeriğini bir dizine kopyalayın.  
  
3. [Content_types] .xml dosyasının dizinden silin.  
  
4. VSIX bildirimi, önceki yordamda gösterildiği gibi düzenleyin.  
  
5. Kalan dosyaları kurulum projenize ekleyin.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Installer dağıtımı](https://msdn.microsoft.com/121be21b-b916-43e2-8f10-8b080516d2a0)   
 [İzlenecek yol: Bir özel eylem oluşturma](https://msdn.microsoft.com/4bd4b63a-2b91-431e-839c-5752443f0eaf)
