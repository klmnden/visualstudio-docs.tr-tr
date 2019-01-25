---
title: SharePoint için site tanımları oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, site definitions
- site definitions [SharePoint development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 3b2709426cca892e60d864fa62695b2eef8c776b
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54874048"
---
# <a name="create-site-definitions-for-sharepoint"></a>SharePoint için site tanımları oluşturma
  SharePoint Site tanımı projesi içinde [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] oluşturmanızı sağlar bir *site tanım*, yeni bir SharePoint sitesi için bir temel olarak görev gören. Bu tanımları yalnızca görünümünü ve davranışını SharePoint sitesi, ancak aynı zamanda varsayılan içeriğini ve işlevleri belirler. Tanımında önceden yapılandırılmış listeler, içerik türleri, Olay alıcıları, görüntüleri ve diğer öğeleri koyabilirsiniz. Örneğin, SharePoint, BLOG gibi bazı site tanımları içerir. BLOG site tanımını temel alan bir site oluşturduğunuzda, site, listeler, Web Bölümleri ve bir blog sitesi gerektiren diğer öğeleri içerir.  
  
 Site tanımları hakkında daha fazla bilgi için bkz: [Site şablonları ve tanımları](http://go.microsoft.com/fwlink/?LinkId=179134).  
  
## <a name="site-definition-projects"></a>Site tanımı projeleri
 Site tanımı projeleri [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] bir SharePoint sitesi gereken temel dosyaları sağlar; herhangi bir varsayılan işlevsellik sağlamaz. Dosyaları ve istediğiniz işlevleri sağlamak için içeriği eklemeniz gerekir. Oluşturma ve ihtiyaç duyduğunuz dosyaları ekleyerek, siteyi el ile oluşturabilirsiniz.  
  
## <a name="feature-stapling"></a>Özellik Zımbalama
 Site tanımları oluşturma yararlarından biri [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] otomatik olarak kullandıkları olan *özellik Zımbalama*. Özellik Zımbalama işlevselliği ekleme site tanımını kendisi yerine bir site tanımı bir özellik ekler. Bunun yapılması, özgün site tanımı değiştirmeden site tanımı kullanılarak oluşturulan herhangi bir siteye özelliği eklemenizi sağlar. Daha fazla bilgi için [özellik Zımbalama](http://go.microsoft.com/fwlink/?LinkID=119283).  
  
## <a name="site-definition-project-components"></a>Site tanımı proje bileşenleri
 Site tanımı çözümü oluşturduğunuzda, aşağıdaki varsayılan dosyaları eklenir, **SiteDefinition** düğümü.  
  
|Dosya Adı|Açıklama|  
|---------------|-----------------|  
|*default.aspx*|Varsayılan ASPX giriş sayfasına yeni bir SharePoint sitesi için.|  
|*Onet.XML*|Yeni sitenin yapılandırmasını, bileşenleri site tanımı şablonu ve varsayılan davranışını belirtir. Bu ayarlar, öznitelikler, etkinleştirilmiş içerik türleri gibi varsayılan liste görünümleri belge şablonu dosyaları içerir ve Web Bölümleri siteyle dahil. Varsayılan olarak, `Modules` bölümü SharePoint sitesine ve nasıl yapılandırılacağını eklenecek dosyaları listeler.|  
|*webtemp_\<SiteDefinitionName>.xml*|Görünür site tanımı yapılandırmaları belirtir **Şablon Seçimi** bölümünü **yeni SharePoint sitesi** sayfası.|  
  
 Varsayılan olarak, tüm site tanımları depolanan  *\<sürücü: > \Program Files\Microsoft Shared\Web Server Extensions\14\TEMPLATE\SiteTemplates* klasör. Her bir site tanımı kendi alt vardır.  
  
## <a name="related-topics"></a>İlgili konular
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[İzlenecek yol: Temel bir Site tanımı projesi oluşturma](../sharepoint/walkthrough-create-a-basic-site-definition-project.md)|Temel bir site tanımı projesi oluşturmak adım adım müşteri adayları [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)].|  
|[Nasıl yapılır: Bir özel Site tanımı oluşturup yapılandırma](http://go.microsoft.com/fwlink/?LinkId=183309)|Mevcut bir site tanımı kopyalama ve sonra kopyayı değiştirerek bir özel site tanımı SharePoint'te oluşturmayı açıklar.|  
|[*WebTemp.xml*](http://go.microsoft.com/fwlink/?LinkId=183310)|Kullanılabilir site tanımları belirten özgün dosyayı açıklayan **Şablon Seçimi** bölümünü **yeni SharePoint sitesi** sayfası.|  
|[SharePoint Çözümlerini Yerelleştirme](../sharepoint/localizing-sharepoint-solutions.md)|Genel kullanım için SharePoint çözümlerinizi hazırlanma işlemi açıklanmaktadır.|  
|[SharePoint için Web bölümleri oluşturma](../sharepoint/creating-web-parts-for-sharepoint.md)|Kullanıcıların değiştirebileceği bir SharePoint sayfasına bölümlerini nasıl oluşturacağınızı açıklar.|  
|[Web bölümleri veya uygulama sayfaları için yeniden kullanılabilir denetimler oluşturma](../sharepoint/creating-reusable-controls-for-web-parts-or-application-pages.md)|Uygulama sayfaları ve Web Bölümleri'ni çalıştırın, yeniden kullanılabilir denetimleri nasıl oluşturacağınızı açıklar.|  
|[Visual Web Developer](http://go.microsoft.com/fwlink/?LinkId=178725)|Projenizde bir Web sayfası açtığınızda görünen tasarımcıyı nasıl kullanacağınızı açıklar.|  
|[ASP.NET Web sayfaları genel bakış](http://go.microsoft.com/fwlink/?LinkId=178726)|Yapısı hakkında genel bilgiler sağlar [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] Web sayfaları, sayfa tarafından nasıl işlendiğini [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)], nasıl ve ne [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] sayfaları, XHTML standartları ile uyumlu biçimlendirme görüntüler.|  
|[ASP.NET Web sayfası sözdizimi](http://go.microsoft.com/fwlink/?LinkId=178727)|Bir ASP.NET sayfasını oluştururlar işaretleme öğeleri açıklar.|  
|[ASP.NET Web sayfaları programlama](http://go.microsoft.com/fwlink/?LinkId=178728)|Olay işleyicileri oluşturma hakkında bilgi sağlar [!INCLUDE[vstecasp](../sharepoint/includes/vstecasp-md.md)] sayfaları ve istemci komut dosyası ile çalışmayı öğrenin.|  
|[Windows SharePoint Services programlama](http://go.microsoft.com/fwlink/?LinkId=178729)|Sağlanan yönetilen nesne modelinin nasıl kullanılacağını açıklar [!INCLUDE[sharepointShort](../sharepoint/includes/sharepointshort-md.md)].|  
  
## <a name="see-also"></a>Ayrıca bkz.
 [SharePoint çözümleri geliştirme](../sharepoint/developing-sharepoint-solutions.md)  
