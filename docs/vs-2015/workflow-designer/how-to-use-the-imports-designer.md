---
title: 'Nasıl yapılır: içeri aktarmalar Tasarımcısını kullanma | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: .net-framework-4.6
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- System.Activities.Presentation.View.ImportDesigner.UI
ms.assetid: 61328ab6-9b66-4e12-8630-22e30ee8c9d1
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: erikre
ms.openlocfilehash: 776fbd9ba58268adb16957c732b96a7c8303b213
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49278388"
---
# <a name="how-to-use-the-imports-designer"></a>Nasıl yapılır: içeri aktarmalar Tasarımcısını kullanma
İçe Aktarılanlar tasarımcısını Deyimlerinizde kullanın türler için ad alanları girmenizi sağlar. Benzer şekilde **aktarır** veya **kullanarak** anahtar sözcükleri Visual Basic .NET ve ad alanlarını içeri aktarmalar Tasarımcısı'nda belirtme #c, ifadeniz yerine tam nitelikli tür adı girmeniz yeterlidir etkinleştir Sürüm türü adı.  
  
 İçe Aktarılanlar tasarımcısını, her iki değişiklik kullanıcı arabiriminde ve iş akışı kaydedildiğinde yapılan değişiklikleri tepki verir. İş akışı kaydedildikten sonra ad alanları için içeri aktarmalar tasarımcısını otomatik olarak eklenebilir. Bunlar aşağıdakileri içerir:  
  
-   Değişken ve bağımsız değişken bildirimlerinde kullanılan türler için ad alanları.  
  
-   İfadelerinde kullanılan türler için ad alanları.  
  
-   İş akışı (örneğin, özel etkinlikler iş akışında bırakılan tarafından kullanılan ad) serileştirmek için gereken bir diğer ad alanları.  
  
 İş akışı kaydedildiğinde, el ile silinmiş bazı ad alanları önceki listede açıklanan mantığı nedeniyle otomatik olarak için içeri aktarmalar tasarımcısını yeniden eklenmiş olduğunu fark edebilirsiniz.  
  
### <a name="to-add-a-namespace-to-the-list-of-imported-namespaces"></a>Bir ad alanı içeri aktarılan ad uzaylarını listesine eklemek için  
  
1.  Bir WCF iş akışı hizmeti uygulaması, iş akışı konsol uygulaması veya etkinlik kitaplığı projesinde [!INCLUDE[vs2010](../includes/vs2010-md.md)] ya da yeniden barındırılan iş akışı bir uygulama.  
  
2.  Tıklayın **içeri aktarmalar** ana tuvalin alt. İçe Aktarılanlar tasarımcısını görünür.  
  
3.  İçe Aktarılanlar tasarımcısını üst kısmındaki açılan liste denetiminden bir ad alanı seçin veya girin.  
  
     Siz yazarken, yazılan karakterlerin eşleşen geçerli ad alanlarının listesi görüntülenir.  
  
4.  Tuşuna **Enter** ad listesine ekleme.  
  
5.  Listeden bir ad alanı kaldırmak istiyorsanız, ad alanını seçin ve sonra basın **Sil** klavyenizde anahtar. Ad alanı herhangi bir nedenle örneğin ad alanını içeren derleme artık proje tarafından başvurulan, geçersizse, bir ad alanı'nin yalnızca silinmiş unutmayın.