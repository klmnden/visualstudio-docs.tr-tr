---
title: "Nasıl Yapılır: Outlook'ta program aracılığıyla öğeleri taşıma"
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- Outlook folders [Office development in Visual Studio], moving items
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload:
- office
ms.openlocfilehash: 51123937fd26b6d6decf3770affd83b1d58d5bfc
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53875747"
---
# <a name="how-to-programmatically-move-items-in-outlook"></a>Nasıl Yapılır: Outlook'ta program aracılığıyla öğeleri taşıma
  Bu örnekte okunmamış e-posta iletileri taşır **gelen** adlı bir klasöre **Test**. Örneğin, yalnızca Word'ün iletileri taşır **Test** içinde `Subject` alan.  
  
 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]  
  
## <a name="example"></a>Örnek  
 [!code-csharp[Trin_OL_MoveItems#1](../vsto/codesnippet/CSharp/Trin_OL_MoveItems/thisaddin.cs#1)]  
  
## <a name="compile-the-code"></a>Kod derleme  
 Bu örnek gerektirir:  
  
-   Adlı bir Outlook e-posta klasörü **Test**.  
  
-   E-posta iletisine word ile ulaşan **Test** içinde `Subject` alan.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [Klasörlerle çalışma](../vsto/working-with-folders.md)   
 [Nasıl yapılır: Program aracılığıyla klasörü ada göre alma](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)   
 [Nasıl yapılır: Belirli klasör içinde program aracılığıyla arama yapma](../vsto/how-to-programmatically-search-within-a-specific-folder.md)   
 [Nasıl yapılır: Bir e-posta iletisi alındığında program aracılığıyla işlem gerçekleştirme](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)  
