---
title: SharePoint için uygulama sayfaları oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, Web pages
- SharePoint development in Visual Studio, content pages
- SharePoint development in Visual Studio, application pages
- application pages [SharePoint development in Visual Studio], developing
- application pages [SharePoint development in Visual Studio], creating
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 815d48d7e7874ea5bd34d840ceecadcc4edb8dda
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54865079"
---
# <a name="create-application-pages-for-sharepoint"></a>SharePoint için uygulama sayfaları oluşturma
  Bir *uygulama sayfası* bir SharePoint Web sitesinde kullanılmak üzere tasarlanmış bir ASP.NET Web sayfası. Uygulama sayfaları, ASP.NET sayfasının özelleştirilmiş bir türüdür. Uygulama sayfası ve standart bir ASP.NET sayfası arasındaki birincil fark bir uygulama sayfasını SharePoint ana sayfası ile birleştirilmiş içerik içermesidir. Ana sayfa görünümünü ve davranışını sitesindeki diğer sayfalara paylaşım uygulama sayfaları sağlar.  
  
 Visual Studio, Tasarımcı kullanarak uygulama sayfaları tasarlamanıza olanak tanır. Tasarımcı, bir ana sayfasında tanımlanan her içerik yer tutucusu için bir içerik alanı görüntüler. Uygulama sayfası, bu alanlara denetimleri sürükleyerek tasarlayabilirsiniz.  
  
## <a name="application-pages"></a>Uygulama sayfaları
 Bir site sayfasını bir siteye özgüdür ancak uygulama sayfaları sunucusundaki tüm siteler arasında paylaşılır. Daha fazla bilgi için [SharePoint sayfası türleri](http://go.microsoft.com/fwlink/?LinkID=211584).  
  
 Varsayılan olarak, site sayfaları, bir SharePoint sitesi oluştururken sayfaları çoğu. Bir SharePoint sayfası kitaplığı için bir site sayfasını eklenebilir. Kullanıcılar, SharePoint Tasarımcısı gibi araçları kullanarak bir site sayfasını özelleştirebilirsiniz. Bir site sayfasını, dinamik Web Bölümleri ve Web Bölümü bölgeleri gibi özellikleri de barındırabilir.  
  
 Uygulama sayfaları, bu işlemleri yapamazsınız. Ancak bir uygulama sayfası özel kodu içermesi için sayfayı istiyorsanız oluşturmak için sayfanın en iyi türüdür. Bir site sayfası için özel kod ekleyebilirsiniz, ancak kodu çalıştıran kullanıcının SharePoint Tasarımcısı gibi araçları kullanarak sayfa özelleştirir durdurur.  
  
> [!NOTE]  
>  Visual Studio sağlamaz yardımcı şablonları, bir SharePoint sitesi için site sayfaları oluşturun. Daha fazla bilgi için [SharePoint sayfası türleri](http://go.microsoft.com/fwlink/?LinkID=211584).  
  
## <a name="create-an-application-page"></a>Uygulama sayfası oluşturma
 Uygulama sayfası oluşturmak için bir **uygulama sayfası** bir SharePoint proje öğesi. Uygulama sayfası oluşturduğunuzda, Visual Studio projenize aşağıdaki klasörleri ekler:  
  
|Klasör|Açıklama|  
|------------|-----------------|  
|Düzenler|SharePoint dosya sistemin _layouts sanal dizin eşlenir.|  
|Düzenleri alt|Uygulama sayfası dosyaları içerir. Varsayılan olarak, bu klasör projeniz gibi aynı ada sahip. Bu klasör herhangi bir zamanda yeniden adlandırabilirsiniz. Projeyi çalıştırdığınızda, Visual Studio bu klasör SharePoint dosya sistemin _layouts sanal dizine dağıtır.|  
  
 Visual Studio aşağıdaki dosyaları projenize ekler:  
  
|Dosya|Açıklama|  
|----------|-----------------|  
|ASP.NET sayfası dosyası (*.aspx*)|Sayfayı tanımlayan XML biçimlendirme içeriyor.|  
|Uygulama sayfası kod dosyası|Uygulama sayfası arka plan kod içerir. Bu dosya için olayları işleyen kodu ekleyin.|  
|Uygulama sayfası kod Tasarımcı dosyası|Tasarımcı tarafından oluşturulan kodu içerir. Doğrudan bu dosya düzenlemeyin.|  
  
## <a name="design-and-debug-an-application-page"></a>Tasarım ve uygulama sayfası hata ayıklama
 Visual Studio'da Tasarımcı görünümü kullanarak bir uygulama sayfası içeriğini tasarlayın. Bu tasarımcı projenizde uygulama sayfasını açtığınızda görüntülenen (çift tıklayarak veya kısayol menüsünü açarak ve ardından **açın**) ve ardından **tasarım** kısmındaki düğmesi Düzenleyici.  
  
> [!NOTE]  
>  Sayfa tasarlayabilirsiniz yalnızca **kaynak** Tasarımcı görünümü. **Tasarım** uygulama sayfaları için tasarımcı görünümünü devre dışı.  
  
 Diğer SharePoint Proje öğeleri Visual Studio'da hata ayıklama gibi bir uygulama sayfası ayıklayabilirsiniz. Visual Studio hata ayıklayıcısını başlattığınızda, Visual Studio SharePoint sitesi açılır.  
  
 Uygulama sayfasını görüntülemek için el ile uygulama sayfasının konumuna gidin gerekir (örneğin: http://<em>sunucu_adı</em>/_layouts/*Project_Name*/ApplicationPage1.aspx).  
  
 SharePoint projelerinde hata ayıklama hakkında daha fazla bilgi için bkz: [sorun giderme SharePoint çözümleri](../sharepoint/troubleshooting-sharepoint-solutions.md).  
  
## <a name="choose-a-master-page"></a>Bir ana sayfa seçin
 Varsayılan olarak, bir **uygulama sayfası** başvuran projenizin hata ayıklamak için kullanmakta olduğunuz sitenin ana sayfasını öğesi. Sayfa v4.master adlı ve listede bulabilirsiniz **Ana Sayfa Galerisi** SharePoint sitesi.  
  
 Hangi ana sayfa ayarlayarak uygulama sayfa tarafından kullanılan açıkça değiştirebilirsiniz `MasterPageFile` özniteliği uygulamanın `Page` öğesi. (Örneğin: `MasterPageFile="~/_layouts/applicationv4.master"`). Aslında, dinamik ana sayfalar SharePoint sunucusu üzerinde etkin değilse, bu öznitelik ayarlamanız gerekir. SharePoint ana sayfaları hakkında daha fazla bilgi için bkz. [ana sayfalar](http://go.microsoft.com/fwlink/?LinkID=169281).  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint Foundation geliştirme derinlemesine](http://go.microsoft.com/fwlink/?LinkID=182103)   
 [ASP.NET genel bakış](/aspnet/overview)   
 [ASP.NET Web Sayfaları](/aspnet/web-pages/index)   
