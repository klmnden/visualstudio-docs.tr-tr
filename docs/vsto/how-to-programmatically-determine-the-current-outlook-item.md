---
title: 'Nasıl yapılır: Program aracılığıyla geçerli Outlook öğesini belirleme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- mail items [Office development in Visual Studio], current
- e-mail [Office development in Visual Studio], current item
- SelectionChange event
- Outlook [Office development in Visual Studio], current item
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 5566538b428502c8e63e752463b0271daeac2918
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62814960"
---
# <a name="how-to-programmatically-determine-the-current-outlook-item"></a>Nasıl yapılır: Program aracılığıyla geçerli Outlook öğesini belirleme
  Bu örnekte `Explorer.SelectionChange` adı geçerli klasörde ve seçtiğiniz öğe hakkındaki bazı bilgileri görüntülenecek olayı. Kod, daha sonra seçilen öğeyi görüntüler.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-vb[Trin_OL_CurrentItem#1](../vsto/codesnippet/VisualBasic/Trin_OL_CurrentItem/thisaddin.vb#1)]
 [!code-csharp[Trin_OL_CurrentItem#1](../vsto/codesnippet/CSharp/Trin_OL_CurrentItem/thisaddin.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

- Randevu, kişi ve Microsoft Office Outlook'ta e-posta öğeleri.

## <a name="see-also"></a>Ayrıca bkz.
- [Outlook nesne modeline genel bakış](../vsto/outlook-object-model-overview.md)
- [Nasıl yapılır: Program aracılığıyla klasörü ada göre alma](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)
- [Nasıl yapılır: Program aracılığıyla belirli bir kişi arama](../vsto/how-to-programmatically-search-for-a-specific-contact.md)
