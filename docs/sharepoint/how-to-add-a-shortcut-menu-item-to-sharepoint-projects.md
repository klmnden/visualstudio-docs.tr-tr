---
title: 'Nasıl Yapılır: Bir kısayol menü öğesini SharePoint projelerine ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- projects [SharePoint development in Visual Studio], extending
- SharePoint development in Visual Studio, extending projects
- SharePoint projects, extending
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: ba38984b5c49dbf834286414e61734fe46069876
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53964143"
---
# <a name="how-to-add-a-shortcut-menu-item-to-sharepoint-projects"></a>Nasıl Yapılır: Bir kısayol menü öğesini SharePoint projelerine ekleme
  Herhangi bir SharePoint projesine bir kısayol menü öğesi ekleyebilirsiniz. Bir kullanıcı,'nde proje düğümüne sağ tıkladığı zaman menü öğesi görünür **Çözüm Gezgini**.  
  
 Aşağıdaki adımlar, bir proje uzantısı zaten oluşturduğunuzu varsayalım. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md).  
  
### <a name="to-add-a-shortcut-menu-item-to-sharepoint-projects"></a>Bir kısayol menü öğesini SharePoint projelerine ekleme  
  
1.  İçinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension.Initialize%2A> yöntemi, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectExtension> uygulama, tanıtıcısını <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectMenuItemsRequested> olayı *projectService* parametresi.  
  
2.  Sizin için olay işleyicisinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectMenuItemsRequested> olay, yeni bir <xref:Microsoft.VisualStudio.SharePoint.IMenuItem> nesnesini <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectMenuItemsRequestedEventArgs.ActionMenuItems%2A> veya <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectMenuItemsRequestedEventArgs.AddMenuItems%2A> olay bağımsız değişkenleri parametre koleksiyonu.  
  
3.  İçinde <xref:Microsoft.VisualStudio.SharePoint.IMenuItem.Click> yeni olay işleyicisi <xref:Microsoft.VisualStudio.SharePoint.IMenuItem> nesne, istediğiniz kullanıcı kısayol menü öğesine tıkladığında yürütülecek görevleri gerçekleştirin.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, bir kısayol menü öğesini SharePoint Proje düğümleri eklemek gösterilmiştir **Çözüm Gezgini**. Kullanıcı bir proje düğümünü sağ tıklatır ve tıkladığında **ileti yazmak için çıkış penceresine** menü öğesi, Visual Studio, bir ileti görüntüler **çıkış** penceresi. Bu örnek, iletiyi görüntülemek için SharePoint Proje hizmeti kullanır. Daha fazla bilgi için [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).  
  
 [!code-csharp[SPExtensibility.ProjectExtension.Menu#1](../sharepoint/codesnippet/CSharp/projectmenu/extension/projectitemextensionmenu.cs#1)]
 [!code-vb[SPExtensibility.ProjectExtension.Menu#1](../sharepoint/codesnippet/VisualBasic/projectmenu/extension/projectitemextensionmenu.vb#1)]  
  
## <a name="compile-the-code"></a>Kod derleme  
 Bu örnek aşağıdaki derlemelere başvurular içeren bir sınıf kitaplığı projesi gerektirir:  
  
-   Microsoft.VisualStudio.SharePoint
-     
-   System.ComponentModel.Composition  
  
## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak  
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint projeleri genişletme](../sharepoint/extending-sharepoint-projects.md)   
 [Nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md)   
 [Nasıl yapılır: SharePoint projelerine özellik ekleme](../sharepoint/how-to-add-a-property-to-sharepoint-projects.md)  
