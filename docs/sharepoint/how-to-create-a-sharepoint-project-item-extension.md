---
title: 'Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma | Microsoft Docs'
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
ms.openlocfilehash: 42cea2633ceb0cbda1c63b76a4e2b7775e967bc2
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56597107"
---
# <a name="how-to-create-a-sharepoint-project-item-extension"></a>Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma
  Visual Studio'da yüklü olan bir SharePoint proje öğesi işlevselliği eklemek istediğinizde bir proje öğesi uzantısı oluşturma. Daha fazla bilgi için [genişletmek SharePoint Proje öğeleri](../sharepoint/extending-sharepoint-project-items.md).

### <a name="to-create-a-project-item-extension"></a>Bir proje öğesi uzantısını oluşturmak için

1.  Bir sınıf kitaplığı projesi oluşturun.

2.  Aşağıdaki derlemelere başvurular ekleyin:

    -   Microsoft.VisualStudio.SharePoint

    -   System.ComponentModel.Composition

3.  Uygulayan bir sınıf oluşturma <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension> arabirimi.

4.  Sınıfına aşağıdaki öznitelikler ekleyin:

    -   <xref:System.ComponentModel.Composition.ExportAttribute>. Bu öznitelik bulmak ve yüklemek Visual Studio sağlar, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension> uygulaması. Geçirmek <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension> özniteliği Oluşturucu türü.

    -   <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemTypeAttribute>. Bu öznitelik, bir proje öğesi uzantısı, genişletmek istediğiniz proje öğesi tanımlar. Proje öğesi kimliği öznitelik yapıcısına geçirin. Visual Studio'da proje öğeleri kimlikleri listesi için bkz. [genişletmek SharePoint Proje öğeleri](../sharepoint/extending-sharepoint-project-items.md).

5.  Uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeExtension.Initialize%2A> yöntemi, kullanım üyeleri *Projectıtemtype* uzantınızı davranışını tanımlamak için parametre. Bu parametre bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemType> tanımlanan olaylara erişim sağlayan nesne <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemFileEvents> arabirimleri. Genişletme proje öğesi türü belirli bir örneğine erişmek için tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents> gibi olayları <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemAdded> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemInitialized>.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, basit bir olay alıcısı proje öğesi uzantısı oluşturma işlemini gösterir. Her kullanıcı bir SharePoint projesine bir olay alıcısı proje öğesi ekler, bu uzantı için bir ileti yazar **çıkış** penceresi ve **hata listesi** penceresi.

 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#1](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/projectitemextension.cs#1)]
 [!code-vb[SPExtensibility.ProjectSystemExtension.General#1](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/projectitemextension.vb#1)]

 Bu örnekte, ileti yazmak için SharePoint Proje hizmeti kullanır. **çıkış** penceresi ve **hata listesi** penceresi. Daha fazla bilgi için [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:

-   Microsoft.VisualStudio.SharePoint

-   System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)
- [İzlenecek yol: Bir SharePoint proje öğesi türünü genişletme](../sharepoint/walkthrough-extending-a-sharepoint-project-item-type.md)
