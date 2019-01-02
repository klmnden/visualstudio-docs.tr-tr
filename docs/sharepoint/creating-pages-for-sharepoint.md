---
title: SharePoint için sayfa oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- SharePoint development in Visual Studio, master pages
- SharePoint development in Visual Studio, page layouts
- SharePoint development in Visual Studio, content pages
- master pages[SharePoint development in Visual Studio], designing
- content pages[SharePoint development in Visual Studio], designing
- page layouts[SharePoint development in Visual Studio], designing
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 71f0a75678c0123853f128f42bfdbf1c75ac0c74
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53859821"
---
# <a name="create-pages-for-sharepoint"></a>SharePoint için sayfa oluşturma
  Uygulama sayfaları, site sayfaları, ana sayfalar ve sayfa düzenleri için bir SharePoint sitesi oluşturabilirsiniz.  
  
 Visual Studio'da bir şablon kullanarak uygulama sayfaları oluşturabilirsiniz. SharePoint Designer'ı kullanarak site sayfaları, ana sayfalar ve sayfa düzenleri oluşturun. Ardından, bunları bir SharePoint projesinde kullanmak için Visual Studio'yla bu sayfaları içeri aktarabilirsiniz.  
  
 Görünümünü ve davranışını sayfaların geçişli stil sayfaları, ECMAScript ve Temalar aracılığıyla da değiştirebilirsiniz.  
  
## <a name="types-of-sharepoint-pages"></a>SharePoint sayfaları türleri
 Aşağıdaki tabloda dört ana türlerini içeren bir SharePoint sitesi sayfalarının tanımlar.  
  
|Sayfa türü|Açıklama|  
|---------------|-----------------|  
|Uygulama sayfaları|Özel kod içeren sayfasında istediğiniz veya birden çok sitede paylaşılacak sayfa istiyorsanız bir uygulama sayfası oluşturun. Aksi takdirde, bir site sayfası en iyi seçenek olabilir.|  
|Site sayfaları|Aşağıdaki görevlerden herhangi birini gerçekleştirmek istiyorsanız, bir site sayfası oluşturun:<br /><br /> -Sayfanın bir SharePoint kitaplığına ekleyin.<br />-Dinamik Web Bölümleri ve Web Bölümü bölgeleri gibi konak özellikleri sayfasına etkinleştirin.<br />-SharePoint Designer'ı kullanarak sayfayı özelleştirmek kullanıcıları etkinleştirin.<br /><br /> Özel kodu içermesi için sayfayı istiyorsanız, bir site sayfasını oluşturmayın. Bir site sayfası için özel kod ekleyebilirsiniz, ancak kodu çalıştıran kullanıcının SharePoint Designer kullanarak sayfa özelleştirir durdurur.|  
|Ana sayfalar|Site sayfaları için ortak yapı tanımlamak istiyorsanız bir ana sayfa ve uygulama sayfaları oluşturun.|  
|Sayfa düzenleri|Sayfa düzenleri özeldir [!INCLUDE[moss_14_long](../sharepoint/includes/moss-14-long-md.md)] ve, daha fazla site sayfaları ve uygulama sayfaları için ortak bir yapıya tanımlamanıza olanak sağlar.|  
  
 Her tür sayfa genel bakış için bkz. [yapı taşı: Sayfalar ve kullanıcı arabirimi](http://go.microsoft.com/fwlink/?LinkID=182095), ve [sayfa düzenleri ve ana sayfalar](http://go.microsoft.com/fwlink/?LinkID=182096).  
  
## <a name="create-application-pages"></a>Uygulama sayfaları oluşturma
 Visual Studio'da Uygulama sayfaları ekleyerek oluşturabilirsiniz bir **uygulama sayfası** bir SharePoint proje öğesi. Sayfasına denetim ekleme ve ardından kod ekleyerek denetim olaylarını işleme.  
  
 Sayfanın kod dosyasında kesme noktaları ayarlayın, hata ayıklayıcıyı başlatın ve ek yapılandırma adımları gerçekleştirmeden yerel bir SharePoint sitesine sayfasında test. Daha fazla bilgi için [SharePoint için uygulama sayfaları oluşturma](../sharepoint/creating-application-pages-for-sharepoint.md).  
  
## <a name="create-site-pages-master-pages-and-page-layouts"></a>Site sayfaları, ana sayfalar ve sayfa düzenleri oluşturma
 SharePoint Designer'ı kullanarak site sayfaları, ana sayfalar ve sayfa düzenleri oluşturabilirsiniz. Ardından, bu sayfaları Visual Studio'ya içeri aktarabilirsiniz. Visual Studio'da kullanılabilen kaynak denetimi özellikleri ve dağıtım yararlanmak istiyorsanız sayfalarınızı içeri aktarın. Daha fazla bilgi için [var olan bir SharePoint sitesinden öğeleri içeri aktarma](../sharepoint/importing-items-from-an-existing-sharepoint-site.md).  
  
 Bu sayfalar aldıktan sonra değiştirilmesi zor olduğundan, bunları içeri aktarmadan önce bu sayfaları tasarlamanız gerekir.  
  
## <a name="create-cascading-style-sheets-ecmascript-and-themes"></a>Geçişli stil sayfaları, ECMAScript ve Temalar oluşturma
 Visual Studio şablonları geliştirme geçişli stil sayfaları (CSS), ECMAScript (JavaScript, JScript) veya SharePoint siteleri için tema dosyası için sağlamaz. SharePoint SDK'da bulunan yönergeleri kullanarak veya SharePoint Tasarımcısı gibi araçları kullanarak bu dosyaları oluşturabilirsiniz.  
  
 Çözümünüz için bu dosyaları doğrudan ekleyebilir veya bunları içeri aktarabilir. Her iki durumda da eklediğiniz her öğe için uygun eşlenen klasörler oluşturmanız gerekir. Eşleşen bir klasör oluşturma hakkında daha fazla bilgi için bkz. [nasıl yapılır: eşlenmiş klasörler ekleme ve kaldırma](../sharepoint/how-to-add-and-remove-mapped-folders.md).  
  
 Geçişli stil sayfaları oluşturma hakkında daha fazla bilgi için bkz. [geçişli stil sayfaları sınıfı kullanımı SharePoint Foundation](http://go.microsoft.com/fwlink/?LinkID=182098). JavaScript ve JScript dosyaları bir SharePoint çözüm oluşturma hakkında daha fazla bilgi için bkz. [ayarı oluşturan bir temel ASPX sayfa için ECMAScript](http://go.microsoft.com/fwlink/?LinkID=182099). Temalar hakkında daha fazla bilgi için bkz. [yapı taşı: Sayfalar ve kullanıcı arabirimi](http://go.microsoft.com/fwlink/?LinkID=182095).  
  
## <a name="related-topics"></a>İlgili konular
  
|Başlık|Açıklama|  
|-----------|-----------------|  
|[SharePoint için uygulama sayfaları oluşturma](../sharepoint/creating-application-pages-for-sharepoint.md)|Uygulama sayfaları nasıl ekleyeceğinizi açıklar: *.aspx* SharePoint ana sayfası ile birleştirilmiş içeriği.|  
|[Nasıl yapılır: Uygulama sayfası oluşturma](../sharepoint/how-to-create-an-application-page.md)|Bir SharePoint sitesinde çalıştırmasının ASP.NET sayfaları oluşturma işlemi gösterilmektedir.|  
|[İzlenecek yol: SharePoint uygulama sayfası oluşturma](../sharepoint/walkthrough-creating-a-sharepoint-application-page.md)|Tasarım ve hata ayıklama SharePoint sitesi için bir ASP.NET Web sayfası işlemi gösterilmektedir.|  
