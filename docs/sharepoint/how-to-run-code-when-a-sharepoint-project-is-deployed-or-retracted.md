---
title: SharePoint Proje dağıtılan ya da geri çekilebilir kodu çalıştırın.
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
ms.openlocfilehash: 9e3f46ff9d2e83307f745180288e69839a0d336e
ms.sourcegitcommit: 25570fb5fb197318a96d45160eaf7def60d49b2b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/30/2019
ms.locfileid: "66401771"
---
# <a name="how-to-run-code-when-a-sharepoint-project-is-deployed-or-retracted"></a>Nasıl yapılır: Bir SharePoint projesine dağıtılan ya da geri çekilebilir kodu çalıştırın.
  Bir SharePoint projesine dağıtılan ya da geri çekilebilir ek görevleri gerçekleştirmek istiyorsanız, Visual Studio tarafından oluşturulan olayları işleyebilir. Daha fazla bilgi için [genişletmek SharePoint paketleme ve dağıtım](../sharepoint/extending-sharepoint-packaging-and-deployment.md).

### <a name="to-run-code-when-a-sharepoint-project-is-deployed-or-retracted"></a>Bir SharePoint projesi kodu çalıştırmak için dağıtılan geri çekilebilir veya

1. Bir proje öğesi uzantısı, bir proje uzantısı veya yeni bir proje öğesi türü tanımını oluşturun. Daha fazla bilgi için aşağıdaki konulara bakın:

   - [Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)

   - [Nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md)

   - [Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)

2. Uzantı, erişim <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService> nesne. Daha fazla bilgi için [nasıl yapılır: SharePoint Proje hizmetini alma](../sharepoint/how-to-retrieve-the-sharepoint-project-service.md).

3. Tanıtıcı <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentStarted> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentCompleted> proje hizmeti olayları.

4. Olay işleyicilerini kullanmak <xref:Microsoft.VisualStudio.SharePoint.DeploymentEventArgs> geçerli dağıtım oturumu hakkında bilgi almak için parametre. Örneğin, geçerli bir dağıtım oturumunda projesidir ve olup ettiğinden belirleyebilirsiniz dağıtılan veya geri çekilebilir.

   Aşağıdaki kod örneğinde nasıl işleneceğini gösterir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentStarted> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.DeploymentCompleted> proje uzantı olayları. Bu uzantı için ek bir ileti yazar **çıkış** dağıtım başlayıp bir SharePoint projesi için tamamlandığında penceresi.

   [!code-csharp[SPExtensibility.ProjectSystemExtension.General#12](../sharepoint/codesnippet/CSharp/projectsystemexamples/extension/handleprojectdeploymentevents.cs#12)]
   [!code-vb[SPExtensibility.ProjectSystemExtension.General#12](../sharepoint/codesnippet/VisualBasic/projectsystemexamples/extension/handleprojectdeploymentevents.vb#12)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:

- Microsoft.VisualStudio.SharePoint

- System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)
- [Nasıl yapılır: Dağıtım adımları yürütüldüğünde kodu çalıştırma](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md)
