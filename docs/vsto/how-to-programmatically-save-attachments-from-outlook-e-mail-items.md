---
title: Ekleri Outlook e-posta öğelerinden program aracılığıyla kaydetme
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- CSharp
helpviewer_keywords:
- Outlook [Office development in Visual Studio], attachments
- e-mail [Office development in Visual Studio], attachments
- saving e-mail attachments
- mail items [Office development in Visual Studio], attachments
- attachments [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: e7e0cff4761b26bac8265592b681d4e56f2ad92f
ms.sourcegitcommit: 7eb2fb21805d92f085126f3a820ac274f2216b4e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/22/2019
ms.locfileid: "67328958"
---
# <a name="how-to-programmatically-save-attachments-from-outlook-email-items"></a>Nasıl yapılır: Ekleri Outlook e-posta öğelerinden program aracılığıyla kaydetme

Bu örnek, posta gelen kutusunda alındığında e-posta eklerini belirli bir klasöre kaydeder.

> [!IMPORTANT]
> Bu örnek adlı bir klasör eklerseniz çalışır **TestFileSave** C dizininin köküne.

[!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek

[!code-csharp[Trin_OL_SaveAttachments#1](../vsto/codesnippet/CSharp/Trin_OL_SaveAttachments/thisaddin.cs#1)]

## <a name="see-also"></a>Ayrıca bkz.

- [Posta öğeleriyle çalışma](../vsto/working-with-mail-items.md)
- [Nasıl yapılır: Program aracılığıyla klasörü ada göre alma](../vsto/how-to-programmatically-retrieve-a-folder-by-name.md)
- [Nasıl yapılır: Bir e-posta iletisi alındığında program aracılığıyla işlem gerçekleştirme](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
- [Nasıl yapılır: Belirli klasör içinde program aracılığıyla arama yapma](../vsto/how-to-programmatically-search-within-a-specific-folder.md)
