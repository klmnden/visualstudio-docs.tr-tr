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
ms.openlocfilehash: 3dcbfbe7b6e6ac5bacb9e8e36e43d780d3051903
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60108977"
---
# <a name="how-to-programmatically-move-items-in-outlook"></a>Nasıl yapılır: Outlook'ta program aracılığıyla öğeleri taşıma
  Bu örnekte okunmamış e-posta iletileri taşır **gelen** adlı bir klasöre **Test**. Örneğin, yalnızca Word'ün iletileri taşır **Test** içinde `Subject` alan.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_MoveItems#1](../vsto/codesnippet/CSharp/Trin_OL_MoveItems/thisaddin.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

- Adlı bir Outlook e-posta klasörü **Test**.

- E-posta iletisine word ile ulaşan **Test** içinde `Subject` alan.

## <a name="see-also"></a>Ayrıca bkz.
- [Klasörlerle çalışma](../vsto/working-with-folders.md)
- [Nasıl yapılır: Program aracılığıyla klasörü ada göre alma](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)
- [Nasıl yapılır: Belirli klasör içinde program aracılığıyla arama yapma](../vsto/how-to-programmatically-search-within-a-specific-folder.md)
- [Nasıl yapılır: Bir e-posta iletisi alındığında program aracılığıyla işlem gerçekleştirme](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
