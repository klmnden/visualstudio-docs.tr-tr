---
title: 'Nasıl yapılır: ListObject denetimine yeni bir satır eklendiğinde verileri doğrulama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- controls [Office development in Visual Studio], validating data
- ListObject control, new row
- ListObject control, validating data
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a78674a0738c0b7a0f69e04decd70fbbf1d1e367
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56615864"
---
# <a name="how-to-validate-data-when-a-new-row-is-added-to-a-listobject-control"></a>Nasıl yapılır: ListObject denetimine yeni bir satır eklendiğinde verileri doğrulama
  Kullanıcı için yeni satır ekleme bir <xref:Microsoft.Office.Tools.Excel.ListObject> veriye bağlı denetim. Veri kaynağına değişiklikler yapmadan önce kullanıcının verileri doğrulayabilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="data-validation"></a>Veri doğrulama
 Her bir satır eklendiğinde bir <xref:Microsoft.Office.Tools.Excel.ListObject> verilere bağlı <xref:Microsoft.Office.Tools.Excel.ListObject.BeforeAddDataBoundRow> olayı oluşturulur. Veri doğrulama gerçekleştirmek için bu olay işleyebilir. Örneğin, uygulamanız yalnızca çalışanlar 18 yaş ve 65 arasında veri kaynağına eklenebilir gerektiriyorsa, satır eklenmeden önce girilen yaş, aralığa denk gelen doğrulayın.

> [!NOTE]
>  Her zaman, sunucunun istemci yanı sıra kullanıcı girdisi denetlemeniz gerekir. Daha fazla bilgi için [güvenli istemci uygulamaları](/dotnet/framework/data/adonet/secure-client-applications).

### <a name="to-validate-data-when-a-new-row-is-added-to-data-bound-listobject"></a>Veri ListObject denetimine yeni bir satır verileri doğrulamak için eklendi

1.  Değişkenleri Kimliğini oluşturma ve <xref:System.Data.DataTable> sınıf düzeyinde.

     [!code-csharp[Trin_VstcoreHostControlsExcel#8](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#8)]
     [!code-vb[Trin_VstcoreHostControlsExcel#8](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#8)]

2.  Yeni bir <xref:System.Data.DataTable> ve örnek sütunlar ekleyip verileri `Startup` olay işleyicisine `Sheet1` sınıfı (belge düzeyi projede) veya `ThisAddIn` (bir VSTO eklenti projesinde sınıftaki).

     [!code-csharp[Trin_VstcoreHostControlsExcel#9](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#9)]
     [!code-vb[Trin_VstcoreHostControlsExcel#9](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#9)]

3.  Kodu `list1_BeforeAddDataBoundRow` girilen yaş kabul edilebilir aralık içinde olup olmadığını denetlemek için olay işleyicisi.

     [!code-csharp[Trin_VstcoreHostControlsExcel#10](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#10)]
     [!code-vb[Trin_VstcoreHostControlsExcel#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#10)]

## <a name="compile-the-code"></a>Kod derleme
 Bu kod örneği, mevcut bir sahibi olduğunuzu varsayar <xref:Microsoft.Office.Tools.Excel.ListObject> adlı `list1` bu kodu göründüğü çalışma.

## <a name="see-also"></a>Ayrıca bkz.
- [Word belgelerini ve Excel çalışma kitaplarını VSTO eklentileri çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Office belgelerine çalışma zamanında denetimler ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [ListObject denetimi](../vsto/listobject-control.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Nasıl yapılır: ListObject sütunlarıyla verileri eşleme](../vsto/how-to-map-listobject-columns-to-data.md)
