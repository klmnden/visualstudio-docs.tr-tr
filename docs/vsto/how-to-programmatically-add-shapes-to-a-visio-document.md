---
title: 'Nasıl yapılır: Visio belgesine program aracılığıyla şekiller ekleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Visio [Office development in Visual Studio], adding Visio shapes
- shapes [Office development in Visual Studio], adding Visio shapes
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 1abc85ade942a0f9d8f88322f1117f32c94bd258
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56644477"
---
# <a name="how-to-programmatically-add-shapes-to-a-visio-document"></a>Nasıl yapılır: Visio belgesine program aracılığıyla şekiller ekleme
  Microsoft Office Visio belgesine şekiller, asıl kalıptan alma ve etkin sayfada şekilleri bırakarak ekleyebilirsiniz.

 Daha fazla bilgi için bkz: VBA başvuru belgelerine [Microsoft.Office.Interop.Visio.Documents.Add](/office/vba/api/Visio.Documents.Add) yöntemi [Microsoft.Office.Interop.Visio.Application.ActivePage](/office/vba/api/Visio.Application.ActivePage) özelliği ve [Microsoft.Office.Interop.Visio.Page.Drop](/office/vba/api/Visio.Page.Drop) yöntemi.

## <a name="add-shapes-to-a-visio-document"></a>Bir Visio belgesine şekiller ekleme

### <a name="to-add-shapes-to-a-visio-document"></a>Visio belgesine şekilleri eklemek için

-   Etkin belge, asıl Documents.Masters koleksiyondan ve şekiller etkin belgede bırakın. Bir ana dizin veya ana adı kullanarak alabilirsiniz.

     Aşağıdaki kod örneği boş bir Visio belgesi oluşturur ve sonra açıyor **temel şekilleri** yerleşik bir şablon. Kod birkaç şekil alır ve bunları etkin sayfada bırakır.

     [!code-csharp[Trin_VstcoreVisioAutomationAddIn#13](../vsto/codesnippet/CSharp/trin_vstcorevisioautomationaddin/ThisAddIn.cs#13)]
     [!code-vb[Trin_VstcoreVisioAutomationAddIn#13](../vsto/codesnippet/VisualBasic/trin_vstcorevisioautomationaddin/ThisAddIn.vb#13)]

## <a name="see-also"></a>Ayrıca bkz.
- [Visio çözümleri](../vsto/visio-solutions.md)
- [Visio nesne modeline genel bakış](../vsto/visio-object-model-overview.md)
- [Visio şekilleri ile çalışma](../vsto/working-with-visio-shapes.md)
- [Nasıl yapılır: Program aracılığıyla kopyalayın ve bir Visio belgesinde şekiller yapıştırın](../vsto/how-to-programmatically-copy-and-paste-shapes-in-a-visio-document.md)
