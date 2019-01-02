---
title: Özel SharePoint proje öğesi türleri tanımlama | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint project items, defining your own types
- project items [SharePoint development in Visual Studio], defining your own types
- SharePoint development in Visual Studio, defining new project item types
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: e4b678d0a4a148bbd8a7414c8a7585b50fbc9c01
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53855172"
---
# <a name="define-custom-sharepoint-project-item-types"></a>Özel SharePoint proje öğesi türlerini tanımlama
  Yeni bir SharePoint proje öğesi türünü oluşturmak istediğinizde, yeni bir SharePoint proje öğesi türü tanımlar. Örneğin, Visual Studio SharePoint Proje öğeleri için alanlar ekleyerek veya bir SharePoint sitesi için özel eylemler dahil değildir. Kendi türlerinizi alanları, özel eylemler veya diğer SharePoint bileşenlerini türleri oluşturmak için SharePoint Proje öğeleri tanımlayabilirsiniz.  
  
## <a name="tasks-for-defining-sharepoint-project-item-types"></a>SharePoint proje öğesi türleri tanımlamak için görevleri
 Özel proje öğesi türü tanımlamak için uygulayan bir Visual Studio uzantısı derleme <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider> arabirimi. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi türü tanımlayacağınızı](../sharepoint/how-to-define-a-sharepoint-project-item-type.md).  
  
 Özel proje öğesi türünü tanımlarken, aşağıdaki işlevleri için proje öğesi de ekleyebilirsiniz:  
  
- Bir kısayol menü öğesi için proje öğesi ekleyin. Proje öğesi için kısayol menüsünü açtığınızda, menü öğesi görünür **Çözüm Gezgini** proje öğesi sağ tıklayarak veya seçip ardından **Shift** +  **F10** anahtarları. Daha fazla bilgi için [nasıl yapılır: Özel bir SharePoint Proje öğe türüne bir kısayol menü öğesi ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-a-custom-sharepoint-project-item-type.md).  
  
- Özel bir özellik için proje öğesi ekleyin. Özellik görünür **özellikleri** proje öğesinde seçtiğinizde penceresi **Çözüm Gezgini**. Daha fazla bilgi için [nasıl yapılır: Özel bir SharePoint Proje öğe türüne özellik ekleme](../sharepoint/how-to-add-a-property-to-a-custom-sharepoint-project-item-type.md).  
  
  Diğer geliştiricilerin, proje öğesi Visual Studio'da kullanmak için bir .spdata dosyası oluşturun ve bir öğe şablonu veya proje öğesi ile ilişkili proje şablonu oluşturun. Daha fazla bilgi için [öğe şablonları ve proje şablonları SharePoint Proje öğeleri için oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md).  
  
## <a name="understand-the-relationship-between-project-item-types-and-project-item-instances"></a>Proje öğesi türleri ve proje öğesi örnekleri arasındaki ilişkiyi anlamak
 Bir SharePoint proje öğesi türünü tanımlarken, Visual Studio bir proje öğesi türüyle bir SharePoint projesine eklendiğinde uzantınızı yükler. Örneğin, yeni bir tanımlarsanız **özel eylem** proje öğesi türü, Visual Studio, bir kullanıcı eklendiğinde uzantınızı yükleyen bir **özel eylem** projesine bir proje. Visual Studio, ilişkili proje öğesi türünün tüm örnekleri için uzantınızı aynı örneğini kullanır. Önceki örnekte kullanıcı ikinci eklerse **özel eylem** projeye proje öğesi, uzantınızı'nın aynı örneğine ikinci proje öğesi özelleştirmek için kullanılır.  
  
 Proje öğesi türünü belirli bir örneğine erişmek için aşağıdakilerden birini işlemek <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents> olayları *projectItemTypeDefinition* uygulamanızda parametresi <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider.InitializeType%2A> yöntemi. Örneğin, bir proje öğesi, özel tür bir projeye eklendiğinde belirlemek için tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemAdded> olay. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi türü tanımlayacağınızı](../sharepoint/how-to-define-a-sharepoint-project-item-type.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)   
 [Nasıl yapılır: Özel bir SharePoint Proje öğe türüne özellik ekleme](../sharepoint/how-to-add-a-property-to-a-custom-sharepoint-project-item-type.md)   
 [Nasıl yapılır: Özel bir SharePoint Proje öğe türüne bir kısayol menü öğesi ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-a-custom-sharepoint-project-item-type.md)   
 [Öğe şablonları ve SharePoint Proje öğeleri için proje şablonları oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md)   
 [İzlenecek yol: Bir öğe şablonu, bölüm 1 ile özel bir eylem proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-custom-action-project-item-with-an-item-template-part-1.md)   
 [İzlenecek yol: Bir proje şablonu, bölüm 1 ile site sütunu proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-site-column-project-item-with-a-project-template-part-1.md)   
 [İzlenecek yol: Bir öğe şablonu, bölüm 2 ile özel bir eylem proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-custom-action-project-item-with-an-item-template-part-2.md)   
 [İzlenecek yol: Bir proje şablonu, bölüm 2 ile bir site sütunu proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-site-column-project-item-with-a-project-template-part-2.md)   
 [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md)  
