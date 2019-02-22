---
title: 'Nasıl yapılır: Program aracılığıyla bir e-posta adresi arama'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- e-mail [Office development in Visual Studio], searching
- contacts [Office development in Visual Studio], searching
- searching contacts
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: b6b29e46a61a46ae5e986dec7b14733e3807064b
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56615500"
---
# <a name="how-to-programmatically-search-for-an-email-address-in-contacts"></a>Nasıl yapılır: Program aracılığıyla bir e-posta adresi arama
  Bu örnekte, etki alanı adına sahip kişiler için kişi bir klasör arama **example.com** kendi e-posta adresleri.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_SearchEmail#1](../vsto/codesnippet/CSharp/Trin_OL_SearchEmail/thisaddin.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

-   Etki alanı adına sahip kişiler **example.com** e-posta (örneğin, `somebody@example.com`), ve ilk ve son adları vardır.

## <a name="see-also"></a>Ayrıca bkz.
- [Kişi öğeleriyle çalışma](../vsto/working-with-contact-items.md)
- [Nasıl yapılır: Program aracılığıyla e-posta gönderme](../vsto/how-to-programmatically-send-e-mail-programmatically.md)
- [Nasıl yapılır: Program aracılığıyla Outlook Kişilerine erişme](../vsto/how-to-programmatically-access-outlook-contacts.md)
- [Nasıl yapılır: Program aracılığıyla Outlook Kişilerine bir giriş ekleyin](../vsto/how-to-programmatically-add-an-entry-to-outlook-contacts.md)
