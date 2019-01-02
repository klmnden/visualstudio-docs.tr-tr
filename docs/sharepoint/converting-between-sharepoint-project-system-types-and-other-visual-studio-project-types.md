---
title: SharePoint Proje sistem türleri ve diğer Visual Studio Proje türleri arasında dönüştürme | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint project service
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 145f080812356a4387401ef47adbd48fe783e60b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53920624"
---
# <a name="convert-between-sharepoint-project-system-types-and-other-visual-studio-project-types"></a>SharePoint Proje sistem türleri ve diğer Visual Studio Proje türleri arasında dönüştürme
  Bazı durumlarda SharePoint Proje sistemi bir nesne olabilir ve Visual Studio Otomasyon nesne modeli veya tümleştirme nesne modeli, karşılık gelen nesne özelliklerini kullanmak istediğiniz ya da tam tersi. Bu durumlarda, kullandığınız <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService.Convert%2A> farklı nesne modeline nesneyi dönüştürmek için SharePoint Proje hizmeti yöntemi.

 Örneğin, sahip olabileceğiniz bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> nesne, ancak yalnızca mevcut yöntemleri kullanmak istediğiniz bir <xref:EnvDTE.Project> veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject> nesne. Bu durumda, kullanabileceğiniz <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService.Convert%2A> yöntemini <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> için bir <xref:EnvDTE.Project> veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject>.

 Visual Studio Otomasyon nesne modeli ve Visual Studio tümleştirmesi nesne modeli hakkında daha fazla bilgi için bkz. [SharePoint programlama modeline genel bakış araçları uzantıları](../sharepoint/overview-of-the-programming-model-of-sharepoint-tools-extensions.md).

## <a name="types-of-conversions"></a>Türleri dönüştürme
 Aşağıdaki tabloda, bu yöntem, SharePoint Proje sistemi ve diğer Visual Studio nesne modelleri arasında dönüştürme yapabilirsiniz türlerini listeler.

|SharePoint Proje sistem türü|Otomasyon ve tümleştirme nesne modellerini karşılık gelen türler|
|------------------------------------|-------------------------------------------------------------------------|
|<xref:Microsoft.VisualStudio.SharePoint.ISharePointProject>|<xref:EnvDTE.Project><br /><br /> veya<br /><br /> Proje için temel alınan COM nesnesi tarafından uygulanır Visual Studio tümleştirmesi nesne modelinde herhangi arabirimi. Bu arabirimler dahil <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy>, <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject> (veya türetilmiş bir arabirim) ve <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage>. Projeleri tarafından uygulanan arabirimler ana listesi için bkz. [proje modeli çekirdek bileşenleri](../extensibility/internals/project-model-core-components.md).|
|<xref:Microsoft.VisualStudio.SharePoint.IMappedFolder><br /><br /> <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItem><br /><br /> <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectItemFile><br /><br /> <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectFeature><br /><br /> <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectFeatureResourceFile><br /><br /> <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectPackage>|<xref:EnvDTE.ProjectItem><br /><br /> veya<br /><br /> A<xref:System.UInt32> proje üye tanımlayan (bir VSITEMID olarak da bilinir) değer <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> , içerir. Bu değer geçirilebilir *ItemId* bazı parametre <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> yöntemleri.|

## <a name="example"></a>Örnek
 Aşağıdaki kod örneğinde nasıl kullanılacağını gösterir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService.Convert%2A> dönüştürmek için yöntemi bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProject> nesnesini bir <xref:EnvDTE.Project>.

 [!code-csharp[SPExtensibility.ProjectService.FromDTE#2](../sharepoint/codesnippet/CSharp/spprojectserviceaddin/connect.cs#2)]
 [!code-vb[SPExtensibility.ProjectService.FromDTE#2](../sharepoint/codesnippet/VisualBasic/spprojectserviceaddin/connect.vb#2)]

 Bu örnek gerektirir:

-   SharePoint Proje sisteminin bir başvuru içeren bir uzantı *EnvDTE.dll* derleme. Daha fazla bilgi için [SharePoint Proje sistemini genişletmek](../sharepoint/extending-the-sharepoint-project-system.md).

-   Kaydeden kod `projectService_ProjectAdded` işlemek için gereken yöntemini <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectEvents.ProjectAdded> olayı bir <xref:Microsoft.VisualStudio.SharePoint.ISharePointProjectService> nesne. Bir örnek için bkz [nasıl yapılır: Bir SharePoint proje uzantısı oluşturma](../sharepoint/how-to-create-a-sharepoint-project-extension.md).

## <a name="see-also"></a>Ayrıca bkz.

- [SharePoint Proje hizmetini kullanın](../sharepoint/using-the-sharepoint-project-service.md)
- [Nasıl yapılır: SharePoint Proje hizmetini alma](../sharepoint/how-to-retrieve-the-sharepoint-project-service.md)
- [Araç uzantılarının programlama modeline SharePoint genel bakış](../sharepoint/overview-of-the-programming-model-of-sharepoint-tools-extensions.md)
