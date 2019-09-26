---
title: Office Projelerindeki Nesnelere Genel erişim
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- ThisDocument_Shutdown
- ThisDocument_Startup
- Globals class, object global access
- worksheets [Office development in Visual Studio], global access
- documents [Office development in Visual Studio], global access
- event handlers [Office development in Visual Studio]
- ThisWorkbook_Startup
- application-level addins [Office development in Visual Studio]
- addins [Office development in Visual Studio], events
- workbooks [Office development in Visual Studio], global access
- ThisWorkbook_Shutdown
- document-level customizations [Office development in Visual Studio]
- Startup event
- Shutdown event
- projects [Office development in Visual Studio], global access
- Office documents [Office development in Visual Studio, global access
- ThisAddin_Startup
- events [Office development in Visual Studio]
- ThisAddIn_Shutdown
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: f05f18201a055ac88e4af90d7b8e4d9db8f4e4b6
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71253443"
---
# <a name="global-access-to-objects-in-office-projects"></a>Office Projelerindeki Nesnelere Genel erişim
  Bir Office projesi oluşturduğunuzda, Visual Studio otomatik olarak projede adlı `Globals` bir sınıf oluşturur. Çalışma zamanında, projedeki `Globals` herhangi bir koddan farklı proje öğelerine erişmek için sınıfını kullanabilirsiniz.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

## <a name="how-to-use-the-globals-class"></a>Globals sınıfını kullanma
 `Globals`, projenizdeki belirli öğelere başvuruları tutan statik bir sınıftır. `Globals` Sınıfını kullanarak, çalışma zamanında projedeki herhangi bir koddan aşağıdaki öğelere erişebilirsiniz:

- Excel çalışma `Sheet`kitabı veya şablon projesindeki ven`ThisWorkbook` sınıfları. `Globals.ThisWorkbook` Ve n`Sheet`özelliklerini kullanarak bu nesnelere erişebilirsiniz.

- Word belgesi veya şablon projesindeki sınıf.`ThisDocument` `Globals.ThisDocument` Özelliğini kullanarak bu nesneye erişebilirsiniz.

- VSTO eklenti projesindeki sınıfı. `ThisAddIn` `Globals.ThisAddIn` Özelliğini kullanarak bu nesneye erişebilirsiniz.

- Projenizdeki şerit tasarımcısını kullanarak özelleştirdiğiniz tüm şeritler. `Globals.Ribbons` Özelliğini kullanarak Şeritlere erişebilirsiniz. Daha fazla bilgi için bkz. [çalışma zamanında Şerit 'e erişme](../vsto/accessing-the-ribbon-at-run-time.md).

- Outlook VSTO eklenti projesindeki tüm Outlook form bölgeleri. `Globals.FormRegions` Özelliğini kullanarak form bölgelerine erişebilirsiniz. Daha fazla bilgi için bkz. [çalışma zamanında form bölgesine erişme](../vsto/accessing-a-form-region-at-run-time.md).

- Şerit denetimleri oluşturmanızı ve [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)]veya öğesini hedefleyen projelerde çalışma zamanında öğeleri barındırmanızı sağlayan bir fabrika nesnesi. `Globals.Factory` Özelliğini kullanarak bu nesneye erişebilirsiniz. Bu nesne, aşağıdaki arayüzleri uygulayan bir sınıfın örneğidir:

  - <xref:Microsoft.Office.Tools.Factory>

  - <xref:Microsoft.Office.Tools.Excel.Factory>

  - <xref:Microsoft.Office.Tools.Outlook.Factory>

  - <xref:Microsoft.Office.Tools.Word.Factory>

  Örneğin, bir Kullanıcı, Excel için `Globals.Sheet1` belge düzeyindeki bir projede eylemler bölmesindeki <xref:Microsoft.Office.Tools.Excel.NamedRange> bir düğmeye `Sheet1` tıkladığında bir denetime metin eklemek için özelliğini kullanabilirsiniz.

  [!code-vb[Trin_VstcoreProgramming#1](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/Sheet1.vb#1)]
  [!code-csharp[Trin_VstcoreProgramming#1](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/Sheet1.cs#1)]

## <a name="initialize-the-globals-class"></a>Globals sınıfını başlatma
 Belge veya VSTO eklentisi başlatılmadan önce `Globals` sınıfı kullanmayı deneyen kod, çalışma zamanı özel durumu oluşturabilir. Örneğin, sınıf düzeyinde `Globals` bir değişken bildirirken kullanılması başarısız olabilir `Globals` çünkü sınıf, bildirilmeyen nesne örneklendirmeden önce tüm konak öğelerinin başvuruları ile başlatılmamış olabilir.

> [!NOTE]
> `Globals` Sınıf tasarım zamanında hiçbir zaman başlatılmaz, ancak denetim örnekleri tasarımcı tarafından oluşturulur. Yani, bir kullanıcı denetimi sınıfının içinden `Globals` sınıfının bir özelliğini kullanan bir kullanıcı denetimi oluşturursanız, döndürülen nesneyi kullanmayı denemeden önce özelliğin **null** döndürüp döndürmediğini denetlemeniz gerekir.

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma zamanında Şerite erişin](../vsto/accessing-the-ribbon-at-run-time.md)
- [Çalışma zamanında form bölgesine erişme](../vsto/accessing-a-form-region-at-run-time.md)
- [Konak öğeleri ve konak denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Belge konak öğesi](../vsto/document-host-item.md)
- [Çalışma kitabı konak öğesi](../vsto/workbook-host-item.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)
