---
title: SharePoint Proje öğe uzantısına kısayol menü öğesi ekleme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- project items [SharePoint development in Visual Studio], extending
- SharePoint project items, extending
- SharePoint development in Visual Studio, extending project items
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8041f9cbf19d1e1324478b92d2655f1377102b81
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66401635"
---
# <a name="how-to-add-a-shortcut-menu-item-to-a-sharepoint-project-item-extension"></a>Nasıl yapılır: Bir SharePoint Proje öğe uzantısına bir kısayol menü öğesi ekleme
  Bir proje öğesi uzantısını kullanarak mevcut bir SharePoint proje öğesi için bir kısayol menü öğesi ekleyebilirsiniz. Bir kullanıcı proje öğesine tıkladığında menü öğesi görünür **Çözüm Gezgini**.

 Aşağıdaki adımlar, bir proje öğesi uzantısı zaten oluşturduğunuzu varsayalım. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md).

### <a name="to-add-a-shortcut-menu-item-in-a-project-item-extension"></a>İçinde bir proje öğe uzantısına bir kısayol menü öğesi eklemek için

1. İçinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension.Initialize%2A> yöntemi, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension> uygulama, tanıtıcısını <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemMenuItemsRequested> olayı *Projectıtemtype* parametresi.

2. Sizin için olay işleyicisinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemMenuItemsRequested> olay, yeni bir <xref:Microsoft.VisualStudio.SharePoint.IMenuItem> nesnesini <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemMenuItemsRequestedEventArgs.ViewMenuItems%2A> veya <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemMenuItemsRequestedEventArgs.AddMenuItems%2A> olay bağımsız değişkenleri parametre koleksiyonu.

3. İçinde <xref:Microsoft.VisualStudio.SharePoint.IMenuItem.Click> yeni olay işleyicisi <xref:Microsoft.VisualStudio.SharePoint.IMenuItem> nesne, istediğiniz kullanıcı kısayol menü öğesine tıkladığında yürütülecek görevleri gerçekleştirin.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği için olay alıcısı proje öğesi bir kısayol menü öğesi ekleme gösterir. Kullanıcı, proje öğeyi tıklattığında **Çözüm Gezgini** ve **ileti yazmak için çıkış penceresine** menü öğesi, Visual Studio, bir ileti görüntüler **çıkış**penceresi.

 [!code-vb[SPExtensibility.ProjectItemExtension.MenuAndProperty#1](../sharepoint/codesnippet/VisualBasic/projectitemmenuandproperty/extension/projectitemextensionmenu.vb#1)]
 [!code-csharp[SPExtensibility.ProjectItemExtension.MenuAndProperty#1](../sharepoint/codesnippet/CSharp/projectitemmenuandproperty/extension/projectitemextensionmenu.cs#1)]

 Bu örnekte, ileti yazmak için SharePoint Proje hizmeti kullanır. **çıkış** penceresi. Daha fazla bilgi için [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular içeren bir sınıf kitaplığı projesi gerektirir:

- Microsoft.VisualStudio.SharePoint

- System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)
- [Nasıl yapılır: Bir SharePoint Proje öğe uzantısına özellik ekleme](../sharepoint/how-to-add-a-property-to-a-sharepoint-project-item-extension.md)
- [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)
- [İzlenecek yol: Bir SharePoint proje öğesi türünü genişletme](../sharepoint/walkthrough-extending-a-sharepoint-project-item-type.md)
