---
title: SharePoint paketleme ve dağıtımını genişletme | Microsoft Docs
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
ms.openlocfilehash: 87e6f4663a73b1c3f7bfe203833ed62c686298bc
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867773"
---
# <a name="extend-sharepoint-packaging-and-deployment"></a>SharePoint paketleme ve dağıtımını genişletme
  Paketleme ve dağıtım işlemi SharePoint projeleri için genişletebilirsiniz.
  
## <a name="create-deployment-steps"></a>Dağıtım adımı oluşturma
 Bir SharePoint projesi dağıttığınızda [!INCLUDE[vs_current_short](../sharepoint/includes/vs-current-short-md.md)] bir dizi dağıtım adımı yürütür. Visual Studio Geri Çekiliyor ve çözümleri ekleme gibi birçok görevi için yerleşik dağıtım adımlarını içerir. Ancak, kendi dağıtım adımları da oluşturabilirsiniz.  
  
 Bir dağıtım adımı oluşturmak nasıl gösteren bir kılavuz için bkz. [izlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturmak](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md).  
  
## <a name="create-deployment-configurations"></a>Dağıtım yapılandırmaları oluşturma
 Bir dağıtım yapılandırması için belirli bir projenin yürütülür, ancak tüm SharePoint Proje öğeleri etkileyebilecek dağıtım adımları kümesidir. Her dağıtım yapılandırmasının Proje dağıtıldığında çalıştırılan adım kümesi ve projeyi geri çekilebilir çalıştırılan başka bir kümesi içerir. [!INCLUDE[vs_current_short](../sharepoint/includes/vs-current-short-md.md)] iki yerleşik dağıtım yapılandırmaları içerir ancak aynı zamanda kendi oluşturabilirsiniz. Bir dağıtım yapılandırması oluşturduğunuzda, yerleşik dağıtım adımları ve oluşturduğunuz dağıtım adımları ekleyebilirsiniz.  
  
 Dağıtım yapılandırmasının nasıl oluşturulacağını gösteren bir kılavuz için bkz. [izlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturmak](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md).  
  
## <a name="run-code-when-a-sharepoint-solution-is-deployed-or-retracted"></a>Bir SharePoint çözümünü dağıtılan ya da geri çekilebilir kodu çalıştırın.
 Bir SharePoint çözümünü dağıtılan ya da geri çekilebilir ek görevleri gerçekleştirmek için olayları işleyebilir. Visual Studio aşağıdaki senaryolarda işleyebileceği olayları oluşturur:  
  
-   Önce ve sonra her bir dağıtım adımı için bir SharePoint proje öğesi yürütülür. Daha fazla bilgi için [nasıl yapılır: Dağıtım adımları yürütüldüğünde kodu çalıştırma](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md).  
  
-   Önce ve sonra bir SharePoint Proje dağıtılan veya geri çekilebilir. Daha fazla bilgi için [nasıl yapılır: Bir SharePoint Proje dağıtılan ya da geri çekilebilir kodu çalıştırmak](../sharepoint/how-to-run-code-when-a-sharepoint-project-is-deployed-or-retracted.md).  
  
## <a name="handle-deployment-conflicts"></a>Dağıtım çakışmalarını işleme
 SharePoint Proje öğeleri, modüller, Web bölümleri, liste örnekleri ve içerik türleri dahil olmak üzere bazı türler, yerleşik dağıtım çakışması çözümü sağlar. Bu proje öğelerinden birini içeren bir çözümü dağıttığınızda, Visual Studio ilk kez bir dosya zaten aynı adı, URL'si veya kimliği olan SharePoint sitesindeki dağıtmakta olduğunuz öğesinde bir dosya olarak mevcut olup olmadığını denetler. Bir çakışma varsa, Visual Studio otomatik olarak çakışmayı çözebildiğinde veya Visual Studio çakışmayı veya dağıtımı iptal olmasını isteyip istemediğinizi belirlemek için isteyebilir. Daha fazla bilgi için [sorun giderme SharePoint paketleme ve dağıtım](../sharepoint/troubleshooting-sharepoint-packaging-and-deployment.md).  
  
 Bu özellik olup olmadığını denetleyen ve dağıtım çakışmaları çözer kendi kodunuzu sağlayarak genişletebilirsiniz. Daha fazla bilgi için [nasıl yapılır: Dağıtım çakışmalarını işleme](../sharepoint/how-to-handle-deployment-conflicts.md).  
  
## <a name="run-command-line-operations-before-or-after-a-project-is-deployed"></a>Önce veya bir proje dağıtıldıktan sonra komut satırı işlemlerini çalıştırın
 Bir SharePoint çözümünü dağıttığınızda, bir komut satırı işlemi çalıştırmak istiyorsanız, ayarlayabileceğiniz <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject.PreDeploymentCommand%2A> ve <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject.PostDeploymentCommand%2A> özelliklerini bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> nesne. Visual Studio, önce ve proje dağıtıldıktan sonra bu komutları yürütür.  
  
 Bazı durumlarda, dağıtım çakışmalarını görebilirsiniz. Çakışmaları çözümlemek için çeşitli yollar vardır. Daha fazla bilgi için [sorun giderme SharePoint paketleme ve dağıtım](../sharepoint/troubleshooting-sharepoint-packaging-and-deployment.md).  
  
## <a name="customize-validation-rules"></a>Doğrulama kurallarını özelleştirme
 Çözüm paketine (.wsp) dağıtmadan önce özel özellik ve paket doğrulama kuralları özellik veya paket geçerli olduğunu doğrulamak için oluşturabilirsiniz. Örneğin, doğrulama sorunları gidermeye yardımcı olmak için geliştiriciler için bilgi, uyarı veya hatalar bildirebilir. Daha fazla bilgi için [nasıl yapılır: Özel özellik ve paket doğrulama kuralları için SharePoint çözümleri oluşturma](../sharepoint/how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions.md).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [Nasıl yapılır: Dağıtım adımları yürütüldüğünde kodu çalıştırma](../sharepoint/how-to-run-code-when-deployment-steps-are-executed.md)   
 [İzlenecek yol: SharePoint projeleri için bir özel dağıtım adımı oluşturma](../sharepoint/walkthrough-creating-a-custom-deployment-step-for-sharepoint-projects.md)   
 [Nasıl yapılır: Özel özellik ve paket doğrulama kuralları için SharePoint çözümleri oluşturma](../sharepoint/how-to-create-custom-feature-and-package-validation-rules-for-sharepoint-solutions.md)   
 [SharePoint Proje sistemini genişletme](../sharepoint/extending-the-sharepoint-project-system.md)  
