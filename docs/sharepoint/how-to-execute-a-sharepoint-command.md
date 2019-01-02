---
title: 'Nasıl Yapılır: Bir SharePoint komutu yürütme | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint commands [SharePoint development in Visual Studio], executing
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: d6e529420db8261e87c856e2fc80ef436bbc3e73
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53953124"
---
# <a name="how-to-execute-a-sharepoint-command"></a>Nasıl Yapılır: Bir SharePoint komutu yürütme
  Sunucu nesne modeli SharePoint Araçlar uzantısından kullanmak istiyorsanız, özel bir oluşturmalısınız *SharePoint komutu* API'sini çağırmak için. Komut tanımlayıp, SharePoint Araçlar uzantısından ile dağıttıktan sonra uzantınızı komutu SharePoint sunucusu nesne modeline çağrı yürütebilir. Komutu yürütmek için ExecuteCommand yöntemlerinden birini kullanın: bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection> nesne.  
  
 SharePoint komutları amacı hakkında daha fazla bilgi için bkz. [SharePoint nesne modellerini çağırma](../sharepoint/calling-into-the-sharepoint-object-models.md).  
  
### <a name="to-execute-a-sharepoint-command"></a>Bir SharePoint komutu yürütmek için  
  
1.  SharePoint araçları uzantısını edinin bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection> nesne. Size yol bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection> nesnesini oluşturmakta olduğunuz uzantı türüne bağlıdır:  
  
    -   SharePoint Proje sistemi bir uzantı kullanmak <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject.SharePointConnection%2A> özelliği.  
  
         Proje sistemi uzantıları hakkında daha fazla bilgi için bkz. [SharePoint Proje sistemini genişletmek](../sharepoint/extending-the-sharepoint-project-system.md).  
  
    -   ' In bir uzantısı olarak **SharePoint bağlantıları** düğümünde **Sunucu Gezgini**, kullanın <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeContext.SharePointConnection%2A> özelliği. Alınacak bir <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNodeContext> nesnesi <xref:Microsoft.VisualStudio.SharePoint.Explorer.IExplorerNode.Context%2A> özelliği.  
  
         Hakkında daha fazla bilgi için **Sunucu Gezgini** uzantıları, bakın [Sunucu Gezgininde SharePoint bağlantıları düğümünü genişletme](../sharepoint/extending-the-sharepoint-connections-node-in-server-explorer.md).  
  
    -   SharePoint araçlarının bir proje şablonu Sihirbazı gibi bir uzantının parçası olmayan kodu kullanmak <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService.SharePointConnection%2A> özelliği.  
  
         Proje hizmetini alma hakkında daha fazla bilgi için bkz. [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md).  
  
2.  ExecuteCommand yöntemlerinden birini çağırın <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection> nesne. ExecuteCommand yöntemin ilk bağımsız değişkeni yürütmek istediğiniz komutun adı geçirin. Komutunuz özel bir parametreye sahipse, bu parametrenin ExecuteCommand yönteminin ikinci bağımsız değişkeni için geçirin.  
  
     Her desteklenen komut imza için farklı bir ExecuteCommand aşırı yüklemesi vardır. Aşağıdaki tabloda, desteklenen imzalar ve her imzası için kullanılacak olan aşırı yükleme listeler.  
  
    |Komut imzası|Kullanılacak ExecuteCommand aşırı yükleme|  
    |-----------------------|------------------------------------|  
    |Yalnızca varsayılan komut sahip <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandContext> parametre ve dönüş değeri yok.|<xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection.ExecuteCommand%2A>|  
    |Yalnızca varsayılan komut sahip <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandContext> parametre ve dönüş değeri.|<xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection.ExecuteCommand%2A>|  
    |Komut iki parametreye sahiptir (varsayılan <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandContext> parametre ve bir özel parametre) ve dönüş değeri yok.|<xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection.ExecuteCommand%2A>|  
    |Komutu, iki parametre ve dönüş değeri vardır.|<xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection.ExecuteCommand%2A>|  
  
## <a name="example"></a>Örnek  
 Aşağıdaki kod örneğinde nasıl kullanılacağını gösterir <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection.ExecuteCommand%2A> aşırı yüklemesini çağırmak için `Contoso.Commands.UpgradeSolution` açıklanan komutu [nasıl yapılır: Bir SharePoint komutu oluşturma](../sharepoint/how-to-create-a-sharepoint-command.md).  
  
 [!code-csharp[SPExtensibility.ProjectExtension.UpgradeDeploymentStep#6](../sharepoint/codesnippet/CSharp/UpgradeDeploymentStep/deploymentstepextension/upgradestep.cs#6)]
 [!code-vb[SPExtensibility.ProjectExtension.UpgradeDeploymentStep#6](../sharepoint/codesnippet/VisualBasic/upgradedeploymentstep/deploymentstepextension/upgradestep.vb#6)]  
  
 `Execute` Bu örnekte gösterilen uygulaması yöntemdir <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentStep.Execute%2A> yöntemi <xref:Microsoft.VisualStudio.SharePoint.Deployment.IDeploymentStep> özel bir dağıtım adımı arabirimi. Daha büyük bir örneğin bağlamında bu kodu görmek için bkz: [izlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturmak](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md).  
  
 Çağrı ilgili aşağıdaki bilgileri Not <xref:Microsoft.VisualStudio.SharePoint.ISharePointConnection.ExecuteCommand%2A> yöntemi:  
  
-   İlk parametre, aramak istediğiniz komut tanımlar. Bu dize geçirdiğiniz değerle <xref:Microsoft.VisualStudio.SharePoint.Commands.SharePointCommandAttribute> komut tanımı.  
  
-   İkinci parametre özel ikinci parametresi komutun geçirmek istediğiniz değerdir. Bu durumda tam yolu olduğu *.wsp* SharePoint sitesine yükseltilmekte olan dosya.  
  
-   Kod örtük geçirmez <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandContext> komut parametresi. SharePoint Proje sistemi bir uzantı veya uzantısı komuta çağrı yaptığınızda bu parametre komutu otomatik olarak geçirilen **SharePoint bağlantıları** düğümünde **Sunucu Gezgini**. Çözümler, uygulayan bir proje şablonu Sihirbazı gibi diğer tür <xref:Microsoft.VisualStudio.TemplateWizard.IWizard> arabirimidir, bu parametre **null**.  
  
## <a name="compile-the-code"></a>Kod derleme  
 Bu örnek Microsoft.VisualStudio.SharePoint derlemesine bir başvuru gerektirir.  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint nesne modellerini çağırma](../sharepoint/calling-into-the-sharepoint-object-models.md)   
 [Nasıl yapılır: Bir SharePoint komutu oluşturma](../sharepoint/how-to-create-a-sharepoint-command.md)   
 [İzlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md)  
