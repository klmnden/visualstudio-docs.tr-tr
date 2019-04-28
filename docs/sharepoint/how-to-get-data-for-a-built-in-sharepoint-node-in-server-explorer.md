---
title: 'Nasıl yapılır: Sunucu Gezgininde yerleşik bir SharePoint düğümü için veri alma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint Connections [SharePoint development in Visual Studio], extending a node
- SharePoint development in Visual Studio, extending SharePoint Connections node in Server Explorer
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d1e3ec8fd6598573a60f852727397d6baa63d3e9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62813742"
---
# <a name="how-to-get-data-for-a-built-in-sharepoint-node-in-server-explorer"></a>Nasıl yapılır: Sunucu Gezgininde yerleşik bir SharePoint düğümü için veri alma
  Her yerleşik SharePoint düğümü için **Sunucu Gezgini**, veri düğümünü temsil eden bir temel alınan SharePoint bileşenini Al. Daha fazla bilgi için [Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme](../sharepoint/extending-the-sharepoint-connections-node-in-server-explorer.md).

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, bir liste düğümünü temsil eder temel alınan bir SharePoint listesi için verileri almak gösterilmiştir **Sunucu Gezgini**. Varsayılan olarak, liste düğüme sahip bir **tarayıcıda görüntüle** listeleri bir Web tarayıcısında açmak için tıklayın ve bağlam menüsü öğesi. Bu örnekte liste düğümleri ekleyerek genişletir bir **Görünümü'nde Visual Studio** listeleri doğrudan Visual Studio'da açılır bağlam menüsü öğesi. Kodu Visual Studio'da açmak için listeden URL'sini almak bir düğüm için liste verilerini erişir.

 [!code-vb[SPExtensibility.ProjectSystemExtension.General#10](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/serverexplorerextensionnodeinfo.vb#10)]
 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#10](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/serverexplorerextensionnodeinfo.cs#10)]

 Bu örnek, elde etmek için SharePoint Proje hizmeti kullanır. <xref:EnvDTE.DTE> listeler Visual Studio'da açmak için kullanılan nesne. SharePoint Proje hizmeti hakkında daha fazla bilgi için bkz: [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).

 Bir SharePoint düğümü için bir uzantı oluşturmak için temel görevleri hakkında daha fazla bilgi için bkz: [nasıl yapılır: Sunucu Gezgininde SharePoint düğümünü genişletme](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md).

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:

- EnvDTE

- Microsoft.VisualStudio.SharePoint

- Microsoft.VisualStudio.SharePoint.Explorer.Extensions

- System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Dağıtılacak **Sunucu Gezgini** uzantısı oluşturma bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme](../sharepoint/extending-the-sharepoint-connections-node-in-server-explorer.md)
- [Nasıl yapılır: Sunucu Gezgininde SharePoint düğümünü genişletme](../sharepoint/how-to-extend-a-sharepoint-node-in-server-explorer.md)
- [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md)
- [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md)
