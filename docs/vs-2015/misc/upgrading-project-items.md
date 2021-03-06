---
title: Proje öğeleri yükseltme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: devlang-csharp
ms.topic: conceptual
helpviewer_keywords:
- upgrading project items
- projects [Visual Studio SDK], upgrading items
- project items [Visual Studio], upgrading
ms.assetid: 8af29dd4-eaf1-4b3c-b602-198e1a3dff23
caps.latest.revision: 14
manager: jillfra
ms.openlocfilehash: eb3619e187c7856cf03ee60c8a04cbe527bf0a69
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65698691"
---
# <a name="upgrading-project-items"></a>Proje öğeleri yükseltme
Ekler veya öğeleri uygulamaz proje sistemleri içinde yönetmek, proje yükseltme işlemine katılmasını gerekebilir. Crystal Reports, proje sistemi için eklenebilir bir öğenin bir örnektir.  
  
 Genellikle, proje öğesi uygulayıcılar hangi proje başvuruları ve diğer proje özellikleri var. bir yükseltme kararı vermeniz nelerdir bilmesi gerektiğinden proje zaten tam olarak oluşturulmuş ve yükseltilen yararlanmak isteyen.  
  
### <a name="to-get-the-project-upgrade-notification"></a>Proje yükseltme bildirim almak için  
  
1. Ayarlama <xref:Microsoft.VisualStudio.Shell.Interop.UIContextGuids80.SolutionOrProjectUpgrading> proje öğesi uygulamanızda bayrağı (vsshell80.idl içinde tanımlanmıştır). Bu proje öğenizin otomatik olarak VSPackage'ı neden olduğunda yük [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] kabuğu, proje sistemi yükseltme sürecinde olduğunu belirler.  
  
2. Öneri <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEventsProjectUpgrade> aracılığıyla arabirim <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolution2.AdviseSolutionEvents%2A> yöntemi.  
  
3. <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEventsProjectUpgrade> Arabirimi, proje sistemi uygulama yükseltme işlemlerini tamamladı ve yeni yükseltilen proje oluşturulduktan sonra tetiklenir. Senaryoya bağlı olarak <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEventsProjectUpgrade> arabirimi sonra tetiklenir <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterOpenSolution%2A>, <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterOpenProject%2A>, veya <xref:Microsoft.VisualStudio.Shell.Interop.IVsSolutionEvents3.OnAfterLoadProject%2A> yöntemleri.  
  
### <a name="to-upgrade-the-project-item-files"></a>Proje öğesi dosyaları yükseltmek için  
  
1. Proje öğesi uygulamanızda dosya yedekleme işlemi dikkatle yönetmeniz gerekir. Yan yana yedeklemesi için bu özellikle geçerlidir burada `fUpgradeFlag` parametresinin <xref:Microsoft.VisualStudio.Shell.Interop.IVsProjectUpgradeViaFactory.UpgradeProject%2A> yöntemi ayarlandığında <xref:Microsoft.VisualStudio.Shell.Interop.__VSPPROJECTUPGRADEVIAFACTORYFLAGS>, "eski" belirlenmiş dosyalarını boyunca yedeklenmiş dosyaları yerleştirildiği. Proje zaman yükseltildi sistem saatinden daha önce Yedeklenen dosyaların eski belirlenebilir. Ayrıca, bunu önlemek için belirli adımlar sürece, yazılabilir.  
  
2. Zaman, proje öğesi proje yükseltme bir bildirim alır. **Visual Studio Dönüştürme Sihirbazı** gösterilmeye devam eder. Bu nedenle, yöntemlerini kullanmanız gerekir <xref:Microsoft.VisualStudio.Shell.Interop.IVsUpgradeLogger> arabirimi yükseltme iletileri Sihirbazı kullanıcı Arabirimi sağlar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Visual Studio Dönüştürme Sihirbazı](https://msdn.microsoft.com/4acfd30e-c192-4184-a86f-2da5e4c3d83c)   
 [Özel projelerini yükseltme](../misc/upgrading-custom-projects.md)