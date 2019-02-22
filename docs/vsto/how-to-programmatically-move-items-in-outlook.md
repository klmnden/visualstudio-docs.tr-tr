---
title: "Nasıl yapılır: Outlook'ta program aracılığıyla öğeleri taşıma"
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Outlook folders [Office development in Visual Studio], moving items
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 10b0f05e758f71830d5377c738ff9dee683022b8
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641630"
---
# <a name="how-to-programmatically-move-items-in-outlook"></a>Nasıl yapılır: Outlook'ta program aracılığıyla öğeleri taşıma
  Bu örnekte okunmamış e-posta iletileri taşır **gelen** adlı bir klasöre **Test**. Örneğin, yalnızca Word'ün iletileri taşır **Test** içinde `Subject` alan.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_MoveItems#1](../vsto/codesnippet/CSharp/Trin_OL_MoveItems/thisaddin.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

-   Adlı bir Outlook e-posta klasörü **Test**.

-   E-posta iletisine word ile ulaşan **Test** içinde `Subject` alan.

## <a name="see-also"></a>Ayrıca bkz.
- [Klasörlerle çalışma](../vsto/working-with-folders.md)
- [Nasıl yapılır: Program aracılığıyla klasörü ada göre alma](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)
- [Nasıl yapılır: Belirli klasör içinde program aracılığıyla arama yapma](../vsto/how-to-programmatically-search-within-a-specific-folder.md)
- [Nasıl yapılır: Bir e-posta iletisi alındığında program aracılığıyla işlem gerçekleştirme](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
