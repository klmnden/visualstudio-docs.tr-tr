---
title: XMLNodes denetimi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XMLNodes control, events
- XMLNodes control
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 227c7b72e8574556cfb18635b6fa329229c4bea6
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53865433"
---
# <a name="xmlnodes-control"></a>XMLNodes denetimi
  **Önemli** Microsoft Word ile ilgili bu konu kümesindeki bilgileri avantajı ve kişiler ve kimin bulunur Amerika Birleşik Devletleri ve kendi bölgeler dışında veya servis kullanan kuruluşlar için özel olarak sunulan veya geliştirme üzerinde çalışan programlar Ocak Microsoft uygulaması belirli işlevlerin ne zaman kaldırıldı 2010'dan önce Microsoft lisanslı Microsoft Word ürünler, Microsoft Word için özel XML ilgili. Bu bilgileri Microsoft Word ile ilgili değil okuma veya kişi ve kuruluşların Amerika Birleşik Devletleri ya da kullanarak veya Microsoft tarafından 10 Ocak 2010'dan sonra lisansına sahip Microsoft Word ürünleri üzerinde çalışan programlar geliştirme alt bölgeleri tarafından kullanılan ; Bu ürünlerin bu tarihten önce lisanslı veya satın alınan ve Amerika Birleşik Devletleri dışında kullanım için lisanslı ürünleri aynı davranmaz.  
  
 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]  
  
 <xref:Microsoft.Office.Tools.Word.XMLNodes> Denetimidir olayları ortaya koyan eşlenen XML düğümü nesneleri koleksiyonu. <xref:Microsoft.Office.Tools.Word.XMLNodes> Denetimi, yalnızca bir Microsoft Office Word belgesi üzerinde yinelenen bir şema öğesine eşlendiğinde oluşturulur. Yinelenen öğe, alt öğeler içeriyorsa, alt öğelerin her biri de olarak oluşturulan bir <xref:Microsoft.Office.Tools.Word.XMLNodes> denetimi.  
  
 Visual Studio XML düğümü koleksiyonunu oluşturduktan sonra Word nesne modeline geçiş yapmak zorunda kalmadan doğrudan denetim karşı programlama yapabilirsiniz. <xref:Microsoft.Office.Tools.Word.XMLNodes> Denetimi yalnızca belgeden öğe eşlemesi kaldırarak silinebilir.  
  
> [!NOTE]  
>  Bir alt öğenin erişim <xref:Microsoft.Office.Tools.Word.XMLNodes> aracılığıyla denetim <xref:Microsoft.Office.Tools.Word.XMLNodes.Item%2A> özelliği döndürür bir <xref:Microsoft.Office.Interop.Word.XMLNode> nesne yerine <xref:Microsoft.Office.Tools.Word.XMLNode> denetimi. Daha fazla bilgi için [konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md).  
  
## <a name="bind-data-to-the-control"></a>Veriyi denetime bağlama  
 Bir <xref:Microsoft.Office.Tools.Word.XMLNodes> denetimi veri bağlamayı desteklemez. Bunun nedeni, <xref:Microsoft.Office.Tools.Word.XMLNodes> denetim karmaşık veri bağlama yeteneğine sahip değil ve basit veri bağlama temsil edemez yinelenen veriler.  
  
## <a name="formatting"></a>Biçimlendirme  
 Metin belgesi içinde uygulanabilir her biçimlendirme için uygulanabilir bir <xref:Microsoft.Office.Tools.Word.XMLNodes> denetimi.  
  
## <a name="events"></a>Olaylar  
 İçin kullanılabilir olan olaylar <xref:Microsoft.Office.Tools.Word.XMLNodes> denetimi:  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.AfterInsert>  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.BeforeDelete>  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextEnter>  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextLeave>  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.Deselect>  
  
-   <xref:System.ComponentModel.IComponent.Disposed>  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.Select>  
  
-   <xref:Microsoft.Office.Tools.Word.XMLNodes.ValidationError>  
  
## <a name="compare-events"></a>Olayları karşılaştırın  
 Kullanıcı belirli bir bağlamı bilgilendirilmesine imleci taşındığında bir olay yakalayabilirsiniz <xref:Microsoft.Office.Tools.Word.XMLNodes> denetimi. Örneğin, olabilir bir <xref:Microsoft.Office.Tools.Word.XMLNodes> adlı Denetim `Customer` alt öğesi olan <xref:Microsoft.Office.Tools.Word.XMLNodes> adlı Denetim `Company`, ve `Company` iki çocuğu <xref:Microsoft.Office.Tools.Word.XMLNodes> adlarında `CompanyName` ve `CompanyRegion` gibi:  
  
```xml  
<Customer>  
    <Company>  
        <CompanyName>  
        <CompanyRegion>  
```  
  
 Eylemler bölmesinde denetimde göstermek istiyorsanız her imleç taşınan içine `Company` düğümünü, önemli imlecin bulunduğu olup olmadığını `CompanyName` veya `CompanyRegion` bağlamında her ikisi de çünkü `Company`. Bu durumda, kod yazabileceğiniz <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextEnter> olayı `Company`.  
  
 Çoğu durumda, imleç girdiğinde bir <xref:Microsoft.Office.Tools.Word.XMLNodes> denetlemek, her ikisi de <xref:Microsoft.Office.Tools.Word.XMLNodes.Select> ve <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextEnter> olayları ortaya çıkar. Aşağıdaki tabloda, bu olaylar arasındaki farklar gösterilmektedir.  
  
|Olay seçin|ContextEnter olay|  
|------------------|------------------------|  
|İmleç düğümlerinin birini yerleştirildiğinde gerçekleşir <xref:Microsoft.Office.Tools.Word.XMLNodes> koleksiyonu.|İmleç bir düğüm veya alt düğümleri içinde yeniden konumlandırıldığında gerçekleşir <xref:Microsoft.Office.Tools.Word.XMLNodes> koleksiyonundan bir alan düğümü bağlamı dışında. Diğer bir deyişle, yalnızca bağlamı değiştiğinde oluşturulur ve birden çok iç içe geçmiş harekete Geçirilmemesi <xref:Microsoft.Office.Tools.Word.XMLNodes> kontrol eder.|  
  
 Örneğin, dışında imleci taşıdığınızda `Customer` içine `CompanyName`, <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextEnter> olayları `Customer`, `Company`, ve `CompanyName` oluşturulur. Ardından imleci taşırsanız `CompanyName` için `CompanyRegion`, <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextEnter> yalnızca olay `CompanyRegion` oluşturulur, bağlam her ikisi için de aynı olduğundan `Company` ve `Customer`. Birden çok olabilir `Company` belgenizdeki düğümleri. İmleci taşırsanız `CompanyName` bir düğüm `Company` için `CompanyName` başka bir düğüm `Company`, bağlam nedenle yalnızca aynıdır <xref:Microsoft.Office.Tools.Word.XMLNodes.Select> olayı oluşturulur.  
  
 Aynı arasındaki farklar <xref:Microsoft.Office.Tools.Word.XMLNodes.ContextLeave> olay ve <xref:Microsoft.Office.Tools.Word.XMLNodes.Deselect> olay.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)   
 [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)   
 [XMLNode denetimi](../vsto/xmlnode-control.md)   
 [Nasıl yapılır: Word belgelerine XMLNodes denetimleri ekleme](../vsto/how-to-add-xmlnodes-controls-to-word-documents.md)   
 [Nasıl yapılır: Şemaları Visual Studio içindeki Word belgeleriyle eşleştirme](../vsto/how-to-map-schemas-to-word-documents-inside-visual-studio.md)   
 [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)  
