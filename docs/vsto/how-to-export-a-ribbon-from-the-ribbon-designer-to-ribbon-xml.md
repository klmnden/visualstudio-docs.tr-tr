---
title: "Nasıl Yapılır: Bir Şerit Şerit Tasarımcısından Şerit XML'ine verebilir."
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- custom Ribbon, XML
- customizing the Ribbon, XML
- Ribbon [Office development in Visual Studio], XML
- Ribbon [Office development in Visual Studio], exporting
- XML [Office development in Visual Studio], Ribbon
- Ribbon Designer [Office development in Visual Studio]
- exporting Ribbon
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: c1f50ec718e1f3a6c9780d956f9b845abd890bb1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53894067"
---
# <a name="how-to-export-a-ribbon-from-the-ribbon-designer-to-ribbon-xml"></a>Nasıl Yapılır: Bir Şerit Şerit Tasarımcısından Şerit XML'ine verebilir.
  **Şerit (Görsel Tasarımcı)** öğesi, tüm olası şeridi özelleştirme türlerini desteklemez. Şerit Gelişmiş şekilde özelleştirmek için Şerit Tasarımcısından Şerit XML'ine verebilir ve XML doğrudan düzenlemek.  
  
> [!NOTE]  
>  Tüm özellik değerlerini Şerit XML dosyasında görünür. Daha fazla bilgi için [Şerite Genel Bakış](../vsto/ribbon-overview.md).  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
### <a name="to-export-a-ribbon-from-the-ribbon-designer-to-ribbon-xml"></a>Bir Şerit Şerit Tasarımcısından Şerit XML'ine dışarı aktarmak için  
  
1.  Şerit kod dosyasını sağ tıklatın **Çözüm Gezgini**ve ardından **Görünüm Tasarımcısı**.  
  
2.  Şerit Tasarımcısını sağ tıklayın ve ardından **dışarı Şerit XML**.  
  
     Visual Studio Ribbon XML dosyasındaki ve bir Şerit XML kod dosyası projenize ekler.  
  
3.  Şerit kod sınıfında ile başlayan açıklamaları bulmak `TODO:`.  
  
4.  Bu açıklamalar için kod bloğu kopyalayın **ThisAddIn**, **ThisWorkbook**, veya **ThisDocument** , geliştirdiğiniz çözümü türünü bağlı olarak, sınıf.  
  
     Bu kod, bulmak ve kendi özel Şerit'i yüklemek Microsoft Office uygulamasını sağlar. Daha fazla bilgi için [Ribbon XML](../vsto/ribbon-xml.md).  
  
5.  İçinde **ThisAddIn**, **ThisWorkbook**, veya **ThisDocument** sınıfından, kod bloğunun açıklamasını kaldırın.  
  
     Kodun açıklamasını kaldırın, sonra aşağıdaki örneğe benzemelidir. Bu örnekte, Şerit sınıfı olarak adlandırılan `MyRibbon`.  
  
     [!code-csharp[Trin_Ribbon_Custom_Tab_XML#1](../vsto/codesnippet/CSharp/Trin_Ribbon_Custom_Tab_XML_O12/ThisAddIn.cs#1)]
     [!code-vb[Trin_Ribbon_Custom_Tab_XML#1](../vsto/codesnippet/VisualBasic/Trin_Ribbon_Custom_Tab_XML_O12/ThisAddIn.vb#1)]  
  
6.  Geçiş için Ribbon XML kodunu ve bulma `Ribbon Callbacks` bölge.  
  
     Burada, bir düğmeye tıklanması gibi kullanıcı eylemlerini işlemek için geri çağırma yöntemleri yazdığınız budur.  
  
7.  Şerit Tasarımcısı kod yazdığınız her bir olay işleyicisi için bir geri çağırma yöntemi oluşturun.  
  
8.  Tüm olay işleyici kodu olay işleyicilerindeki geri çağırma yöntemlerine taşıyın ve Ribbon genişletilebilirliği (RibbonX) programlama modeliyle çalışmak için kodu değiştirin.  
  
     Geri çağırma yöntemleri yazmak ve RibbonX programlama modelini kullanma hakkında daha fazla bilgi için bkz: [Ribbon XML](../vsto/ribbon-xml.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Şerite Genel Bakış](../vsto/ribbon-overview.md)   
 [Şerit Tasarımcısı](../vsto/ribbon-designer.md)   
 [Şerit XML](../vsto/ribbon-xml.md)   
 [İzlenecek yol: Şerit Tasarımcısını kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [İzlenecek yol: Şerit XML kullanarak özel sekme oluşturma](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)  
