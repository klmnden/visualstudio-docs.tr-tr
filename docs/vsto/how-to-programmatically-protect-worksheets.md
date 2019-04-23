---
title: 'Nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- protection, adding to worksheets
- documents [Office development in Visual Studio], document protection
- document protection, adding to worksheets
- worksheets, protecting
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 93acd8466ae90a6db4d1f25d93460e501335af50
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60062223"
---
# <a name="how-to-programmatically-protect-worksheets"></a>Nasıl yapılır: Çalışma sayfalarını program aracılığıyla koruma
  Microsoft Office Excel koruma özelliği, kullanıcıları ve kod çalışma sayfasındaki nesneleri değiştirmesini önlemeye yardımcı olur. Korumayı etkinleştirme sonra varsayılan olarak, tüm hücreler kilitlenir.

 [!INCLUDE[appliesto_xlalldocapp](../vsto/includes/appliesto-xlalldocapp-md.md)]

 Belge düzeyi özelleştirmelerde çalışma sayfalarını Excel Tasarımcısı kullanarak koruyabilirsiniz. Ayrıca çalışma programlı olarak çalışma zamanında herhangi bir proje türünde koruyabilirsiniz.

> [!NOTE]
>  Windows Forms denetimleri için korumalı alanlarına çalışma sayfası eklenemiyor.

## <a name="use-the-designer"></a>Tasarımcısını kullanma

### <a name="to-protect-a-worksheet-in-the-designer"></a>Tasarımcıda bir çalışma sayfasını korumak için

1. İçinde **değişiklikleri** grubunu **gözden geçirme** sekmesinde **koruma sayfası**.

    **Koruma sayfası** iletişim kutusu görüntülenir. Bir parola ayarlamanız ve isteğe bağlı olarak kullanıcıların çalışma sayfası hücreleri biçimlendirme gibi ile gerçekleştirmek veya satır eklemek için izin verilen eylemlerin belirtin.

   Ayrıca, korumalı çalışma sayfalarında belirli aralıkları düzenlenecek kullanıcılar izin verebilirsiniz.

### <a name="to-allow-editing-in-specific-ranges"></a>Belirli aralıkları düzenlemeye izin vermek için

1. İçinde **değişiklikleri** grubunu **gözden geçirme** sekmesini tıklatın, **düzenlemesine izin kullanıcılara**.

     **Düzenlemesine izin kullanıcılara** iletişim kutusu görüntülenir. Bir parola ve parola kullanmadan aralıkları düzenleyebilecek kullanıcıları kullanarak kilitsiz aralıkları belirtebilirsiniz.

## <a name="use-code-at-runtime"></a>Çalışma zamanında kodu kullanın
 Aşağıdaki kod (kullanıcıdan alınan bir parola içeren getPasswordFrom kullanarak) parolayı ayarlar ve yalnızca sıralama sağlar.

### <a name="to-protect-a-worksheet-by-using-code-in-a-document-level-customization"></a>Belge düzeyi özelleştirmesinde kod kullanarak bir çalışma sayfasını korumak için

1. Çağrı <xref:Microsoft.Office.Tools.Excel.Worksheet.Protect%2A> çalışma sayfasının yöntemi. Bu örnek adlı bir çalışma sayfası ile çalıştığını varsayar `Sheet1`.

     [!code-csharp[Trin_VstcoreExcelAutomation#27](../vsto/codesnippet/CSharp/Trin_VstcoreExcelAutomationCS/Sheet1.cs#27)]
     [!code-vb[Trin_VstcoreExcelAutomation#27](../vsto/codesnippet/VisualBasic/Trin_VstcoreExcelAutomation/Sheet1.vb#27)]

### <a name="to-protect-a-worksheet-by-using-code-in-a-vsto-add-in"></a>Bir VSTO eklenti kod kullanarak bir çalışma sayfasını korumak için

1. Çağrı <xref:Microsoft.Office.Interop.Excel._Worksheet.Protect%2A> etkin çalışma sayfasının yöntemi.

     [!code-csharp[Trin_VstcoreExcelAutomationAddIn#17](../vsto/codesnippet/CSharp/trin_vstcoreexcelautomationaddin/ThisAddIn.cs#17)]
     [!code-vb[Trin_VstcoreExcelAutomationAddIn#17](../vsto/codesnippet/VisualBasic/trin_vstcoreexcelautomationaddin/ThisAddIn.vb#17)]

## <a name="see-also"></a>Ayrıca bkz.
- [Çalışma sayfaları ile çalışma](../vsto/working-with-worksheets.md)
- [Nasıl yapılır: Çalışma sayfalarından program aracılığıyla korumayı kaldırma](../vsto/how-to-programmatically-remove-protection-from-worksheets.md)
- [Nasıl yapılır: Çalışma kitaplarını program aracılığıyla koruma](../vsto/how-to-programmatically-protect-workbooks.md)
- [Nasıl yapılır: Çalışma sayfalarını program aracılığıyla gizleme](../vsto/how-to-programmatically-hide-worksheets.md)
- [Konak öğelerine ve denetimlerine genel bakış](../vsto/host-items-and-host-controls-overview.md)
- [Çalışma sayfası konak öğesi](../vsto/worksheet-host-item.md)
- [Office projelerindeki nesnelere genel erişim](../vsto/global-access-to-objects-in-office-projects.md)
- [Office çözümlerinde isteğe bağlı parametreler](../vsto/optional-parameters-in-office-solutions.md)
