---
title: 'Nasıl yapılır: İçeri aktarmalar Tasarımcısını kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-workflow-designer
ms.topic: reference
f1_keywords:
- System.Activities.Presentation.View.ImportDesigner.UI
ms.assetid: 61328ab6-9b66-4e12-8630-22e30ee8c9d1
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f1c305129a7f46c8d1841f28d8084535ec7e4d9f
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60077582"
---
# <a name="how-to-use-the-imports-designer"></a>Nasıl yapılır: İçeri Aktarmalar Tasarımcısını Kullanma
İçe Aktarılanlar tasarımcısını Deyimlerinizde kullanın türler için ad alanları girmenizi sağlar. Benzer şekilde **aktarır** veya **kullanarak** anahtar sözcükleri Visual Basic. NET'te ve C#, içeri aktarmalar tasarımcısını alanlarında İfadenizde bir tür adı girmeniz yeterlidir etkinleştirme belirtme yerine tam olarak Sürüm nitelikli tür adı.  
  
 İçe Aktarılanlar tasarımcısını, her iki değişiklik kullanıcı arabiriminde ve iş akışı kaydedildiğinde yapılan değişiklikleri tepki verir. İş akışı kaydedildikten sonra ad alanları için içeri aktarmalar tasarımcısını otomatik olarak eklenebilir. Bunlar aşağıdakileri içerir:  
  
- Değişken ve bağımsız değişken bildirimlerinde kullanılan türler için ad alanları.  
  
- İfadelerinde kullanılan türler için ad alanları.  
  
- İş akışı (örneğin, özel etkinlikler iş akışında bırakılan tarafından kullanılan ad) serileştirmek için gereken bir diğer ad alanları.  
  
  İş akışı kaydedildiğinde, el ile silinmiş bazı ad alanları önceki listede açıklanan mantığı nedeniyle otomatik olarak için içeri aktarmalar tasarımcısını yeniden eklenmiş olduğunu fark edebilirsiniz.  
  
### <a name="to-add-a-namespace-to-the-list-of-imported-namespaces"></a>Bir ad alanı içeri aktarılan ad uzaylarını listesine eklemek için  
  
1. Bir WCF iş akışı hizmeti uygulaması, iş akışı konsol uygulaması veya etkinlik kitaplığı projesinde [!INCLUDE[vs2010](../includes/vs2010-md.md)] ya da yeniden barındırılan iş akışı bir uygulama.  
  
2. Tıklayın **içeri aktarmalar** ana tuvalin alt. İçe Aktarılanlar tasarımcısını görünür.  
  
3. İçe Aktarılanlar tasarımcısını üst kısmındaki açılan liste denetiminden bir ad alanı seçin veya girin.  
  
     Siz yazarken, yazılan karakterlerin eşleşen geçerli ad alanlarının listesi görüntülenir.  
  
4. Tuşuna **Enter** ad listesine ekleme.  
  
5. Listeden bir ad alanı kaldırmak istiyorsanız, ad alanını seçin ve sonra basın **Sil** klavyenizde anahtar. Ad alanı herhangi bir nedenle örneğin ad alanını içeren derleme artık proje tarafından başvurulan, geçersizse, bir ad alanı'nin yalnızca silinmiş unutmayın.