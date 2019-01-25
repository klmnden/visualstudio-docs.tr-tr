---
title: 'Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama | Microsoft Docs'
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
ms.openlocfilehash: bfb04256a1bb8aacb062f30839566b75b599a3a3
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54872033"
---
# <a name="how-to-define-a-sharepoint-project-item-type"></a>Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama
  Özel bir SharePoint proje öğesi oluşturmak istediğinizde bir proje öğesi türünü tanımlar. Daha fazla bilgi için [özel SharePoint proje öğesi türleri tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md).  
  
### <a name="to-define-a-project-item-type"></a>Bir proje öğesi türü tanımlama  
  
1.  Bir sınıf kitaplığı projesi oluşturun.  
  
2.  Aşağıdaki derlemelere başvurular ekleyin:  
  
    -   Microsoft.VisualStudio.SharePoint  
  
    -   System.ComponentModel.Composition  
  
3.  Uygulayan bir sınıf oluşturma <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider> arabirimi.  
  
4.  Sınıfına aşağıdaki öznitelikler ekleyin:  
  
    -   <xref:System.ComponentModel.Composition.ExportAttribute>. Bu öznitelik bulmak ve yüklemek Visual Studio sağlar, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider> uygulaması. Geçirmek <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider> özniteliği Oluşturucu türü.  
  
    -   <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemTypeAttribute>. Proje öğesi türü tanımında, bu öznitelik yeni proje öğesinin dize tanımlayıcısını belirtir. Biçimini kullanmanızı öneririz *şirket adı*. *özellik adı* tüm proje öğeleri benzersiz bir ada sahip olduğundan emin olun yardımcı olmak için.  
  
    -   <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemIconAttribute>. Bu öznitelik bu proje öğesi için görüntülenecek simge belirtir **Çözüm Gezgini**. Bu öznitelik isteğe bağlıdır; sınıfı, uygulamazsanız Visual Studio, proje öğesi için varsayılan bir simge görüntüler. Bu öznitelik ayarlanırsa, bir simge ya da, bir derlemede gömülü olan bit eşlem tam olarak nitelenmiş adını geçirin.  
  
5.  Uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeProvider.InitializeType%2A> yöntemi, kullanım üyeleri *projectItemTypeDefinition* proje öğesi türü davranışını tanımlamak için parametre. Bu parametre bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition> tanımlanan olaylara erişim sağlayan nesne <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemFileEvents> arabirimleri. Proje öğesi türünü belirli bir örneğine erişmesi için tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents> gibi olayları <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemAdded> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.ProjectItemInitialized>.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde nasıl basit bir proje öğesi türü tanımlayacağınızı gösterir. Bu proje öğesi türü için bir ileti yazar **çıkış** penceresi ve **hata listesi** penceresini bir kullanıcı bu türde bir proje öğesi projeye ekler.  
  
 [!code-vb[SPExtensibility.ProjectSystemExtension.General#2](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/projectitemtype.vb#2)]
 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#2](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/projectitemtype.cs#2)]  
  
 Bu örnekte, ileti yazmak için SharePoint Proje hizmeti kullanır. **çıkış** penceresi ve **hata listesi** penceresi. Daha fazla bilgi için [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).  
  
## <a name="compile-the-code"></a>Kod derleme  
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:  
  
-   Microsoft.VisualStudio.SharePoint  
  
-   System.ComponentModel.Composition  
  
## <a name="deploy-the-project-item"></a>Proje öğesi dağıtma  
 Diğer geliştiricilerin, proje öğesini kullanmak için bir proje şablonu veya bir proje öğesi şablon oluşturun. Daha fazla bilgi için [öğe şablonları ve proje şablonları SharePoint Proje öğeleri için oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md).  
  
 Proje öğesini dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme, şablon ve proje öğesi ile dağıtmak istediğiniz diğer tüm dosyalar. Daha fazla bilgi için [uzantıları dağıtmak için SharePoint araçları Visual Studio'da](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Özel SharePoint proje öğesi türlerini tanımlama](../sharepoint/defining-custom-sharepoint-project-item-types.md)   
 [Öğe şablonları ve SharePoint Proje öğeleri için proje şablonları oluşturma](../sharepoint/creating-item-templates-and-project-templates-for-sharepoint-project-items.md)   
 [İzlenecek yol: Bir öğe şablonu, bölüm 1 ile özel bir eylem proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-custom-action-project-item-with-an-item-template-part-1.md)   
 [İzlenecek yol: Bir proje şablonu, bölüm 1 ile bir site sütunu proje öğesi oluşturma](../sharepoint/walkthrough-creating-a-site-column-project-item-with-a-project-template-part-1.md)   
 [Nasıl yapılır: Özel bir SharePoint Proje öğe türüne özellik ekleme](../sharepoint/how-to-add-a-property-to-a-custom-sharepoint-project-item-type.md)   
 [Nasıl yapılır: Özel bir SharePoint Proje öğe türüne bir kısayol menü öğesi ekleme](../sharepoint/how-to-add-a-shortcut-menu-item-to-a-custom-sharepoint-project-item-type.md)  
