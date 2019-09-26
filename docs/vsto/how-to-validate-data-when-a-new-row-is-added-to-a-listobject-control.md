---
title: ListObject denetimine yeni satır eklendiğinde verileri doğrula
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
ms.openlocfilehash: f65bbc374c1d0ec2a940ff98fcc6f04e5391b2db
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255678"
---
# <a name="how-to-validate-data-when-a-new-row-is-added-to-a-listobject-control"></a>Nasıl yapılır: ListObject denetimine yeni bir satır eklendiğinde verileri doğrulama
  Kullanıcılar, verilere bağlanan bir <xref:Microsoft.Office.Tools.Excel.ListObject> denetime yeni satırlar ekleyebilir. Veri kaynağına değişiklikleri uygulamadan önce kullanıcının verilerini doğrulayabilirsiniz.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

## <a name="data-validation"></a>Veri doğrulama
 <xref:Microsoft.Office.Tools.Excel.ListObject> Veriye<xref:Microsoft.Office.Tools.Excel.ListObject.BeforeAddDataBoundRow> bağlanan bir satır öğesine her eklendiğinde olay tetiklenir. Bu olayı, veri doğrulamayı gerçekleştirmek için işleyebilirsiniz. Örneğin, uygulamanız yalnızca 18 yaş ve 65 yaşar arasındaki çalışanların veri kaynağına eklenebildiğini gerektiriyorsa, girilen yaş satırı, satır eklenmeden önce bu aralıkta yer aldığından emin olun.

> [!NOTE]
> İstemciye ek olarak sunucu üzerinde kullanıcı girişini her zaman denetlemeniz gerekir. Daha fazla bilgi için bkz. [güvenli istemci uygulamaları](/dotnet/framework/data/adonet/secure-client-applications).

### <a name="to-validate-data-when-a-new-row-is-added-to-data-bound-listobject"></a>Veri bağlantılı ListObject 'e yeni bir satır eklendiğinde verileri doğrulamak için

1. Kimliği ve <xref:System.Data.DataTable> sınıf düzeyinde değişken oluşturun.

     [!code-csharp[Trin_VstcoreHostControlsExcel#8](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#8)]
     [!code-vb[Trin_VstcoreHostControlsExcel#8](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#8)]

2. Yeni <xref:System.Data.DataTable> bir oluşturun ve `Sheet1` sınıfın `Startup` olay işleyicisine (belge düzeyi projesinde) veya `ThisAddIn` sınıfa (VSTO eklenti projesinde) örnek sütunlar ve veriler ekleyin.

     [!code-csharp[Trin_VstcoreHostControlsExcel#9](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#9)]
     [!code-vb[Trin_VstcoreHostControlsExcel#9](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#9)]

3. Girilen yaş kabul edilebilir `list1_BeforeAddDataBoundRow` Aralık dahilinde olup olmadığını denetlemek için olay işleyicisine kod ekleyin.

     [!code-csharp[Trin_VstcoreHostControlsExcel#10](../vsto/codesnippet/CSharp/Trin_VstcoreHostControlsExcelCS/Sheet1.cs#10)]
     [!code-vb[Trin_VstcoreHostControlsExcel#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreHostControlsExcelVB/Sheet1.vb#10)]

## <a name="compile-the-code"></a>Kod derleme
 Bu kod örneği, bu kodun göründüğü çalışma sayfasında <xref:Microsoft.Office.Tools.Excel.ListObject> var `list1` olan bir ada sahip olduğunuzu varsayar.

## <a name="see-also"></a>Ayrıca bkz.
- [VSTO Eklentilerindeki Word belgelerini ve Excel çalışma kitaplarını çalışma zamanında genişletme](../vsto/extending-word-documents-and-excel-workbooks-in-vsto-add-ins-at-run-time.md)
- [Office belgelerindeki denetimler](../vsto/controls-on-office-documents.md)
- [Çalışma zamanında Office belgelerine denetim ekleme](../vsto/adding-controls-to-office-documents-at-run-time.md)
- [ListObject denetimi](../vsto/listobject-control.md)
- [Genişletilmiş nesneleri kullanarak Excel'i otomatikleştirmek](../vsto/automating-excel-by-using-extended-objects.md)
- [Nasıl yapılır: ListObject sütunlarını verilerle eşleme](../vsto/how-to-map-listobject-columns-to-data.md)
