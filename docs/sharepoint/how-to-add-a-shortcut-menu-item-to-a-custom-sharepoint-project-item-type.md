---
title: 'Nasıl yapılır: Özel SharePoint Proje öğe türüne bir kısayol menü öğesi ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint project items, defining your own types
- project items [SharePoint development in Visual Studio], defining your own types
- SharePoint development in Visual Studio, defining new project item types
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e28c5802b866c7fea0b1e079e2d22aecee60e690
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56621545"
---
# <a name="how-to-add-a-shortcut-menu-item-to-a-custom-sharepoint-project-item-type"></a>Nasıl yapılır: Özel bir SharePoint Proje öğe türüne bir kısayol menü öğesi ekleme
  Özel bir SharePoint proje öğesi türü tanımladığınızda, proje öğesi için bir kısayol menü öğesi ekleyebilirsiniz. Bir kullanıcı proje öğesine tıkladığında menü öğesi görünür **Çözüm Gezgini**.

 Aşağıdaki adımlarda kendi SharePoint proje öğesi türü zaten tanımlamış olduğunuz varsayılır. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint proje öğesi türü tanımlayacağınızı](../sharepoint/how-to-define-a-sharepoint-project-item-type.md).

### <a name="to-add-a-shortcut-menu-item-to-a-custom-project-item-type"></a>Bir özel Proje öğe türüne bir kısayol menü öğesi eklemek için

1.  İçinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider.InitializeType%2A> yöntemi, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider> uygulama, tanıtıcısını <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemMenuItemsRequested> olayı *projectItemTypeDefinition* parametresi.

2.  Sizin için olay işleyicisinde <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemMenuItemsRequested> olay, yeni bir <xref:Microsoft.VisualStudio.SharePoint.IMenuItem> nesnesini <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemMenuItemsRequestedEventArgs.ViewMenuItems%2A> veya <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemMenuItemsRequestedEventArgs.AddMenuItems%2A> olay bağımsız değişkenleri parametre koleksiyonu.

3.  İçinde <xref:Microsoft.VisualStudio.SharePoint.IMenuItem.Click> yeni olay işleyicisi <xref:Microsoft.VisualStudio.SharePoint.IMenuItem> nesne, istediğiniz bir kullanıcı, bir kısayol menü öğesi seçtiğinde yürütülecek görevleri gerçekleştirin.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, bir özel Proje öğe türüne bir bağlam menüsü öğesi eklemek gösterilmektedir. Kullanıcı açtığında kısayol menüsünü Proje öğesinden **Çözüm Gezgini** seçerse **ileti yazmak için çıkış penceresine** menü öğesi, Visual Studio, bir ileti görüntüler **çıkış**  penceresi.

 [!code-csharp[SPExtensibility.ProjectItemExtension.MenuAndProperty#4](../sharepoint/codesnippet/CSharp/projectitemmenuandproperty/extension/projectitemtypemenu.cs#4)]
 [!code-vb[SPExtensibility.ProjectItemExtension.MenuAndProperty#4](../sharepoint/codesnippet/VisualBasic/projectitemmenuandproperty/extension/projectitemtypemenu.vb#4)]

 Bu örnekte, ileti yazmak için SharePoint Proje hizmeti kullanır. **çıkış** penceresi. Daha fazla bilgi için [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular içeren bir sınıf kitaplığı projesi gerektirir:

-   Microsoft.VisualStudio.SharePoint

-   System.ComponentModel.Composition

## <a name="deploy-the-project-item"></a>Proje öğesi dağıtma
 Diğer geliştiricilerin, proje öğesini kullanmak için bir proje şablonu veya bir proje öğesi şablon oluşturun. Daha fazla bilgi için [öğe şablonları ve proje şablonları SharePoint Proje öğeleri için oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md).

 Proje öğesini dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme, şablon ve proje öğesi ile dağıtmak istediğiniz diğer tüm dosyalar. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)
- [Nasıl yapılır: Özel bir SharePoint Proje öğe türüne özellik ekleme](../sharepoint/how-to-add-a-property-to-a-custom-sharepoint-project-item-type.md)
- [Özel SharePoint proje öğesi türleri tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md)
