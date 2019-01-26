---
title: Özellikleri ve yöntemleri genişletilmiş proje alt türleri tarafından | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- project subtypes, extended methods
- project subtypes, extended properties
ms.assetid: 2b9833bf-8551-4ae1-93db-197ba645c65e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7ba57cb5ff2bdeb4c1d6038704642b41d3b9d7a9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55012917"
---
# <a name="properties-and-methods-extended-by-project-subtypes"></a>Proje Alt Türleri Tarafından Genişletilen Özellikler ve Metotlar
Proje alt çok temel bir projenin bir Toplayıcı oluşturulduğu için projenin davranışını etkilemek için güç sahiptir. Bu bölümde bazı gelişmiş veya proje alt türleri tarafından değiştirilen özellikler özetlenmektedir.  
  
## <a name="features-gained-by-aggregation"></a>Toplama tarafından elde edilen Özellikler  
 Aşağıdaki tabloda birçok temel projelerinde geçersiz kılmak proje alt türleri toplama sağlayan yöntemler özetlenmiştir.  
  
|Toplama tarafından geçersiz kılınan yöntemleri|Proje alt türü|  
|---------------------------------------|---------------------|  
|Gelen <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy>:<br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetProperty%2A><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.SetProperty%2A><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.GetGuidProperty%2A><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy.SetGuidProperty%2A>|Proje alt türü için etkinleştirir.<br /><br /> -Açıklamalı alt yazı ve proje düğümünün simgesi değiştirin.<br />-Tamamen proje geçersiz kılma `Browse` nesne.<br />-Proje adlandırılabilir olup olmadığını denetler.<br />-Denetim sıralama düzeni.<br />-Kullanıcı bağlamı devingen Yardım denetimi.|  
|Gelen <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject>:<br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsProject.GetItemContext%2A>|Bağlamsal hangi hizmetlerin tasarımcılar ve düzenleyiciler için sağlanan denetlemek bir proje alt sağlar.|  
|Gelen <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>:<br /><br /> <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.QueryStatus%2A><br /><br /> <xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget.Exec%2A><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.QueryStatusCommand%2A><br /><br /> <xref:Microsoft.VisualStudio.Shell.Interop.IVsUIHierarchy.ExecCommand%2A>|Proje alt türü için etkinleştirir.<br /><br /> -Komut yönlendirme proje komutları için de katılın.<br />-Eklemek, kaldırmak veya hem proje ortam komutları hem de etkin Çözüm Gezgini komutları devre dışı bırakın.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsFilterAddProjectItemDlg2>|Proje alt ne de kullanıcının gördüğü filtrelemek olanak tanır **Yeni Öğe Ekle** iletişim kutusu.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsSingleFileGeneratorFactory>|Proje alt türü için etkinleştirir.<br /><br /> -Bir dosya uzantısı verilen varsayılan oluşturucu belirleyin.<br />-Bir COM nesnesi için bir insan tarafından okunabilir oluşturucu adı eşleyin.|  
  
## <a name="properties-used-by-project-subtypes"></a>Proje alt türleri tarafından kullanılan özellikleri  
 Ortamı ve temel proje sistemi özelliklerinden kullanabilirsiniz <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID> ve <xref:Microsoft.VisualStudio.Shell.Interop.__VSSPROPID2> proje sisteminin çeşitli özellikleri denetlemek bir proje alt etkinleştirmek için aşağıdaki tabloda ayrıntılı olarak listeleme.  
  
|VSHPROPID özelliği|Proje alt türü|  
|------------------------|---------------------|  
|`AddItemTemplatesGuid`|İçeriğini denetlemek bir proje alt sağlayan **Öğe Ekle** iletişim kutusu. Proje alt şablon dizinlerin yeni bir belirtim sağlar, yeni öğe türlerini eklemek, var olan öğeleri kaldırmak ve temel proje öğeleri kümesini reorganıze **Öğe Ekle** iletişim kutusu.|  
|`PropertyPagesCLSIDList`|Ekleme veya kaldırma yapılandırma bağımsız özellik sayfaları bir proje alt sağlar.|  
|`CfgPropertyPagesCLSIDList`|Ekleme veya kaldırma yapılandırma bağımlı özellik sayfaları bir proje alt sağlar.|  
|`ExtObjectCATID`|Otomasyon Genişleticisi proje veya proje öğesi nesneleri genişletici catID öğrenerek sağlamak bir proje alt sağlar. Örneğin, bir proje alt türü özel bir sağlayabilir `Project.Extender("<subtype>")` nesne.|  
|`BrowseObjectCATID`|Otomasyon Genişleticisi için sağlamak bir proje alt sağlayan `Browse` genişletici catID bilerek nesne. Örneğin, bir proje alt türü için ek özellikler ekleyebilirsiniz <xref:EnvDTE.Project.Properties%2A> koleksiyonu.|  
|`CfgBrowseObjectCATID`|Otomasyon Genişleticisi için proje yapılandırma Gözat nesnesi sağlamak bir proje alt sağlar. Örneğin, bir proje alt türü için ek özellikler ekleyebilirsiniz <xref:EnvDTE.Configuration.Properties%2A> koleksiyonu.|  
|`CfgExtObjectCATID`|Otomasyon Genişleticisi için yapılandırma nesnesi sağlamak bir proje alt sağlar.|  
|`DefaultPlatformName`|Projenin yapılandırma nesnelerini platform adını belirlemek bir proje alt sağlar.|  
  
 Temel projenin yukarıdaki özelliklerinin varsayılan uygulamasını sağlar. Temel projenin bu çağırarak alır `QueryInterface` için <xref:Microsoft.VisualStudio.Shell.Interop.IVsHierarchy> böylece izin vererek uygulama özellikleri geçersiz kılmak proje alt en dıştaki proje alt türü.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje Alt Türleri Tasarımı](../../extensibility/internals/project-subtypes-design.md)