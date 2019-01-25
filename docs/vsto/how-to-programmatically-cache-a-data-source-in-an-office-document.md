---
title: 'Nasıl yapılır: Bir Office belgesi bir veri kaynağını programlamayla önbelleğe alma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Office applications [Office development in Visual Studio], data
- datasets [Office development in Visual Studio], caching
- StartCaching method
- data caching [Office development in Visual Studio], programmatically
- data [Office development in Visual Studio], caching
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a2338e2402167987767ac5c9527113c4b0ff81d6
ms.sourcegitcommit: c0202a77d4dc562cdc55dc2e6223c062281d9749
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/24/2019
ms.locfileid: "54867331"
---
# <a name="how-to-programmatically-cache-a-data-source-in-an-office-document"></a>Nasıl yapılır: Bir Office belgesi bir veri kaynağını programlamayla önbelleğe alma
  Program aracılığıyla bir veri nesnesi bir belgedeki veri önbelleğini çağırarak ekleyebileceğiniz `StartCaching` gibi bir konak yöntemi öğesi bir <xref:Microsoft.Office.Tools.Word.Document>, <xref:Microsoft.Office.Tools.Excel.Workbook>, veya <xref:Microsoft.Office.Tools.Excel.Worksheet>. Bir veri nesnesi çağırarak verileri önbellekten kaldırma `StopCaching` konak öğesinin yöntemi.

 `StartCaching` Yöntemi ve `StopCaching` yöntemi hem de özel olan, ancak bunlar Intellisense'te görünür.

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Kullanırken `StartCaching` veri nesnesinin veri önbelleğini bir veri nesnesi ekleme yöntemi ile bildirilen gerekmez <xref:Microsoft.VisualStudio.Tools.Applications.Runtime.CachedAttribute> özniteliği. Ancak, veri nesnesi, verileri önbelleğe eklenecek belirli gereksinimleri karşılaması gerekir. Daha fazla bilgi için [veriyi önbelleğe alma](../vsto/caching-data.md).

## <a name="to-programmatically-cache-a-data-object"></a>Program aracılığıyla bir veri nesnesini önbelleğe almak için

1.  Yöntemin içinde değil sınıf düzeyinde veri nesnesi bildirir. Bu örnek, bildirdiğiniz varsayar bir <xref:System.Data.DataSet> adlı `dataSet1` programlı olarak önbelleğe almak istediğiniz.

     [!code-csharp[Trin_VstcoreDataExcel#12](../vsto/codesnippet/CSharp/Trin_VstcoreDataExcelCS/Sheet1.cs#12)]
     [!code-vb[Trin_VstcoreDataExcel#12](../vsto/codesnippet/VisualBasic/Trin_VstcoreDataExcelVB/Sheet1.vb#12)]

2.  Veri nesnesi örneği oluşturun ve sonra çağrı `StartCaching` yöntemi oluşturdular. veri nesnesinin ve belge veya çalışma sayfası örneği.

     [!code-csharp[Trin_VstcoreDataExcel#13](../vsto/codesnippet/CSharp/Trin_VstcoreDataExcelCS/Sheet1.cs#13)]
     [!code-vb[Trin_VstcoreDataExcel#13](../vsto/codesnippet/VisualBasic/Trin_VstcoreDataExcelVB/Sheet1.vb#13)]

## <a name="to-stop-caching-a-data-object"></a>Bir veri nesnesini önbelleğe almayı durdurmak için

1.  Çağrı `StopCaching` yöntemi oluşturdular. veri nesnesinin ve belge veya çalışma sayfası örneği. Bu örnekte, sahibi olduğunuzu varsayar bir <xref:System.Data.DataSet> adlı `dataSet1` önbelleğe almayı durdurmak istediğiniz.

     [!code-csharp[Trin_VstcoreDataExcel#14](../vsto/codesnippet/CSharp/Trin_VstcoreDataExcelCS/Sheet1.cs#14)]
     [!code-vb[Trin_VstcoreDataExcel#14](../vsto/codesnippet/VisualBasic/Trin_VstcoreDataExcelVB/Sheet1.vb#14)]

    > [!NOTE]
    >  Çağırmayın `StopCaching` için olay işleyicisinden `Shutdown` belge veya çalışma olayı. Zamana göre `Shutdown` olayı oluşturulur, bu veri önbelleğini değiştirmek için çok geç olur. Hakkında daha fazla bilgi için `Shutdown` olay bkz [Office Projelerindeki Olaylar](../vsto/events-in-office-projects.md).

## <a name="see-also"></a>Ayrıca bkz.

- [Verileri önbelleğe](../vsto/caching-data.md)
- [Nasıl yapılır: Çevrimdışı veya sunucuda kullanmak için verileri önbelleğe](../vsto/how-to-cache-data-for-use-offline-or-on-a-server.md)
- [Nasıl yapılır: Bir parola korumalı belgede veriyi önbelleğe alma](../vsto/how-to-cache-data-in-a-password-protected-document.md)
- [Sunucudaki belgelerde verilere](../vsto/accessing-data-in-documents-on-the-server.md)
- [Verileri kaydetme](../data-tools/saving-data.md)
