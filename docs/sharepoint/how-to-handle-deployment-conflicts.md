---
title: 'Nasıl yapılır: Dağıtım çakışmalarını işleme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
helpviewer_keywords:
- SharePoint development in Visual Studio, extending deployment
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 62e7740915d341eee1bbf5e112c4f09297c98be1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62813805"
---
# <a name="how-to-handle-deployment-conflicts"></a>Nasıl yapılır: Dağıtım çakışmalarını işleme
  Bir SharePoint proje öğesi için dağıtım çakışmalarını işleme için kendi kodunuzu sağlayabilir. Örneğin, geçerli proje öğesi klasördeki tüm dosyaları konumunda zaten mevcut ve geçerli proje öğesi dağıtılmadan önce dağıtılan dosyaları silin olup olmadığını belirlemek. Dağıtım çakışmalarını hakkında daha fazla bilgi için bkz: [genişletme SharePoint paketleme ve dağıtım](../sharepoint/extending-sharepoint-packaging-and-deployment.md).

### <a name="to-handle-a-deployment-conflict"></a>Dağıtım çakışma işlemek için

1. Bir proje öğesi uzantısı, bir proje uzantısı veya yeni bir proje öğesi türü tanımını oluşturun. Daha fazla bilgi için aşağıdaki konulara bakın:

    - [Nasıl yapılır: Bir SharePoint proje öğesi uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-item-extension.md)

    - [Nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md)

    - [Nasıl yapılır: Bir SharePoint proje öğesi türü tanımlama](../sharepoint/how-to-define-a-sharepoint-project-item-type.md)

2. Uzantı, işleme <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepStarted> olayı bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemType> nesne (bir proje öğesi uzantısını veya proje uzantısı) veya bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemTypeDefinition> nesnesinde (yeni bir proje öğesi türü tanımını).

3. Olay işleyicisi, dağıtılmakta proje öğesi ve kendi senaryonuza uygulamak ölçütlere göre dağıtılan çözümün SharePoint sitesindeki arasında bir çakışma olup olmadığını belirler. Kullanabileceğiniz <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemEventArgs.ProjectItem%2A> dağıtılmakta proje öğesi çözümlemek için olay bağımsız değişkenleri parametresinin özelliğini analiz dağıtım konumundaki dosyaları bu amaç için tanımladığınız bir SharePoint komutu çağırarak.

     Çok sayıda çakışma türleri için önce belirlemek hangi dağıtım adımı yürütülürken isteyebilirsiniz. Kullanarak bunu yapabilirsiniz <xref:Microsoft.VisualStudio.SharePoint.DeploymentStepStartedEventArgs.DeploymentStepInfo%2A> olay bağımsız değişkenleri parametresinin özelliği sağlar. Genellikle yerleşik sırasında çakışma algılamasını mantıklıdır rağmen <xref:Microsoft.VisualStudio.SharePoint.Deployment.DeploymentStepIds.AddSolution> dağıtım adımı sırasında herhangi bir dağıtım adımı için çakışmaları denetleyebilirsiniz.

4. Bir çakışma varsa, kullanmak <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentConflictCollection.Add%2A> yöntemi <xref:Microsoft.VisualStudio.SharePoint.DeploymentStepStartedEventArgs.Conflicts%2A> özelliği yeni bir olay bağımsız değişkenlerinin <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentConflict> nesne. Bu nesne, dağıtım çakışması temsil eder. Çağrıda <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentConflictCollection.Add%2A> yöntemi, çakışmayı çözmek için çağrılan yöntem de belirtin.

## <a name="example"></a>Örnek
 Aşağıdaki kod örneği, bir dağıtım çakışma liste tanımı proje öğeleri için bir proje öğesi uzantısını işlemek için temel işlemi gösterilmektedir. Farklı türde bir proje öğesi için bir dağıtım çakışması işlemek için farklı bir dizeyi geçirmek <xref:Microsoft.VisualStudio.SharePoint.SharePointProjectItemTypeAttribute>. Daha fazla bilgi için [genişletmek SharePoint Proje öğeleri](../sharepoint/extending-sharepoint-project-items.md).

 Kolaylık olması için <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepStarted> Bu örnekte olay işleyicisi, bir dağıtım çakışması var olduğunu varsayar (başka bir deyişle, her zaman yeni bir ekler <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentConflict> nesne) ve `Resolve` yöntemi yalnızca döndürür **true** göstermek için çakışma çözüldü. Gerçek bir senaryoda, <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemEvents.DeploymentStepStarted> olay işleyicisi bir dosyada geçerli proje öğesi ve bir dosya dağıtım konumundaki arasında bir çakışma varsa, ilk olarak belirleyin ve ardından ekleyin bir <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentConflict> yalnızca bir çakışma varsa nesne. Örneğin, kullanabileceğinize `e.ProjectItem.Files` özellik dosyalarını proje öğesi ve analiz etmek için olay işleyicisinde dağıtım konumundaki dosyalarını analiz etmek için bir SharePoint komutu çağrısı. Benzer şekilde, gerçek bir senaryoda `Resolve` yöntemi SharePoint sitesi üzerindeki çakışmayı çözmek için bir SharePoint komutu çağrısı. SharePoint komutları oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: Bir SharePoint komutu oluşturma](../sharepoint/how-to-create-a-sharepoint-command.md).

 [!code-vb[SPExtensibility.ProjectItemExtension.DeploymentConflict#1](../sharepoint/codesnippet/VisualBasic/deploymentconflict/extension/deploymentconflictextension.vb#1)]
 [!code-csharp[SPExtensibility.ProjectItemExtension.DeploymentConflict#1](../sharepoint/codesnippet/CSharp/deploymentconflict/extension/deploymentconflictextension.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:

- Microsoft.VisualStudio.SharePoint

- System.ComponentModel.Composition

## <a name="deploy-the-extension"></a>Uzantıyı dağıtmak
 Uzantıyı dağıtmak için oluşturun bir [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (VSIX) paketini derleme ve uzantısıyla dağıtmak istediğiniz diğer tüm dosyalar için. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint paketleme ve dağıtımını genişletme](../sharepoint/extending-sharepoint-packaging-and-deployment.md)
- [SharePoint proje öğelerini genişletme](../sharepoint/extending-sharepoint-project-items.md)
- [Nasıl yapılır: Dağıtım adımları yürütüldüğünde kodu çalıştırma](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md)
- [Nasıl yapılır: Bir SharePoint komutu oluşturma](../sharepoint/how-to-create-a-sharepoint-command.md)
