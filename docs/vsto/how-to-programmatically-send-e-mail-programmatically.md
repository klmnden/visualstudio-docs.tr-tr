---
title: 'Nasıl yapılır: Program aracılığıyla e-posta gönderme'
ms.date: 02/02/2017
ms.topic: conceptual
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- mail items [Office development in Visual Studio], sending e-mail
- Outlook [Office development in Visual Studio], creating e-mail
- Outlook [Office development in Visual Studio], sending e-mail
- e-mail [Office development in Visual Studio], sending
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 280b4f526bad3e0ba646058b3e2410a98ca910fe
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56646011"
---
# <a name="how-to-programmatically-send-email"></a>Nasıl yapılır: Program aracılığıyla e-posta gönderme
  Bu örnekte, etki alanı adına sahip kişilere bir e-posta iletisi gönderilir **example.com** kendi e-posta adresleri.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_ProgramEmail#1](../vsto/codesnippet/CSharp/Trin_OL_ProgramEMail/thisaddin.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek gerektirir:

-   Etki alanı adına sahip kişiler **example.com** kendi e-posta adresleri.

## <a name="robust-programming"></a>Güçlü programlama
 Etki alanı adını arar filtreleme kodunu kaldırmayın **example.com**. Filtreyi kaldırmanız durumunda, çözümünüzün, tüm kişilere e-posta iletilerini gönderir.

## <a name="see-also"></a>Ayrıca bkz.
- [Posta öğeleriyle çalışma](../vsto/working-with-mail-items.md)
- [Nasıl yapılır: Program aracılığıyla bir e-posta öğesi oluşturma](../vsto/how-to-programmatically-create-an-e-mail-item.md)
- [Nasıl yapılır: Program aracılığıyla Outlook Kişilerine erişme](../vsto/how-to-programmatically-access-outlook-contacts.md)
- [Nasıl yapılır: Bir e-posta iletisi alındığında program aracılığıyla işlem gerçekleştirme](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
