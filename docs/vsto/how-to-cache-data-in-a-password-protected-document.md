---
title: 'Nasıl Yapılır: Bir parola korumalı belgede veriyi önbelleğe alma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- data caching [Office development in Visual Studio], protected documents
- datasets [Office development in Visual Studio], caching
- data [Office development in Visual Studio], caching
author: John-Hart
ms.author: johnhart
manager: douge
ms.workload:
- office
ms.openlocfilehash: c47f76c2371737b10c5eb58566cef388aff5fcd7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53968423"
---
# <a name="how-to-cache-data-in-a-password-protected-document"></a>Nasıl Yapılır: Bir parola korumalı belgede veriyi önbelleğe alma
  Bir belge veya parola korumalı çalışma kitabı verileri önbelleğe veri eklerseniz, önbelleğe alınan verilerde yapılan değişiklikleri otomatik olarak kaydedilmez. Projenizdeki iki yöntemi geçersiz kılarak, önbelleğe alınan verilerde yapılan değişiklikleri kaydedebilirsiniz.  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
## <a name="caching-in-word-documents"></a>Word belgelerinde önbelleğe alma  
  
### <a name="to-cache-data-in-a-word-document-that-is-protected-with-a-password"></a>Parola ile korunan bir Word belgesinde verileri önbelleğe almak için  
  
1.  İçinde `ThisDocument` sınıfı, bir ortak alan veya özellik önbelleğe alınacak işaretleyin. Daha fazla bilgi için [veriyi önbelleğe alma](../vsto/caching-data.md).  
  
2.  Geçersiz kılma <xref:Microsoft.Office.Tools.Word.DocumentBase.UnprotectDocument%2A> yönteminde `ThisDocument` sınıfı ve belge korumayı kaldırın.  
  
     Belge kaydedildiğinde [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] belgenin korumasını kaldırmak için bir fırsat vermek için bu yöntemi çağırır. Bu değişikliklerin kaydedilmesi için önbelleğe alınmış verilerin sağlar.  
  
3.  Geçersiz kılma <xref:Microsoft.Office.Tools.Word.DocumentBase.ProtectDocument%2A> yönteminde `ThisDocument` sınıfı ve belge koruma yeniden uygulayın.  
  
     Belge kaydedildikten sonra [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] belge koruma uygulamak için bir fırsat vermek için bu yöntemi çağırır.  
  
### <a name="example"></a>Örnek  
 Aşağıdaki kod örneği, bir parola ile korunan bir Word belgesinde verileri önbelleğe almak nasıl gösterir. Kod koruma kaldırılmadan önce <xref:Microsoft.Office.Tools.Word.DocumentBase.UnprotectDocument%2A> yöntemi, geçerli kaydeder <xref:Microsoft.Office.Tools.Word.Document.ProtectionType%2A> değeri, aynı koruma türünü uygulanabilir böylece <xref:Microsoft.Office.Tools.Word.DocumentBase.ProtectDocument%2A> yöntemi.  
  
 [!code-csharp[Trin_CachedDataProtectedDocument#1](../vsto/codesnippet/CSharp/Trin_CachedDataProtectedDocument/ThisDocument.cs#1)]
 [!code-vb[Trin_CachedDataProtectedDocument#1](../vsto/codesnippet/VisualBasic/Trin_CachedDataProtectedDocument/ThisDocument.vb#1)]  
  
### <a name="compile-the-code"></a>Kod derleme  
 Bu kodu ekleyin `ThisDocument` projenizdeki sınıfı. Bu kod, parola adlı bir alanda depolandığını varsayar `securelyStoredPassword`.  
  
## <a name="cache-in-excel-workbooks"></a>Excel çalışma kitaplarını önbelleğe alma  
 Excel projelerinde, kullanarak bir parola ile çalışma kitabı korumaya aldığınızda bu yordam gereklidir <xref:Microsoft.Office.Tools.Excel.Workbook.Protect%2A> yöntemi. Bu yordamı kullanarak yalnızca çalışma belirli bir parolayla korumak durumunda gerekli değildir <xref:Microsoft.Office.Tools.Excel.Worksheet.Protect%2A> yöntemi.  
  
### <a name="to-cache-data-in-an-excel-workbook-that-is-protected-with-a-password"></a>Parola korumalı bir Excel çalışma kitabında verileri önbelleğe almak için  
  
1.  İçinde `ThisWorkbook` sınıf veya biri `Sheet` *n* sınıfları, ortak alan veya özellik önbelleğe alınacak işaretleyin. Daha fazla bilgi için [veriyi önbelleğe alma](../vsto/caching-data.md).  
  
2.  Geçersiz kılma <xref:Microsoft.Office.Tools.Excel.WorkbookBase.UnprotectDocument%2A> yönteminde `ThisWorkbook` sınıfı ve koruma çalışma kitabından kaldırın.  
  
     Çalışma kitabı kaydedildiğinde [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] çalışma kitabının korumasını kaldırmak için bir fırsat vermek için bu yöntemi çağırır. Bu değişikliklerin kaydedilmesi için önbelleğe alınmış verilerin sağlar.  
  
3.  Geçersiz kılma <xref:Microsoft.Office.Tools.Excel.WorkbookBase.ProtectDocument%2A> yönteminde `ThisWorkbook` sınıfı ve belge koruma yeniden uygulayın.  
  
     Çalışma kitabı kaydedildikten sonra [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] çalışma kitabına korumayı uygulamak için bir fırsat vermek için bu yöntemi çağırır.  
  
### <a name="example"></a>Örnek  
 Aşağıdaki kod örneği bir parolayla korunduğu Excel çalışma kitabındaki veriler önbelleğe alınacağını gösterir. Kod koruma kaldırılmadan önce <xref:Microsoft.Office.Tools.Excel.WorkbookBase.UnprotectDocument%2A> yöntemi, geçerli kaydeder <xref:Microsoft.Office.Tools.Excel.Workbook.ProtectStructure%2A> ve <xref:Microsoft.Office.Tools.Excel.Workbook.ProtectWindows%2A> değerleri, böylece koruma aynı tür olarak uygulanabilir <xref:Microsoft.Office.Tools.Excel.WorkbookBase.ProtectDocument%2A> yöntemi.  
  
 [!code-vb[Trin_CachedDataProtectedWorkbook#1](../vsto/codesnippet/VisualBasic/Trin_CachedDataProtectedWorkbook/ThisWorkbook.vb#1)]
 [!code-csharp[Trin_CachedDataProtectedWorkbook#1](../vsto/codesnippet/CSharp/Trin_CachedDataProtectedWorkbook/ThisWorkbook.cs#1)]  
  
### <a name="compile-the-code"></a>Kod derleme  
 Bu kodu ekleyin `ThisWorkbook` projenizdeki sınıfı. Bu kod, parola adlı bir alanda depolandığını varsayar `securelyStoredPassword`.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Verileri önbelleğe](../vsto/caching-data.md)   
 [Nasıl yapılır: Çevrimdışı veya sunucuda kullanmak için verileri önbelleğe](../vsto/how-to-cache-data-for-use-offline-or-on-a-server.md)   
 [Nasıl yapılır: Bir Office belgesi bir veri kaynağını programlamayla önbelleğe alma](../vsto/how-to-programmatically-cache-a-data-source-in-an-office-document.md)  
