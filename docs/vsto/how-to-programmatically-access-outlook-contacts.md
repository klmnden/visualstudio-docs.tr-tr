---
title: 'Nasıl yapılır: Program aracılığıyla Outlook Kişilerine erişme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- contacts [Office development in Visual Studio], searching
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: a9fc9cf214a8aebd663a7de29528790aa3cc0b46
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60104232"
---
# <a name="how-to-programmatically-access-outlook-contacts"></a>Nasıl yapılır: Program aracılığıyla Outlook Kişilerine erişme
  Bu örnekte, son adları belirtilen arama dizesini içeren tüm kişiler bulur.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_AccessContacts#1](../vsto/codesnippet/CSharp/Trin_OL_AccessContacts.trin_ol_accesscontacts/thisaddin.cs#1)]
 [!code-csharp[Trin_OL_AccessContacts#1](../vsto/codesnippet/CSharp/Trin_OL_AccessContacts.trin_ol_accesscontacts/thisaddin.cs#1)]
 [!code-vb[Trin_OL_AccessContacts#1](../vsto/codesnippet/VisualBasic/Trin_OL_AccessContacts/thisaddin.vb#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

- Son adları dizeyi içeren kişiler "**Na"** (örneğin, Tzipi Butnaru) içinde **kişiler** klasör.

## <a name="see-also"></a>Ayrıca bkz.
- [Kişi öğeleriyle çalışma](../vsto/working-with-contact-items.md)
- [Nasıl yapılır: Program aracılığıyla Outlook Kişilerine bir giriş ekleyin](../vsto/how-to-programmatically-add-an-entry-to-outlook-contacts.md)
- [Nasıl yapılır: Program aracılığıyla belirli bir kişi arama](../vsto/how-to-programmatically-search-for-a-specific-contact.md)
- [Nasıl yapılır: Program aracılığıyla bir e-posta adresi arama](../vsto/how-to-programmatically-search-for-an-e-mail-address-in-contacts.md)
- [Nasıl yapılır: Outlook kişilerini program aracılığıyla silme](../vsto/how-to-programmatically-delete-outlook-contacts.md)
