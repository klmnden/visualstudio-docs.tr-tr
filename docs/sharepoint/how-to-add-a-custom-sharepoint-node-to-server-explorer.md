---
title: 'Nasıl yapılır: Sunucu Gezginine özel bir SharePoint düğümü ekleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, extending SharePoint Connections node in Server Explorer
- SharePoint Connections [SharePoint development in Visual Studio], creating a new node type
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 7e68d15c195983a087ed335718b02d0bd95b5ff3
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54868725"
---
# <a name="how-to-add-a-custom-sharepoint-node-to-server-explorer"></a>Nasıl yapılır: Sunucu Gezginine özel bir SharePoint düğümü ekleme
  Özel düğüm altında ekleyebilirsiniz **SharePoint bağlantıları** düğümünde **Sunucu Gezgini**. Gösterilmez ek SharePoint bileşenlerini görüntülemek istediğiniz gerektiğinde bu faydalıdır **Sunucu Gezgini** varsayılan olarak. Daha fazla bilgi için [Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme](../sharepoint/extending-the-sharepoint-connections-node-in-server-explorer.md).  
  
 Özel bir düğüm eklemek için öncelikle yeni düğümü tanımlayan bir sınıf oluşturun. Ardından, düğümün alt öğesi var olan bir düğüm olarak ekleyen bir uzantı oluşturun.  
  
### <a name="to-define-the-new-node"></a>Yeni düğüm tanımlamak için  
  
1.  Bir sınıf kitaplığı projesi oluşturun.  
  
2.  Aşağıdaki derlemelere başvurular ekleyin:  
  
    -   Microsoft.VisualStudio.SharePoint  
  
    -   Microsoft.VisualStudio.SharePoint.Explorer.Extensions  
  
    -   System.ComponentModel.Composition  
  
    -   System.Drawing  
  
3.  Uygulayan bir sınıf oluşturma <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeProvider> arabirimi.  
  
4.  Sınıfına aşağıdaki öznitelikler ekleyin:  
  
    -   <xref:System.ComponentModel.Composition.ExportAttribute>. Bu öznitelik bulmak ve yüklemek Visual Studio sağlar, <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeProvider> uygulaması. Geçirmek <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeProvider> özniteliği Oluşturucu türü.  
  
    -   <xref:Microsoft.VisualStudio.SharePoint.Explorer.ExplorerNodeTypeAttribute>. Bir düğüm tanımında, bu öznitelik yeni düğümü için dize tanımlayıcısını belirtir. Biçimini kullanmanızı öneririz *şirket adı*. *düğüm adı* tüm düğümleri benzersiz bir tanımlayıcı olup olmadığından emin olun.  
  
5.  Uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeProvider.InitializeType%2A> yöntemi, kullanım üyeleri *typeDefinition* yeni düğümü davranışını yapılandırmak için parametre. Bu parametre bir <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeDefinition> tanımlanan olaylara erişim sağlayan nesne <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeEvents> arabirimi.  
  
     Aşağıdaki kod örneği, yeni bir düğüm tanımlamak gösterilmektedir. Bu örnek, projenizi CustomChildNodeIcon katıştırılmış bir kaynağı olarak adlandırılan bir simge içeren varsayar.  
  
     [!code-vb[SPExtensibility.ProjectSystemExtension.General#6](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/serverexplorernode.vb#6)]
     [!code-csharp[SPExtensibility.ProjectSystemExtension.General#6](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/serverexplorernode.cs#6)]  
  
### <a name="to-add-the-new-node-as-a-child-of-an-existing-node"></a>Yeni düğümün alt öğesi var olan bir düğüm olarak eklemek için  
  
1.  Uygulayan bir sınıf, düğüm tanımı olarak aynı projede oluşturma <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeExtension> arabirimi.  
  
2.  Ekleme <xref:System.ComponentModel.Composition.ExportAttribute> öznitelik sınıfı. Bu öznitelik bulmak ve yüklemek Visual Studio sağlar, <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeExtension> uygulaması. Geçirmek <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeExtension> özniteliği Oluşturucu türü.  
  
3.  Ekleme <xref:Microsoft.VisualStudio.SharePoint.Explorer.ExplorerNodeTypeAttribute> öznitelik sınıfı. Bir düğüm uzantısı'nda, bu öznitelik, genişletmek istediğiniz düğüm türü için dize tanımlayıcısını belirtir.  
  
     Visual Studio tarafından sağlanan yerleşik düğüm türlerini belirtmek için aşağıdaki numaralandırma değerlerinden biri öznitelik yapıcısına geçirin:  
  
    -   <xref:Microsoft.VisualStudio.SharePoint.Explorer.ExplorerNodeTypes>: Site bağlantı düğümleri (site URL'leri görüntüleme düğüm) belirtmek için bu değerleri site düğümleri veya diğer tüm üst düğümleri kullanım **Sunucu Gezgini**.  
  
    -   <xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.ExtensionNodeTypes>: Bu değerleri bir liste, alan veya içerik türünü temsil eden bir düğüm gibi bir SharePoint sitesindeki tek tek bir bileşen temsil eden yerleşik düğümlerinden belirtmek için kullanın.  
  
4.  Uygulamanızda <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeExtension.Initialize%2A> yöntemi, tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeEvents.NodeChildrenRequested> olayı <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeType> parametresi.  
  
5.  İçinde <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeEvents.NodeChildrenRequested> olay işleyicisi, alt düğümleri koleksiyonu için yeni düğümü eklemek <xref:Microsoft.VisualStudio.SharePoint.Explorer.ExplorerNodeEventArgs.Node%2A> olay bağımsız değişkenleri parametresi tarafından açık bir nesne.  
  
     Aşağıdaki kod örneği, yeni düğümü bir alt öğesi SharePoint sitesi düğümü olarak eklemek gösterilmiştir **Sunucu Gezgini**.  
  
     [!code-vb[SPExtensibility.ProjectSystemExtension.General#7](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/serverexplorernode.vb#7)]
     [!code-csharp[SPExtensibility.ProjectSystemExtension.General#7](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/serverexplorernode.cs#7)]  
  
## <a name="complete-example"></a>Tam örnek
 Aşağıdaki kod örneği basit bir düğüm tanımlamak ve eklemek, SharePoint sitesi düğümünün alt öğesi için tam kod sağlar **Sunucu Gezgini**.  
  
 [!code-vb[SPExtensibility.ProjectSystemExtension.General#5](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/serverexplorernode.vb#5)]
 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#5](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/serverexplorernode.cs#5)]  
  
## <a name="compiling-the-code"></a>Kod derleme  
 Bu örnek, projenizi CustomChildNodeIcon katıştırılmış bir kaynağı olarak adlandırılan bir simge içeren varsayar. Bu örnek ayrıca aşağıdaki derlemelere başvurular gerektirir:  
  
-   Microsoft.VisualStudio.SharePoint  
  
-   System.ComponentModel.Composition  
  
-   System.Drawing  
  
## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak  
 Dağıtılacak **Sunucu Gezgini** uzantısı oluşturma bir [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme](../sharepoint/extending-the-sharepoint-connections-node-in-server-explorer.md)   
 [Nasıl yapılır: Sunucu Gezgininde SharePoint düğümünü genişletme](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md)   
 [İzlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md)  
