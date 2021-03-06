---
title: 'Nasıl yapılır: Program aracılığıyla e-posta gönder'
ms.date: 08/14/2019
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
ms.openlocfilehash: 72d033add2ba8320b14eebd5af700ab225d34410
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69551759"
---
# <a name="how-to-programmatically-send-email"></a>Nasıl yapılır: Program aracılığıyla e-posta gönder
  Bu örnek, e-posta adreslerinde **example.com** etki alanı adına sahip kişilere bir e-posta iletisi gönderir.

 [!INCLUDE[appliesto_olkallapp](../vsto/includes/appliesto-olkallapp-md.md)]

[!include[Add-ins note](includes/addinsnote.md)]

## <a name="example"></a>Örnek
 [!code-csharp[Trin_OL_ProgramEmail#1](../vsto/codesnippet/CSharp/Trin_OL_ProgramEMail/thisaddin.cs#1)]

## <a name="compile-the-code"></a>Kod derleme
 Bu örnek şunları gerektirir:

- **Example.com** etki alanı adına sahip kişiler, e-posta adresleridir.

## <a name="robust-programming"></a>Güçlü programlama
 **Example.com**etki alanı adını arayan filtre kodunu kaldırmayın. Filtreyi kaldırırsanız çözümünüz tüm kişilerinize e-posta iletileri gönderir.

## <a name="see-also"></a>Ayrıca bkz.
- [Posta öğeleriyle çalışma](../vsto/working-with-mail-items.md)
- [Nasıl yapılır: Program aracılığıyla e-posta öğesi oluşturma](../vsto/how-to-programmatically-create-an-e-mail-item.md)
- [Nasıl yapılır: Program aracılığıyla Outlook kişilerine erişme](../vsto/how-to-programmatically-access-outlook-contacts.md)
- [Nasıl yapılır: Bir e-posta iletisi alındığında program aracılığıyla işlem gerçekleştirme](../vsto/how-to-programmatically-perform-actions-when-an-e-mail-message-is-received.md)
