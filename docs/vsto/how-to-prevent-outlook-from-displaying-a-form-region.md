---
title: "Nasıl yapılır: Outlook'un form bölgesini görüntülemesini engelleme"
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- form regions [Office development in Visual Studio], canceling display
- canceling form region display
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: ad17041650324e597fb76925f521bb7fc2e9ce93
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62967663"
---
# <a name="how-to-prevent-outlook-from-displaying-a-form-region"></a>Nasıl yapılır: Outlook'un form bölgesini görüntülemesini engelleme
  Microsoft Office Outlook, belirli bir öğe için bir form bölgesinin istemediğiniz durumlar olabilir. Örneğin, bir kişi öğesi bir iş adresi içermiyorsa görüntülenmesini bir eşlem içindeki iş konumunu gösteren bir form bölgesi engelleyebilirsiniz.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="to-prevent-outlook-from-displaying-a-form-region"></a>Outlook'un form bölgesini görüntülemesini engelleme için

1. Değiştirmek istediğiniz form bölgesi için kod dosyasını açın.

2. Genişletin **Form bölgesi fabrikası** kod bölge.

3. Kodu `FormRegionInitializing` ayarlar olay işleyicisi <xref:System.ComponentModel.CancelEventArgs.Cancel%2A> özelliği <xref:Microsoft.Office.Tools.Outlook.FormRegionInitializingEventArgs> sınıfının **true**.

   Bu örnekte, kişi öğesi bir adresi içermiyorsa <xref:System.ComponentModel.CancelEventArgs.Cancel%2A> özelliği **true**, ve form bölgesi görünmez.

## <a name="example"></a>Örnek
 [!code-csharp[Trin_Outlook_FR_Separate#1](../vsto/codesnippet/CSharp/Trin_Outlook_FR_Separate_O12/MapIt.cs#1)]
 [!code-vb[Trin_Outlook_FR_Separate#1](../vsto/codesnippet/VisualBasic/Trin_Outlook_FR_Separate_O12/MapIt.vb#1)]

## <a name="see-also"></a>Ayrıca bkz.
- [Outlook form bölgeleri oluşturma](../vsto/creating-outlook-form-regions.md)
- [İzlenecek yol: Outlook form bölgesi tasarlama](../vsto/walkthrough-designing-an-outlook-form-region.md)
- [Nasıl yapılır: Bir Outlook eklenti projesine form bölgesi ekleme](../vsto/how-to-add-a-form-region-to-an-outlook-add-in-project.md)
- [İzlenecek yol: Outlook form bölgesi tasarlama](../vsto/walkthrough-designing-an-outlook-form-region.md)
- [İzlenecek yol: Outlook'ta tasarlanan form bölgesini içeri aktarma](../vsto/walkthrough-importing-a-form-region-that-is-designed-in-outlook.md)
