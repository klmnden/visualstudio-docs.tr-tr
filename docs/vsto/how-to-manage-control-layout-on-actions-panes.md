---
title: 'Nasıl yapılır: Eylemler bölmelerindeki Düzen denetim yönetme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- actions panes [Office development in Visual Studio], control layout
- controls [Office development in Visual Studio], layout on actions panes
- smart documents [Office development in Visual Studio], control layout
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 94e3ccc30507ccd7995c4d4fad548fe5ff425365
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60094620"
---
# <a name="how-to-manage-control-layout-on-actions-panes"></a>Nasıl yapılır: Eylemler bölmelerindeki Düzen denetim yönetme
  Eylemler bölmesi varsayılan belge veya çalışma sağa yerleştirilir; Ancak, sol, üst veya alt yerleştirilmiş olabilir. Birden çok kullanıcı denetimleri kullanıyorsanız, Eylemler bölmesinde kullanıcı denetimleri düzgün yığın için kod yazabilirsiniz. Daha fazla bilgi için [Eylemler bölmesine genel bakış](../vsto/actions-pane-overview.md).

 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]

 Eylemler bölmesinde yatay veya dikey olarak yerleştirilmiş üzerinde denetimleri yığın sırasını bağlıdır.

> [!NOTE]
>  Kullanıcının çalışma zamanında eylemler bölmesinde yeniden boyutlandırırsa, Eylemler bölmesi için denetimleri ayarlayabilirsiniz. Kullanabileceğiniz <xref:System.Windows.Forms.Control.Anchor%2A> eylemler bölmesindeki denetimlere bağlantı için bir Windows Forms denetiminin özelliği. Daha fazla bilgi için [nasıl yapılır: Windows formlarında denetimleri sabitleme](/dotnet/framework/winforms/controls/how-to-anchor-controls-on-windows-forms).

> [!NOTE]
>  Bilgisayarınız, aşağıdaki yönergelerde yer alan Visual Studio kullanıcı arabirimi öğelerinden bazıları için farklı adlar veya konumlar gösterebilir. Sahip olduğunuz Visual Studio sürümü ve kullandığınız ayarlar bu öğeleri belirler. Daha fazla bilgi için [Visual Studio IDE'yi kişiselleştirme](../ide/personalizing-the-visual-studio-ide.md).

## <a name="to-set-the-stack-order-of-the-actions-pane-controls"></a>Eylemler bölmesi denetimlerinin yığın sırasını ayarlamak için

1. Eylemler bölmesi ile birden çok kullanıcı veya iç içe geçmiş eylemler bölmesinde denetimleri içeren bir Microsoft Office Word için belge düzeyi projesi açın. Daha fazla bilgi için [nasıl yapılır: Eylemler bölmesi ekleme Word belgelerine veya Excel çalışma kitapları](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md).

2. Sağ **ThisDocument.vb** veya **ThisDocument.vb** içinde **Çözüm Gezgini** ve ardından **Kodu Görüntüle**.

3. İçinde <xref:Microsoft.Office.Tools.ActionsPane.OrientationChanged> olay işleyicisi, Eylemler bölmesi, Eylemler bölmesinde'nın yönünü yatay olup olmadığını denetleyin.

     [!code-csharp[Trin_VstcoreActionsPaneWord#30](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/ThisDocument.cs#30)]
     [!code-vb[Trin_VstcoreActionsPaneWord#30](../vsto/codesnippet/VisualBasic/Trin_VstcoreActionsPaneWordVB/ThisDocument.vb#30)]

4. Yönünü yatay ise, yığın Eylem Bölmesi Sol taraftan denetler; Aksi takdirde, bunları üstünden yığın.

     [!code-csharp[Trin_VstcoreActionsPaneWord#31](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/ThisDocument.cs#31)]
     [!code-vb[Trin_VstcoreActionsPaneWord#31](../vsto/codesnippet/VisualBasic/Trin_VstcoreActionsPaneWordVB/ThisDocument.vb#31)]

5. İçinde C#, bir olay işleyicisi için eklemelisiniz `ActionsPane` için <xref:Microsoft.Office.Tools.Word.Document.Startup> olay işleyicisi. Olay işleyicileri oluşturma hakkında daha fazla bilgi için bkz: [nasıl yapılır: Office projelerinde olay işleyicileri oluşturma](../vsto/how-to-create-event-handlers-in-office-projects.md).

     [!code-csharp[Trin_VstcoreActionsPaneWord#32](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/ThisDocument.cs#32)]

6. Projeyi çalıştırmak ve Eylemler bölmesinde denetimler soldan sağa Eylemler bölmesinde, belgenin üst kısmında yerleştirilir ve Eylemler bölmesinde belgenin sağ tarafa yerleştirildiğinde denetimleri üstten alta Yığılmış yığınlandığını doğrulayın.

## <a name="example"></a>Örnek
 [!code-csharp[Trin_VstcoreActionsPaneWord#29](../vsto/codesnippet/CSharp/Trin_VstcoreActionsPaneWordCS/ThisDocument.cs#29)]
 [!code-vb[Trin_VstcoreActionsPaneWord#29](../vsto/codesnippet/VisualBasic/Trin_VstcoreActionsPaneWordVB/ThisDocument.vb#29)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

- Word belge düzeyi projesi birden fazla kullanıcı denetimleri içeren eylemler bölmesi veya iç içe geçmiş eylemler bölmesinde denetler.

## <a name="see-also"></a>Ayrıca bkz.
- [Eylemler bölmesine genel bakış](../vsto/actions-pane-overview.md)
- [Nasıl yapılır: Word belgelerine veya Excel çalışma kitaplarına Eylemler bölmesi ekleme](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md)
- [Nasıl yapılır: Word belgelerine veya Excel çalışma kitaplarına Eylemler bölmesi ekleme](../vsto/how-to-add-an-actions-pane-to-word-documents-or-excel-workbooks.md)
- [İzlenecek yol: Eylemler bölmesinden belgeye metin ekleme](../vsto/walkthrough-inserting-text-into-a-document-from-an-actions-pane.md)
- [İzlenecek yol: Eylemler bölmesinden belgeye metin ekleme](../vsto/walkthrough-inserting-text-into-a-document-from-an-actions-pane.md)
