---
title: 'Nasıl yapılır: Gizli modda program aracılığıyla Word iletişim kutuları kullanma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- hidden dialog boxes
- Word [Office development in Visual Studio], dialog boxes
- dialog boxes, hidden mode in Word
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e32c97069e3400b447f8756f9638c9d88d38d99a
ms.sourcegitcommit: e98db44f3a33529b0ba188d24390efd09e548191
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71255842"
---
# <a name="how-to-programmatically-use-word-dialog-boxes-in-hidden-mode"></a>Nasıl yapılır: Gizli modda program aracılığıyla Word iletişim kutuları kullanma
  Microsoft Office Word içindeki yerleşik iletişim kutularını kullanıcıya görüntülemeden çağırarak, tek bir yöntem çağrısıyla karmaşık işlemler gerçekleştirebilirsiniz. Yöntemi çağırmak <xref:Microsoft.Office.Interop.Word.Dialog> <xref:Microsoft.Office.Interop.Word.Dialog.Execute%2A> zorundakalmadannesneyönteminikullanarakbunuyapabilirsiniz<xref:Microsoft.Office.Interop.Word.Dialog.Display%2A> .

 [!INCLUDE[appliesto_wdalldocapp](../vsto/includes/appliesto-wdalldocapp-md.md)]

## <a name="examples"></a>Örnekler
 Aşağıdaki kod örnekleri, Kullanıcı girişi olmadan birden çok sayfa kurulum özelliği ayarlamak için **sayfa yapısı** iletişim kutusunun gizli modda nasıl kullanılacağını göstermektedir. Örnekler özel bir sayfa <xref:Microsoft.Office.Interop.Word.Dialog> boyutunu yapılandırmak için bir nesnesi kullanır. Sayfa kurulumu için, üst kenar boşluğu, alt kenar boşluğu vb. gibi belirli ayarlar <xref:Microsoft.Office.Interop.Word.Dialog> nesnenin geç bağlı özellikleri olarak kullanılabilir. Bu özellikler, çalışma zamanında Word tarafından dinamik olarak oluşturulur.

 Aşağıdaki örnek, **seçeneğinin Strict** olduğu ve öğesini hedefleyen C# [!INCLUDE[net_v40_short](../sharepoint/includes/net-v40-short-md.md)]görsel projelerdeki Visual Basic projelerinde bu görevin nasıl gerçekleştirileceğini gösterir. Bu projelerde Visual Basic ve Visual C# derleyicilerinin geç bağlama özelliklerini kullanabilirsiniz. Bu örneği kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

 [!code-vb[Trin_VstcoreWordAutomation#123](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#123)]
 [!code-csharp[Trin_VstcoreWordAutomation#123](../vsto/codesnippet/CSharp/Trin_VstcoreWordAutomationCS/ThisDocument.cs#123)]

 Aşağıdaki örnek, bu görevin, **seçeneğinin Strict** olduğu Visual Basic projelerinde nasıl gerçekleştirileceğini gösterir. Bu projelerde, geç bağlantılı özelliklere erişmek için yansıma kullanmanız gerekir. Bu örneği kullanmak için, projenizdeki `ThisDocument` veya `ThisAddIn` sınıfından çalıştırın.

 [!code-vb[Trin_VstcoreWordAutomation#104](../vsto/codesnippet/VisualBasic/Trin_VstcoreWordAutomationVB/ThisDocument.vb#104)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Word 'de yerleşik iletişim kutularını program aracılığıyla kullanma](../vsto/how-to-programmatically-use-built-in-dialog-boxes-in-word.md)
- [Word nesne modeline genel bakış](../vsto/word-object-model-overview.md)
- [Office çözümlerinde geç bağlama](../vsto/late-binding-in-office-solutions.md)
- [Yansıma (C#)](/dotnet/csharp/programming-guide/concepts/reflection)
- [Yansıma (Visual Basic)](/dotnet/visual-basic/programming-guide/concepts/reflection)
