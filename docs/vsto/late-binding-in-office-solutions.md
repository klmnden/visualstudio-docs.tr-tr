---
title: Office çözümlerinde geç bağlama
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- objects [Office development in Visual Studio], casting
- types [Office development in Visual Studio], casting
- automation [Office development in Visual Studio], casting objects
- casting, object to specific type
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 520ad17bf96f4a6c657a8bd48ac0fdd29b52e1b1
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54873177"
---
# <a name="late-binding-in-office-solutions"></a>Office çözümlerinde geç bağlama
  Nesne modellerinde Office uygulamalarının bazı türleri geç bağlama özellikleri kullanılabilir olan işlevsellik sağlar. Örneğin, yöntemler ve özellikler farklı türde Office uygulamasının bağlama nesneleri döndürebilir ve bazı türleri farklı yöntemler veya farklı bağlamlardaki özelliklerinde kullanıma sunabilirsiniz.  
  
 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]  
  
 Visual Basic projeleri **Option Strict** kapalı ve görsel C# hedefleyen projelerde [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)] doğrudan, bu geç bağlama özellikleri uygulayan türleri ile çalışabilir.  
  
## <a name="implicit-and-explicit-casting-of-object-return-values"></a>Örtük ve açık atama nesnenin dönüş değerleri  
 Birçok yöntem ve özellikleri Microsoft Office birincil birlikte çalışma derlemeleri (PIA) iade <xref:System.Object> birkaç farklı türde nesne döndürdüğünden, değerleri. Örneğin, <xref:Microsoft.Office.Tools.Excel.Workbook.ActiveSheet%2A> özelliği döndürür bir <xref:System.Object> dönüş değeri bu nedenle bir <xref:Microsoft.Office.Interop.Excel.Worksheet> veya <xref:Microsoft.Office.Interop.Excel.Chart> active sayfanın ne olduğuna bağlı olarak nesnesi.  
  
 Bir yöntem veya özellik döndürdüğünde bir <xref:System.Object>, açıkça (Visual Basic'te) nesne Visual Basic projelerinde doğru türe dönüştürmeniz gerekir burada **Option Strict** açıktır. Açık tür dönüştürme gerekmez <xref:System.Object> dönüş değerleri Visual Basic projelerinde burada **Option Strict** kapalıdır.  
  
 Çoğu durumda, başvuru belgeleri döndüren bir üye için dönüş değeri olası türleri listeler bir <xref:System.Object>. Dönüştürme ya da nesneye Kod Düzenleyicisi'nde nesne için IntelliSense sağlar.  
  
 Visual Basic dönüştürme hakkında daha fazla bilgi için bkz. [örtük ve açık dönüştürmeler &#40;Visual Basic&#41; ](/dotnet/visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions) ve [CType işlevi &#40;Visual Basic&#41;](/dotnet/visual-basic/language-reference/functions/ctype-function).  
  
### <a name="examples"></a>Örnekler  
 Aşağıdaki kod örneği bir Visual Basic projesinde bir nesne için belirli bir tür dönüştürme gösterilmektedir burada **Option Strict** açıktır. İçinde bu tür bir proje açıkça dönüştürmelisiniz <xref:Microsoft.Office.Tools.Excel.WorksheetBase.Cells%2A> özelliğini bir <xref:Microsoft.Office.Interop.Excel.Range>. Bu örnek adlı bir çalışma sayfası sınıfı ile bir belge düzeyi Excel proje gerektirir `Sheet1`.  
  
 [!code-vb[Trin_VstcoreProgramming#9](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/Sheet1.vb#9)]  
  
 Aşağıdaki kod örneği, bir nesne belirli bir türüne örtük olarak bir Visual Basic projesinde dönüştürülecek gösterilmiştir burada **Option Strict** kapalı veya bir görselde C# hedefleyen proje [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]. Projeleri, bu tür <xref:Microsoft.Office.Tools.Excel.WorksheetBase.Cells%2A> özelliği türünden örtük olarak bir <xref:Microsoft.Office.Interop.Excel.Range>. Bu örnek adlı bir çalışma sayfası sınıfı ile bir belge düzeyi Excel proje gerektirir `Sheet1`.  
  
 [!code-vb[Trin_VstcoreProgramming#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreProgrammingExcelVB/Sheet1.vb#10)]
 [!code-csharp[Trin_VstcoreProgramming#10](../vsto/codesnippet/CSharp/Trin_VstcoreProgrammingExcelCS/Sheet1.cs#10)]  
  
## <a name="access-members-that-are-available-only-through-late-binding"></a>Yalnızca geç bağlama aracılığıyla kullanılabilir olan erişim üyeleri  
 Bazı özellikler ve Office PIA'ların yöntemleri geç bağlama aracılığıyla kullanılabilir. Visual Basic projelerinde **Option Strict** kapalı veya görselde C# hedefleyen projelerde [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)] veya [!INCLUDE[net_v45](../vsto/includes/net-v45-md.md)], geç bağlanan üyelere erişim için bu dillerde geç bağlama özellikleri kullanabilirsiniz. Visual Basic projelerinde **Option Strict** açıktır, bu üyelere erişim için yansıma kullanmalısınız.  
  
### <a name="examples"></a>Örnekler  
 Aşağıdaki kod örneği, Visual Basic projesinde geç bağlama üyelerine nasıl erişileceğini gösteren burada **Option Strict** kapalı veya bir görselde C# hedefleyen proje [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]. Bu örnekte, geç bağlanan erişen **adı** özelliği **Dosya Aç** Word'de bir iletişim kutusu. Bu örneği kullanmak için çalıştırın `ThisDocument` veya `ThisAddIn` Word projesindeki sınıf.  
  
 [!code-vb[Trin_VstcoreWordAutomation#122](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#122)]
 [!code-csharp[Trin_VstcoreWordAutomation#122](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#122)]  
  
 Aşağıdaki kod örneği, Visual Basic projesinde aynı görevi başarmak için yansıma kullanmak gösterilmiştir burada **Option Strict** açıktır.  
  
 [!code-vb[Trin_VstcoreWordAutomation#102](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#102)]  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Office çözümlerinde kod yazma](../vsto/writing-code-in-office-solutions.md)   
 [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)   
 [Tür dinamiği kullanma &#40;C&#35; Programlama Kılavuzu&#41;](/dotnet/csharp/programming-guide/types/using-type-dynamic)   
 [Option Strict deyimi](/dotnet/visual-basic/language-reference/statements/option-strict-statement)   
 [Yansıma (C#)](/dotnet/csharp/programming-guide/concepts/reflection)  
 [Yansıma (Visual Basic)](/dotnet/visual-basic/programming-guide/concepts/reflection)  
 [Office çözümleri oluşturma ve tasarlama](../vsto/designing-and-creating-office-solutions.md)  
