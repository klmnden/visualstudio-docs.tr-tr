---
title: 'İş Akışı Tasarımcısı - nasıl yapılır: İçeri Aktarmalar Tasarımcısını Kullanma'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- System.Activities.Presentation.View.ImportDesigner.UI
ms.assetid: 61328ab6-9b66-4e12-8630-22e30ee8c9d1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: df041111bb452462c969995bacee97b08488d1c6
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55931968"
---
# <a name="how-to-use-the-imports-designer"></a>Nasıl yapılır: İçeri Aktarmalar Tasarımcısını Kullanma

İçe Aktarılanlar tasarımcısını Deyimlerinizde kullanın türler için ad alanları girmenizi sağlar. Benzer şekilde **aktarır** veya **kullanarak** Visual Basic anahtar sözcükleri ve C#, içeri aktarmalar tasarımcısını alanlarında İfadenizde bir tür adı girmeniz yeterlidir etkinleştirme belirtme yerine tam olarak Sürüm nitelikli tür adı.

İçe Aktarılanlar tasarımcısını, her iki değişiklik kullanıcı arabiriminde ve iş akışı kaydedildiğinde yapılan değişiklikleri tepki verir. İş akışı kaydedildikten sonra ad alanları için içeri aktarmalar tasarımcısını otomatik olarak eklenebilir. Bunlar aşağıdakileri içerir:

- Değişken ve bağımsız değişken bildirimlerinde kullanılan türler için ad alanları.

- İfadelerinde kullanılan türler için ad alanları.

- İş akışı (örneğin, özel etkinlikler iş akışında bırakılan tarafından kullanılan ad) serileştirmek için gereken bir diğer ad alanları.

  İş akışı kaydedildiğinde, el ile silinmiş bazı ad alanları önceki listede açıklanan mantığı nedeniyle otomatik olarak için içeri aktarmalar tasarımcısını yeniden eklenmiş olduğunu fark edebilirsiniz.

## <a name="to-add-a-namespace-to-the-list-of-imported-namespaces"></a>Bir ad alanı içeri aktarılan ad uzaylarını listesine eklemek için

1.  WCF iş akışı hizmeti uygulaması, iş akışı konsol uygulaması veya etkinlik kitaplığı projesi, Visual Studio veya yeniden barındırılan iş akışı uygulamasını açın.

2.  Tıklayın **içeri aktarmalar** ana tuvalin alt. İçe Aktarılanlar tasarımcısını görünür.

3.  İçe Aktarılanlar tasarımcısını üst kısmındaki açılan liste denetiminden bir ad alanı seçin veya girin.

     Siz yazarken, yazılan karakterlerin eşleşen geçerli ad alanlarının listesi görüntülenir.

4.  Tuşuna **Enter** ad listesine ekleme.

5.  Listeden bir ad alanı kaldırmak istiyorsanız, ad alanını seçin ve sonra basın **Sil** klavyenizde anahtar. Ad alanı herhangi bir nedenle örneğin ad alanını içeren derleme artık proje tarafından başvurulan, geçersizse, bir ad alanı'nin yalnızca silinmiş unutmayın.