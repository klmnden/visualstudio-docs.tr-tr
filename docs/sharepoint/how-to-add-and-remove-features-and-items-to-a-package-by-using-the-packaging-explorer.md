---
title: "Nasıl Yapılır: Ekleme ve kaldırma özellikler ve öğeler pakete paketleme Gezgini'ni kullanarak | Microsoft Docs"
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.RAD.PackagingExplorer
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, packages
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: b1211b0bdc3625b915221cfafaa5377d371aaa25
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53880867"
---
# <a name="how-to-add-and-remove-features-and-items-to-a-package-by-using-the-packaging-explorer"></a>Nasıl Yapılır: Ekleme ve özellikler ve öğeler pakete paketleme Gezgini'ni kullanarak kaldırma
  SharePoint öğeleri ve özellikleri dağıtacağınız bir paket yapılandırmak için paketleme Gezgini'ni kullanabilirsiniz. .Wsp dosyanız içinde SharePoint Proje öğeleri ve özellikleri ayarlayabilirsiniz.  
  
 Alternatif olarak, görüntülemek ve etkinleştirme sırasını değiştirmek için özellikleri yeniden sıralamak için paketleme tasarımcısını kullanabilirsiniz. Daha fazla bilgi için [nasıl yapılır: Ekleme ve paket Tasarımcısını kullanarak, özellikler ve öğeler pakete kaldırma](../sharepoint/how-to-add-and-remove-features-and-items-to-a-package-by-using-the-package-designer.md).  
  
## <a name="open-the-packaging-explorer"></a>Paketleme Gezgini  
 Visual Studio çözümünüzü en az bir SharePoint projesi varsa paketleme Gezgini'ni açmak için aşağıdaki yordamı kullanabilirsiniz. Alternatif olarak, paketleme Gezgini otomatik olarak bir özellik veya paket Tasarımcısı görüntülediğinizde açılır. Tüm özellik ve paket tasarımcıları kapattıktan sonra paketleme Gezgini'ni de kapatır.  
  
#### <a name="to-open-the-packaging-explorer"></a>Paketleme Gezgini açmak için  
  
1.  Menü çubuğunda, **görünümü** > **diğer Windows** > **paketleme Gezgini**.  
  
     **Paketleme Gezgini** görünür **araç kutusu**.  
  
## <a name="adding-a-feature-to-a-package"></a>Bir paket için bir özellik ekleme  
 Paketleme Gezgini'ni kullanarak bir pakete yeni ve mevcut özellikler ekleyebilirsiniz.  
  
#### <a name="to-add-a-sharepoint-feature"></a>Bir SharePoint özelliği eklemek için
  
1.  Açık **paketleme Gezgini**, proje için kısayol menüsünü açın ve ardından **Özellik Ekle**.  
  
#### <a name="to-move-an-existing-sharepoint-feature"></a>Mevcut bir SharePoint özelliği taşımak için  
  
1.  Açık **paketleme Gezgini**ve ardından aşağıdaki adımlardan birini gerçekleştirin:  
  
    -   Sürükleme bir **özellik** başka bir projeye bir projeden.  
  
    -   Bir özellik için kısayol menüsünü açın, **Kes**, özelliği taşıyın ve sonra istediğiniz proje için kısayol menüsünü açın **Yapıştır**.  
  
    > [!NOTE]  
    >  Çözümünüzde birden fazla SharePoint projeniz varsa, bu yordamı kullanın.  
  
## <a name="validate-a-feature-or-package"></a>Bir özellik veya paket doğrulama  
 Dosyaları doğrulayarak SharePoint özellikleriniz ve paketleriniz olası sorunları tespit edebilirsiniz. Uyarılar ve hatalar çıkış penceresinde ve Hata Listesi penceresinde görüntülenir.  
  
#### <a name="to-validate-a-sharepoint-feature-or-package"></a>Bir SharePoint özelliği veya paket doğrulamak için
  
1.  Açık **paketleme Gezgini**.  
  
2.  Bir özellik veya paket için bir kısayol menüsünü açın ve ardından **doğrulama**.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Paketleme ve SharePoint çözümlerini dağıtma](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)  
