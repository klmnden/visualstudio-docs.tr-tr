---
title: 'Nasıl yapılır: Office Çok Dilde Kullanıcı arabirimini hedefleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- globalization [Office development in Visual Studio], user interface targeting
- MUI [Office development in Visual Studio]
- Office applications [Office development in Visual Studio], localization
- Multilingual User Interface [Office development in Visual Studio]
- localization [Office development in Visual Studio], user interface targeting
- Office applications [Office development in Visual Studio], globalization
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: c495f8a83b58c53404056befd2227b295c3324d5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62961145"
---
# <a name="how-to-target-the-office-multilingual-user-interface"></a>Nasıl yapılır: Office Çok Dilde Kullanıcı arabirimini hedefleme
  Çok dilli kullanıcı arabirimi (MUI) son kullanıcı kullanıcı arabirimini (UI) dilini değiştirme olanağı sunan bir Microsoft Office özelliğidir. Örneğin, İngilizce bir kullanıcı Arabirimi ile çalışan bir son kullanıcı, kullanıcı Arabirimi dili İspanyolca için değiştirebilirsiniz.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

 Uygulamanızı Office birçok dil kullanan kişiler tarafından kullanılacaksa, dili, kullanıcı Arabirimi dizeleri (kullanıcının yüklü doğru kaynakları varsa) kullanıcının bilgisayarında Office tarafından kullanılan dil eşleşecek şekilde otomatik olarak değiştirmek için kod ekleyebilirsiniz.

## <a name="to-check-the-current-office-ui-setting"></a>Geçerli Office UI ayarı denetlemek için

1. Kullanım <xref:System.Threading.Thread.CurrentUICulture%2A> geçerli iş parçacığının özelliği. Dili, kullanıcı Arabirimi dizeleri kullanıcının bilgisayarında şu anda çalışan bir Office sürümü tarafından kullanılan dil eşleşecek şekilde ayarlayın.

     [!code-vb[Trin_VstcoreCreatingExcel#10](../vsto/codesnippet/VisualBasic/Trin_VstcoreCreatingExcelVB/Sheet1.vb#10)]
     [!code-csharp[Trin_VstcoreCreatingExcel#10](../vsto/codesnippet/CSharp/Trin_VstcoreCreatingExcelCS/Sheet1.cs#10)]

## <a name="see-also"></a>Ayrıca bkz.
- [Nasıl yapılır: Birincil birlikte çalışma derlemeleriyle Office uygulamalarını hedefleme](../vsto/how-to-target-office-applications-through-primary-interop-assemblies.md)
- [Office çözümlerinde geç bağlama](../vsto/late-binding-in-office-solutions.md)
