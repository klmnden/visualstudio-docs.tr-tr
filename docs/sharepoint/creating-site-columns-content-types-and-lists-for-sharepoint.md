---
title: SharePoint için site sütunları, içerik türleri ve listeler oluşturma | Microsoft Docs
ms.date: 02/02/2017
ms.topic: conceptual
f1_keywords:
- VS.SharePointTools.ListDesigner.ContentTypeSetting
- VS.SharePointTools.ContentTypeDesigner.CommonPropertiesPage
- VS.SharePointTools.ListDesigner.CreatingLists
- VS.SharePointTools.ListDesigner.ListPage
- VS.SharePointTools.ListDesigner.ViewPage
- VS.SharePointTools.ListDesigner.CommonPropertiesPage
- VS.SharePointTools.ContentTypeDesigner.ColumnsPage
dev_langs:
- VB
- CSharp
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 8cecb3e78cea90b927dc6b67b5b4a2cb50bfa87c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62581102"
---
# <a name="create-site-columns-content-types-and-lists-for-sharepoint"></a>SharePoint için site sütunları, içerik türleri ve listeler oluşturma
  Visual Studio da dahil olmak üzere birçok farklı temel SharePoint öğeleri için proje öğesi şablonları sağlar *listeler* ve *içerik türlerine*, ikisi için de site sütunları dahil edebilirsiniz (veya  *alanları*). İçerik türleri ve listeler için yeni tasarımcılar, bu öğeler her zamankinden daha kolay oluşturma olun.

## <a name="site-columns"></a>Site sütunları
 Site sütunları, bir SharePoint projesine ekleyebilirsiniz en temel öğeleri biridir. Bir site sütunu, bir telefon numarası, açıklama ya da bir kişi listesini kişi şehir adı gibi bir veri türünü temsil eder.

 Yeni site sütunu proje öğesi Şablon oluşturulurken site sütunları, Visual Studio'nun önceki sürümde daha kolay getirir. Yeni bir site sütunu oluşturduktan sonra site sütunun XML değiştirebilirsiniz *Elements.xml* görünen adı, kendi veri türüne ve site sütunu görünmesini istediğiniz grubu gibi istediğiniz bilgileri içeren dosya SharePoint. Site sütunları hakkında daha fazla bilgi için bkz: [sütunları giriş](http://go.microsoft.com/fwlink/?LinkId=224996).

## <a name="content-types-and-lists"></a>İçerik türleri ve listeler
 İçerik türlerine ve listelerine arasında en sık kullanılan SharePoint öğeleridir.

 Bir içerik türü, bir SharePoint listesi veya belge kitaplığında meta verileri, iş akışı ve öğeleri kategorisi için davranışını tanımlar. Örneğin, bir içerik türü için bilgi kişiler listesinden veya görev listesini oluşturabilirsiniz. Sütun adı, e-posta, telefon numarası ve adres gibi iletişim bir içerik türü içerebilir. Site düzeyinde tanımladığınız bir içerik türü, sitedeki tüm liste veya belge kitaplığı bağımsızdır. Farklı listeler veya SharePoint sitesinde belge kitaplıkları ile aynı içerik türü kullanabilirsiniz. Çeşitli içerik türleri aynı liste veya belge kitaplığı kullanabilirsiniz.

 Bir liste, başkalarıyla paylaşabilirsiniz SharePoint bilgi koleksiyonudur. Liste, veri içeren sütun satırlarını oluşur. Listelerin bazı örnekleri şunlardır: bir görev listesi, bir kişi listesi ve bir Duyurular listesi.

 Yeni içerik türü ve liste tasarımcılarda [!INCLUDE[vsprvs](../sharepoint/includes/vsprvs-md.md)] çok daha kolay ve daha sezgisel Visual Studio'nun önceki sürümde site içerik türleri ve listeler oluşturma olun. Kullanıcı Arabirimi sayesinde tanıdık bir şekilde içerik türlerine ve listelerine görsel olarak oluşturmak ve sıralama ve listelerdeki veri grubunda ve grup başlıklarını kullanın olanak tanır. İçerik türleri hakkında daha fazla bilgi için bkz. [içerik türleri](http://go.microsoft.com/fwlink/?LinkId=224997). Listeleri hakkında daha fazla bilgi için bkz. [liste formları](http://go.microsoft.com/fwlink/?LinkId=224998) ve [liste görünümleri](http://go.microsoft.com/fwlink/?LinkId=224999).

## <a name="related-topics"></a>İlgili konular

|Başlık|Açıklama|
|-----------|-----------------|
|[İzlenecek yol: SharePoint için site sütunu, içerik türü ve liste oluşturma](../sharepoint/walkthrough-create-a-site-column-content-type-and-list-for-sharepoint.md)|Özel bir içerik türünde kullanılan site sütunları oluşturma işlemini gösterir. İçerik türü, özel bir listede sonra kullanılır.|

## <a name="see-also"></a>Ayrıca bkz.
- [SharePoint 2010'da geliştirmeye başlayın](http://go.microsoft.com/fwlink/?LinkId=225000)
