---
title: SharePoint projeleri genişletme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- projects [SharePoint development in Visual Studio], extending
- SharePoint development in Visual Studio, extending projects
- SharePoint projects, extending
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6bc92d65ed179c7f2cb2f569a7d254a025887845
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967487"
---
# <a name="extend-sharepoint-projects"></a>SharePoint projeleri genişletme
  SharePoint projeleri için proje düzeyi özelliklerini özelleştirmek istediğinizde bir proje uzantısı oluşturma. Örneğin, özel Proje Özellikleri ekleyebilir veya kullanıcı bir SharePoint çözümünü Visual Studio'da geliştirdiğinde başlatan proje düzeyinde olaylara yanıt verme.

## <a name="create-project-extensions"></a>Proje uzantıları oluşturma
 Bir proje öğesi genişletmek için uygulayan bir Visual Studio uzantısı derleme <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> arabirimi. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md).

 Bir proje uzantısı oluşturma, SharePoint projeleri için aşağıdaki işlevler de ekleyebilirsiniz:

- Bir kısayol menü öğesi ekleyin. Bir SharePoint proje düğümü için kısayol menüsünü açtığınızda, menü öğesi görünür **Çözüm Gezgini** düğümü veya seçmeden sağ tıklayıp ardından **Shift** +  **F10** anahtarları. Daha fazla bilgi için [nasıl yapılır: Bir kısayol menü öğesini SharePoint projelerine ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md).

- Özel bir özellik ekleyin. Özellik görünür **özellikleri** bir SharePoint projesinde seçtiğinizde penceresi **Çözüm Gezgini**. Daha fazla bilgi için [nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md).

  Oluşturmanıza, dağıtmanıza ve proje uzantısını test yapmayı gösteren bir kılavuz için bkz. [izlenecek yol: Bir SharePoint proje uzantısı oluşturma](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md).

## <a name="understand-the-relationship-between-project-extensions-and-project-instances"></a>Proje Uzantılar ve proje örnekleri arasındaki ilişkiyi anlamak
 Bir proje uzantısı oluşturma, herhangi bir türden SharePoint projesi açıldığında uzantınızı yüklediği [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)]. [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] Liste tanımları, içerik türleri ve Olay alıcıları gibi bazı SharePoint proje şablonlarını içerir. Ancak, yalnızca bir SharePoint proje türü yoktur. Proje türleri **yeni proje** iletişim kutusu, yalnızca bir veya daha fazla SharePoint Proje öğeleri gruplamak şablonlardır. Yalnızca bir SharePoint proje türü olduğundan, uzantıları bir proje için oluşturulan tüm SharePoint projeleri için geçerlidir. Örneğin, yalnızca geçerli bir uzantı oluşturamazsınız bir **içerik türü** proje.

 Belirli bir proje örneği erişmek için aşağıdakilerden birini işlemek <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents> olayları *projectService* uygulamanızda parametresi <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension.Initialize%2A> yöntemi. Örneğin, bir SharePoint projesine bir çözüme eklendiğinde belirlemek için tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectAdded> olay. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md)
- [Nasıl yapılır: Bir kısayol menü öğesini SharePoint projelerine ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-sharepoint-projects.md)
- [Nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md)
- [İzlenecek yol: Bir SharePoint proje uzantısı oluşturma](../sharepoint/walkthrough-creating-a-sharepoint-project-extension.md)
- [Özel SharePoint proje öğesi türlerini tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md)
- [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)
- [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)
- [SharePoint Proje sistemini genişletme](../sharepoint/extending-the-sharepoint-project-system.md)
