---
title: Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint Connections [SharePoint development in Visual Studio], extending a node
- SharePoint development in Visual Studio, extending SharePoint Connections node in Server Explorer
- SharePoint Connections [SharePoint development in Visual Studio], creating a new node type
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 6b1d461419497a0a45f50f12589cf3ac978a7666
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967363"
---
# <a name="extend-the-sharepoint-connections-node-in-server-explorer"></a>Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme
  Visual Studio'da geliştirme bilgisayarında yerel SharePoint sitelerine kullanarak bağlanabilirsiniz **SharePoint bağlantıları** düğümünde **Sunucu Gezgini** penceresi. Bu düğüm, birçok yerel SharePoint sitelerine bileşenlerinin bir hiyerarşik ağaç görünümünde görüntüler. Örneğin, yerel sitelerinde listeler, belge kitaplıkları ve içerik türlerini görüntüleyebilirsiniz. Kullanma hakkında daha fazla bilgi için **Sunucu Gezgini** yerel SharePoint sitelerine bağlanmak için bkz: [Sunucu Gezgini kullanarak SharePoint Gözat bağlantıları](../sharepoint/browsing-sharepoint-connections-using-server-explorer.md).

 Genişletebileceğiniz **SharePoint bağlantıları** düğümü var olan düğümleri için uzantıları oluşturarak veya özel düğüm türü oluşturma ve düğüm hiyerarşisine ekleme.

## <a name="tasks-for-extending-the-sharepoint-connections-node"></a>SharePoint bağlantıları düğümünü genişletme ile ilgili görevler
 Varolan bir düğümü genişletmek için uygulayan bir Visual Studio uzantısı oluşturma <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeExtension> arabirimi. Bir düğümünü genişlettiğinizde, düğümü kendi kısayol menüsü öğelerini veya özel özellikler gibi işlevler ekleyebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Sunucu Gezgininde SharePoint düğümünü genişletme](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md).

 Bir özel düğüm türü oluşturmak için uygulayan bir Visual Studio uzantısı oluşturma <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeTypeProvider> arabirimi. Gösterilmez SharePoint siteleri bileşenlerinin görüntülemek istiyorsanız özel bir düğüm oluşturmak **Sunucu Gezgini** varsayılan olarak. Örneğin, **Sunucu Gezgini** bir SharePoint sitesinin varsayılan, ancak Web Bölümü Galerisi'ne ekleyebilirsiniz görüntülemez bunu özel bir düğüm yok. Daha fazla bilgi için [nasıl yapılır: Sunucu Gezginine özel bir SharePoint düğümü ekleme](../sharepoint/how-to-add-a-custom-sharepoint-node-to-server-explorer.md) ve [izlenecek yol: Sunucu gezginini Web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md).

## <a name="add-custom-properties-to-nodes"></a>Düğüm özel özellikler ekleme
 Bir düğümü genişletmek veya bir özel düğüm türü oluşturma, düğüme özel özellikler ekleyebilirsiniz. Özellikleri görünür **özellikleri** düğümü seçildiğinde penceresi.

 Özel özellikler için bir düğüm eklemek iki tür vardır:

- Bir SharePoint sitesinden salt okunur veri kümesini görüntüle özellikleri. Veri düğümünü temsil eder SharePoint bileşeni açıklanmaktadır. Bunun nasıl yapılacağını gösteren bir kılavuz için bkz. [izlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md).

- Özel okuma/yazma veri görüntüleme özellikleri. Bunun nasıl yapılacağını gösteren bir kod örneği için bkz. [nasıl yapılır: Sunucu Gezgininde SharePoint düğümünü genişletme](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md).

## <a name="get-data-for-built-in-nodes"></a>Yerleşik düğümleri için veri alma
 Tüm Visual Studio tarafından sağlanan yerleşik düğümleri temsil ettikleri SharePoint bileşeni ile ilgili bazı bilgiler içerir. Örneğin, SharePoint sitesindeki bir listesini temsil eden bir düğüm listesinde, başlık ve URL listesi için varsayılan görünümünün gibi ilgili bazı bilgiler sağlar.

 Bu verilere erişmek için veri nesnesinden almak <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> özelliği <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNode> ilgilendiğiniz düğümünü temsil eden nesne. Veri nesnesi türü düğüm türüne bağlıdır.

 Aşağıdaki kod örneği için bir liste düğümünü veri nesnesini almak nasıl gösterir. Daha büyük bir örneğin bağlamında bu örnek için bkz [nasıl yapılır: Sunucu Gezgininde yerleşik bir SharePoint düğümü için veri alma](../sharepoint/how-to-get-data-for-a-built-in-sharepoint-node-in-server-explorer.md).

 [!code-vb[SPExtensibility.ProjectSystemExtension.General#11](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/serverexplorerextensionnodeinfo.vb#11)]
 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#11](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/serverexplorerextensionnodeinfo.cs#11)]

 Aşağıdaki tabloda her yerleşik düğüm türü için veri nesnesi türlerini listeler.

|Düğüm türü|Veri nesnesi türü|
|---------------|----------------------|
|SharePoint sitesi düğümü|<xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerSiteNodeInfo>|
|İçerik türü|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IContentTypeNodeInfo>|
|Özellik|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IFeatureNodeInfo>|
|Alan|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IFieldNodeInfo>|
|List|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IListNodeInfo>|
|Liste şablonu|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IListTemplateNodeInfo>|
|Liste Görünümü (Microsoft.SharePoint.SPView)|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IListViewNodeInfo>|
|İş akışı ilişkilendirmesi|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IWorkflowAssociationNodeInfo>|
|İş akışı şablonu|<xref:Microsoft.VisualStudio.SharePoint.Explorer.Extensions.IWorkflowTemplateNodeInfo>|

 Kullanma hakkında daha fazla bilgi için <xref:Microsoft.VisualStudio.SharePoint.IAnnotatedObject.Annotations%2A> özelliğine bakın [SharePoint ile özel verileri ilişkilendirme araçları uzantıları](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md).

## <a name="see-also"></a>Ayrıca bkz.
- [İzlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md)
- [Nasıl yapılır: Sunucu Gezgininde SharePoint düğümünü genişletme](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md)
- [Nasıl yapılır: Sunucu Gezginine özel bir SharePoint düğümü ekleme](../sharepoint/how-to-add-a-custom-sharepoint-node-to-server-explorer.md)
- [Nasıl yapılır: Sunucu Gezgininde yerleşik bir SharePoint düğümü için veri alma](../sharepoint/how-to-get-data-for-a-built-in-sharepoint-node-in-server-explorer.md)
- [SharePoint araç uzantıları ile özel verileri ilişkilendirme](../sharepoint/associating-custom-data-with-sharepoint-tools-extensions.md)
- [Sunucu Gezgini kullanarak SharePoint bağlantılarına göz atın](../sharepoint/browsing-sharepoint-connections-using-server-explorer.md)
- [SharePoint araçlarını Visual Studio'da genişletme](../sharepoint/extending-the-sharepoint-tools-in-visual-studio.md)
