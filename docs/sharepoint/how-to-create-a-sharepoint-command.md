---
title: 'Nasıl Yapılır: Bir SharePoint komutu oluşturma | Microsoft Docs'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint commands [SharePoint development in Visual Studio], creating
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 7f83447bcceb010f5a479d61c250e703daa1aab1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53894856"
---
# <a name="how-to-create-a-sharepoint-command"></a>Nasıl Yapılır: Bir SharePoint komutu oluşturma
  Sunucu nesne modeli SharePoint Araçlar uzantısından kullanmak istiyorsanız, özel bir oluşturmalısınız *SharePoint komutu* API'sini çağırmak için. Sunucu nesne modeline doğrudan çağırabilir miyim bir derlemede SharePoint komutunun tanımlarsınız.  
  
 SharePoint komutları amacı hakkında daha fazla bilgi için bkz. [SharePoint nesne modellerini çağırma](../sharepoint/calling-into-the-sharepoint-object-models.md).  
  
### <a name="to-create-a-sharepoint-command"></a>Bir SharePoint komutu oluşturma  
  
1.  Aşağıdaki yapılandırmaya sahip bir sınıf kitaplığı projesi oluşturun:  
  
    -   .NET Framework 3.5 hedefler. Hedef Framework'ü seçme hakkında daha fazla bilgi için bkz. [nasıl yapılır: .NET Framework sürümü hedefleme](../ide/how-to-target-a-version-of-the-dotnet-framework.md).  
  
    -   AnyCPU veya x64 hedef platformu. Varsayılan olarak, hedef sınıf kitaplığı projeleri için AnyCPU platformudur. Hedef platformu seçme hakkında daha fazla bilgi için bkz. [nasıl yapılır: Projeleri hedef platformlar için yapılandırma](../ide/how-to-configure-projects-to-target-platforms.md).  
  
    > [!NOTE]  
    >  .NET Framework 3.5 ve SharePoint araçları uzantıları hedef SharePoint komutları hedef, bir SharePoint komutu, SharePoint Araçlar uzantısından tanımlar aynı projede uygulanamıyor [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]. Uzantınızı ayrı bir proje tarafından kullanılan herhangi bir SharePoint komut tanımlamanız gerekir. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
2.  Aşağıdaki derlemelere başvurular ekleyin:  
  
    -   Microsoft.VisualStudio.SharePoint.Commands  
  
    -   Microsoft.SharePoint  
  
3.  Projedeki bir sınıfta, SharePoint komutu tanımlayan bir yöntem oluşturun. Yöntemi, aşağıdaki yönergelere uygun olmalıdır:  
  
    -   Bir veya iki parametre sağlayabilirsiniz.  
  
         İlk parametre olmalıdır bir <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandContext> nesne. Bu nesne Microsoft.SharePoint.SPSite ya da komut yürütüldüğü Microsoft.SharePoint.SPWeb sağlar. Ayrıca sağlar bir <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandLogger> ileti yazmak için kullanılan nesne **çıkış** penceresi veya **hata listesi** Visual Studio'daki.  
  
         İkinci parametre, tercih ettiğiniz bir tür olabilir, ancak bu isteğe bağlı bir parametredir. Komutu, SharePoint Araçlar uzantısından veri iletmek gerekiyorsa, bu parametre, SharePoint komutu için ekleyebilirsiniz.  
  
    -   Dönüş değerine sahip olabilir, ancak bu özellik isteğe bağlıdır.  
  
    -   İkinci parametre ve dönüş değeri, Windows Communication Foundation (WCF) tarafından seri hale getirilebilir bir tür olmalıdır. Daha fazla bilgi için [veri sözleşme seri hale getirici tarafından desteklenen türleri](/dotnet/framework/wcf/feature-details/types-supported-by-the-data-contract-serializer) ve [XmlSerializer sınıfını kullanarak](/dotnet/framework/wcf/feature-details/using-the-xmlserializer-class).  
  
    -   Yöntem herhangi bir görünürlük sağlayabilirsiniz (**genel**, **iç**, veya **özel**), ve statik veya statik olmayan olabilir.  
  
4.  Uygulama <xref:Microsoft.VisualStudio.SharePoint.Commands.SharePointCommandAttribute> yöntemi. Bu öznitelik komutu için benzersiz bir tanımlayıcı belirtir. Bu tanımlayıcı, yöntem adıyla eşleşecek şekilde yok.  
  
     Komutu, SharePoint Araçlar uzantısından çağırdığınızda aynı benzersiz tanımlayıcıya belirtmeniz gerekir. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint komutu yürütme](../sharepoint/how-to-execute-a-sharepoint-command.md).  
  
## <a name="example"></a>Örnek  
 Tanımlayıcı olan SharePoint komutu aşağıdaki kod örneği gösterir `Contoso.Commands.UpgradeSolution`. Bu komut, dağıtılan bir çözümüne yükseltmek sunucusu nesne modelinde API'lerini kullanır.  
  
 [!code-csharp[SPExtensibility.ProjectExtension.UpgradeDeploymentStep#5](../sharepoint/codesnippet/CSharp/UpgradeDeploymentStep/SharePointCommands/Commands.cs#5)]
 [!code-vb[SPExtensibility.ProjectExtension.UpgradeDeploymentStep#5](../sharepoint/codesnippet/VisualBasic/upgradedeploymentstep/sharepointcommands/commands.vb#5)]  
  
 Örtük ilk yanı sıra <xref:Microsoft.VisualStudio.SharePoint.Commands.ISharePointCommandContext> parametresi bu komut ayrıca SharePoint sitesine yükseltiliyor .wsp dosyasının tam yolunu içeren özel bir dize parametresi vardır. Daha büyük bir örneğin bağlamında bu kodu görmek için bkz: [izlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturmak](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md).  
  
## <a name="compiling-the-code"></a>Kod derleme  
 Bu örnek aşağıdaki derlemelere başvurular gerektirir:  
  
-   Microsoft.VisualStudio.SharePoint.Commands  
  
-   Microsoft.SharePoint  
  
## <a name="deploying-the-command"></a>Komut dağıtma  
 Komut dağıtmak için komut derlemeyi aynı dahil etmek [!include[vsprvs](../sharepoint/includes/vsprvs-md.md)] uzantısı (*VSIX*) komut uzantısı derlemeyle paket. Ayrıca extension.vsixmanifest dosyasındaki komut derleme için bir girdi eklemeniz gerekir. Daha fazla bilgi için [Visual Studio'da SharePoint araçları için uzantıları dağıtma](../sharepoint/deploying-extensions-for-the-sharepoint-tools-in-visual-studio.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint nesne modellerini çağırma](../sharepoint/calling-into-the-sharepoint-object-models.md)   
 [Nasıl yapılır: Bir SharePoint komutu yürütme](../sharepoint/how-to-execute-a-sharepoint-command.md)   
 [İzlenecek yol: Sunucu Gezgini, web bölümlerini görüntülemek üzere genişletme](../sharepoint/walkthrough-extending-server-explorer-to-display-web-parts.md)  
