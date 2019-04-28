---
title: 'Nasıl yapılır: Program aracılığıyla web sayfasını Outlook klasörüyle ilişkilendirme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- folders [Office development in Visual Studio], Web pages and
- Outlook [Office development in Visual Studio], Web pages attached to folders
- Web pages [Office development in Visual Studio], Outlook folders
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e83f8b7f6bcdb790b5e545aa76426bc05f0735f5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62817315"
---
# <a name="how-to-programmatically-associate-a-web-page-with-an-outlook-folder"></a>Nasıl yapılır: Program aracılığıyla web sayfasını Outlook klasörüyle ilişkilendirme
  Bu örnek adlı bir klasör için denetler `HtmlView` Microsoft Office Outlook'ta. Klasör mevcut değilse, kod klasörü oluşturur ve bir Web sayfası atar. Klasör varsa, kod klasör içeriğini görüntüler.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_HTMLFolder#1](../vsto/codesnippet/CSharp/Trin_OL_HTMLFolder/thisaddin.cs#1)]

## <a name="see-also"></a>Ayrıca bkz.
- [Klasörlerle çalışma](../vsto/working-with-folders.md)
- [Nasıl yapılır: Program aracılığıyla klasörü ada göre alma](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)
- [Nasıl yapılır: Program aracılığıyla özel klasör öğeleri oluşturma](../vsto/how-to-programmatically-create-custom-folder-items.md)
