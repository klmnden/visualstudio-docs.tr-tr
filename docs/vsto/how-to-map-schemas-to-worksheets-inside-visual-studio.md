---
title: 'Nasıl yapılır: Şemaları Visual Studio içindeki çalışma sayfalarıyla eşleştirme'
titleSuffix: ''
ms.custom: seodec18
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- XML schemas [Office development in Visual Studio], mapping
- mappings [Office development in Visual Studio], XML schemas to Excel worksheets
- Excel [Office development in Visual Studio], XML schemas
- worksheets [Office development in Visual Studio], XML schemas
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: d01d68404314b366e968f0c2551352d8501ed9ae
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54866340"
---
# <a name="how-to-map-schemas-to-worksheets-inside-visual-studio"></a>Nasıl yapılır: Şemaları Visual Studio içindeki çalışma sayfalarıyla eşleştirme
  Visual Studio'da çalışma açıkken bir XML Şeması çalışma sayfasına eşleyebilirsiniz. Visual Studio'nun dışında çalışma kitabını açtığınızda kullandığınız aynı Microsoft Office Excel araçları kullanırsınız. Office project, çalışma sayfasında önce şemayı eşleştirdiğinizde veya Excel çözümünüzü oluşturduktan sonra aynı nesneleri oluşturur.  
  
 [!INCLUDE[appliesto_xlalldoc](../vsto/includes/appliesto-xlalldoc-md.md)]  
  
> [!NOTE]  
>  Excel çözümleri, çok bölümlü XML şemaları kullanamazsınız.  
  
## <a name="to-map-an-xml-schema-to-an-excel-worksheet-in-visual-studio"></a>Visual Studio'da bir Excel çalışma sayfasına bir XML Şeması eşlemek için  
  
1.  Excel çalışma kitabı veya şablondaki projeyi Visual Studio içinde açın.  
  
2.  Çalışma sayfası tasarımcıya odağı taşımak için tıklayın.  
  
3.  Şerit üzerinde tıklayın **Geliştirici** sekmesi.  
  
    > [!NOTE]  
    >  Varsa **Geliştirici** sekme görünür değilse, önce görünür olmalıdır. Daha fazla bilgi için [nasıl yapılır: Şeritte Geliştirici sekmesini gösterme](../vsto/how-to-show-the-developer-tab-on-the-ribbon.md).  
  
4.  İçinde **XML** grubunda **kaynak**.  
  
     **XML kaynağı** penceresi açılır.  
  
5.  İçinde **XML kaynağı** penceresinde tıklayın **XML eşlemeleri**.  
  
     **XML eşlemeleri** iletişim kutusu açılır.  
  
6.  İçinde **XML eşlemeleri** iletişim kutusu, tıklayın **Ekle**.  
  
7.  Şema dosyasına göz atın, onu seçin ve ardından **açık**.  
  
8.  **Tamam**'ı tıklatın.  
  
     Şema temsil edilir **XML kaynağı** penceresi. Projenizde, belirlenmiş bir <xref:System.Data.DataSet> şemaya göre oluşturulur ve <xref:System.Windows.Forms.BindingSource> oluşturulur.  
  
9. Öğeleri sürükleme **XML kaynağı** çalışma oluşturulacak ilgili denetimlerin, istediğiniz yerde penceresine.  
  
     Yinelenmeyen bir şema öğesi sürükleyin, Office projesi oluşturur. bir <xref:Microsoft.Office.Tools.Excel.XmlMappedRange> otomatik olarak bağlı denetim <xref:System.Windows.Forms.BindingSource>.  
  
     Yinelenen bir şema öğesine sürüklediğinizde, Office projesi oluşturur. bir <xref:Microsoft.Office.Tools.Excel.ListObject> otomatik olarak bir veri kaynağına bağlı olmayan bir denetim. Daha fazla bilgi için [XML şemaları ve verileri belge düzeyi özelleştirmeleri](../vsto/xml-schemas-and-data-in-document-level-customizations.md).  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Nasıl yapılır: Şemaları Visual Studio içindeki Word belgeleriyle eşleştirme](../vsto/how-to-map-schemas-to-word-documents-inside-visual-studio.md)   
 [XML şemaları ve belge düzeyi özelleştirmelerdeki veriler](../vsto/xml-schemas-and-data-in-document-level-customizations.md)  
