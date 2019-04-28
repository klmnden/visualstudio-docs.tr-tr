---
title: XMLNode denetimi
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XMLNode control
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a8bd5c4612b59f909ae623eb4092a209798f98c5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62975717"
---
# <a name="xmlnode-control"></a>XMLNode denetimi
  **Önemli** Microsoft Word ile ilgili bu konu kümesindeki bilgileri avantajı ve kişiler ve kimin bulunur Amerika Birleşik Devletleri ve kendi bölgeler dışında veya servis kullanan kuruluşlar için özel olarak sunulan veya geliştirme üzerinde çalışan programlar Ocak Microsoft uygulaması belirli işlevlerin ne zaman kaldırıldı 2010'dan önce Microsoft lisanslı Microsoft Word ürünler, Microsoft Word için özel XML ilgili. Bu bilgileri Microsoft Word ile ilgili değil okuma veya kişi ve kuruluşların Amerika Birleşik Devletleri ya da kullanarak veya Microsoft tarafından 10 Ocak 2010'dan sonra lisansına sahip Microsoft Word ürünleri üzerinde çalışan programlar geliştirme alt bölgeleri tarafından kullanılan ; Bu ürünlerin bu tarihten önce lisanslı veya satın alınan ve Amerika Birleşik Devletleri dışında kullanım için lisanslı ürünleri aynı davranmaz.

 [!INCLUDE[appliesto_wdalldoc](../vsto/includes/appliesto-wdalldoc-md.md)]

 <xref:Microsoft.Office.Tools.Word.XMLNode> Denetimidir olayları ortaya koyan ve verilere bağlı eşlenen bir XML düğüm nesnesi. <xref:Microsoft.Office.Tools.Word.XMLNode> Denetimi, yalnızca bir Microsoft Office Word belgesine yinelenmeyen bir şema öğesine eşlendiğinde oluşturulur. Visual Studio XML düğümü oluşturduktan sonra Word nesne modeline geçiş yapmak zorunda kalmadan doğrudan karşı programlama yapabilirsiniz.

 <xref:Microsoft.Office.Tools.Word.XMLNode> Denetimi, yalnızca öğe eşlemesi Word'de kaldırarak silinebilir.

## <a name="bind-data-to-the-control"></a>Veriyi denetime bağlama
 Bir <xref:Microsoft.Office.Tools.Word.XMLNode> basit veri bağlama denetimi destekler. XML düğümü kullanarak bir veri kaynağına bağlanmalıdır <xref:System.Windows.Forms.IBindableComponent.DataBindings%2A> özelliği. İlişkili veri kümesindeki veriler güncelleştirilirse <xref:Microsoft.Office.Tools.Word.XMLNode> denetimi değişiklikleri yansıtır.

## <a name="formatting"></a>Biçimlendirme
 Uygulanabilir biçimlendirme bir <xref:Microsoft.Office.Interop.Word.XMLNode> nesne uygulanabilir bir <xref:Microsoft.Office.Tools.Word.XMLNode> denetimi. Bu yazı tipleri, alt çizgi stilleri ve stilleri karakteri içerir.

## <a name="events"></a>Olaylar
 Aşağıdakiler için kullanılabilir <xref:Microsoft.Office.Tools.Word.XMLNode> denetimi:

- <xref:Microsoft.Office.Tools.Word.XMLNode.AfterInsert>

- <xref:Microsoft.Office.Tools.Word.XMLNode.BeforeDelete>

- <xref:Microsoft.Office.Tools.Word.XMLNode.BindingContextChanged>

- <xref:Microsoft.Office.Tools.Word.XMLNode.ContextEnter>

- <xref:Microsoft.Office.Tools.Word.XMLNode.ContextLeave>

- <xref:Microsoft.Office.Tools.Word.XMLNode.Deselect>

- <xref:System.ComponentModel.IComponent.Disposed>

- <xref:Microsoft.Office.Tools.Word.XMLNode.Select>

- <xref:Microsoft.Office.Tools.Word.XMLNode.ValidationError>

## <a name="compare-events"></a>Olayları karşılaştırın
 Kullanıcı belirli bir bağlamı bilgilendirilmesine imleci taşındığında bir olay yakalayabilirsiniz <xref:Microsoft.Office.Tools.Word.XMLNode> denetimi. Örneğin, olabilir bir <xref:Microsoft.Office.Tools.Word.XMLNode> adlı Denetim `Customer` alt öğesi olan <xref:Microsoft.Office.Tools.Word.XMLNode> adlı Denetim `Company`, ve `Company` iki çocuğu <xref:Microsoft.Office.Tools.Word.XMLNode> adlarında `CompanyName` ve `CompanyRegion` gibi:

```xml
<Customer>
    <Company>
        <CompanyName>
        <CompanyRegion>
```

 Eylemler bölmesinde denetimde göstermek istiyorsanız her imleç taşınan içine `Company` düğümünü, önemli imlecin bulunduğu olup olmadığını `CompanyName` veya `CompanyRegion` bağlamında her ikisi de çünkü `Company`. Bu durumda, kod yazabileceğiniz <xref:Microsoft.Office.Tools.Word.XMLNode.ContextEnter> olayı `Company`.

 Çoğu durumda, imleç girdiğinde bir <xref:Microsoft.Office.Tools.Word.XMLNode> denetlemek, her ikisi de <xref:Microsoft.Office.Tools.Word.XMLNode.Select> ve <xref:Microsoft.Office.Tools.Word.XMLNode.ContextEnter> olayları ortaya çıkar. Aşağıdaki tabloda, bu olaylar arasındaki farklar gösterilmektedir.

|Olay seçin|ContextEnter olay|
|------------------|------------------------|
|İmleç içine yerleştirildiğinde gerçekleşir bir <xref:Microsoft.Office.Tools.Word.XMLNode>.|İmleç içine yerleştirildiğinde gerçekleşir bir <xref:Microsoft.Office.Tools.Word.XMLNode> veya düğümün bağlamı dışında bir alandan alt düğümlerinden biri. Diğer bir deyişle, yalnızca bağlamı değiştiğinde oluşturulur.|

 Örneğin, dışında imleci taşıdığınızda `Customer` içine `CompanyName`, <xref:Microsoft.Office.Tools.Word.XMLNode.ContextEnter> olayı `Customer`, `Company`, ve `CompanyName` tetiklenir. Ardından imleci taşırsanız `CompanyName` için `CompanyRegion`, yalnızca <xref:Microsoft.Office.Tools.Word.XMLNode.ContextEnter> olayı `CompanyRegion` hala bağlamındadır olduğundan tetiklenir `Company` ve `Customer`.

 Aynı arasındaki farklar <xref:Microsoft.Office.Tools.Word.XMLNode.ContextLeave> olay ve <xref:Microsoft.Office.Tools.Word.XMLNode.Deselect> olay.

## <a name="see-also"></a>Ayrıca bkz.
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Genişletilmiş nesneleri kullanarak Word'ü otomatikleştirirken](../vsto/automating-word-by-using-extended-objects.md)
- [XMLNodes denetimi](../vsto/xmlnodes-control.md)
- [Nasıl yapılır: Word belgelerine XMLNode denetimleri ekleme](../vsto/how-to-add-xmlnode-controls-to-word-documents.md)
- [Nasıl yapılır: Şemaları Visual Studio içindeki Word belgeleriyle eşleştirme](../vsto/how-to-map-schemas-to-word-documents-inside-visual-studio.md)
- [Konak denetimlerinin ve konak öğelerinin programlama sınırlamaları](../vsto/programmatic-limitations-of-host-items-and-host-controls.md)
