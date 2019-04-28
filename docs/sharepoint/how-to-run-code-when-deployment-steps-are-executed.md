---
title: 'Nasıl yapılır: Çalıştırma zaman dağıtım adımları yürütüldüğünde kodu | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, extending deployment
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 581f9c0b9907fd59863f6a468a45ef67d9966475
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62813158"
---
# <a name="how-to-run-code-when-deployment-steps-are-executed"></a>Nasıl yapılır: Dağıtım adımları yürütüldüğünde kodu çalıştırma
  SharePoint projesindeki bir dağıtım adımı için ek görevler gerçekleştirmek istiyorsanız, önce SharePoint Proje öğeleri ve dağıtımdaki her bir adımın Visual Studio yürütüldükten sonra oluşturulan olayları işleyebilir. Daha fazla bilgi için [genişletme SharePoint paketleme ve dağıtım](../sharepoint/extending-sharepoint-packaging-and-deployment.md).

### <a name="to-run-code-when-deployment-steps-are-executed"></a>Dağıtım adımları yürütüldüğünde kodu çalıştırmak için

1. Bir proje öğesi uzantısı, bir proje uzantısı veya yeni bir proje öğesi türü tanımını oluşturun. Daha fazla bilgi için aşağıdaki konulara bakın:

    - [Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)

    - [Nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md)

    - [Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)

2. Uzantı, işleme <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepStarted> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepCompleted> olayları bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemType> nesne (bir proje öğesi uzantısını veya proje uzantısı) veya bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition> nesnesinde (yeni bir proje öğesi türü tanımını).

3. Olay işleyicilerini kullanmak <xref:Microsoft.VisualStudio.SharePoint.DeploymentStepStartedEventArgs> ve <xref:Microsoft.VisualStudio.SharePoint.DeploymentStepCompletedEventArgs> dağıtım adımı hakkında daha fazla bilgi almak için parametreleri. Örneğin, hangi dağıtım adımı yürütülürken ve çözümü olup ettiğinden belirleyebilirsiniz dağıtılan veya geri çekilebilir.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde nasıl işleneceğini gösterir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepStarted> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepCompleted> liste örneği proje öğesi için bir uzantı olayları. Bu uzantı için ek bir ileti yazar **çıkış** Visual Studio, dağıtma ve çözüm Geri Çekiliyor uygulama havuzu dönüştürüldüğünde penceresi.

 [!code-vb[SPExtensibility.ProjectSystemExtension.General#4](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/handledeploymentstepevents.vb#4)]
 [!code-csharp[SPExtensibility.ProjectSystemExtension.General#4](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/handledeploymentstepevents.cs#4)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:

- Microsoft.VisualStudio.SharePoint

- System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)
- [İzlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturma](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md)
- [Nasıl yapılır: Bir SharePoint projesine dağıtılan ya da geri çekilebilir kodu çalıştırın.](../sharepoint/how-to-run-code-when-a-sharepoint-project-is-deployed-or-retracted.md)
