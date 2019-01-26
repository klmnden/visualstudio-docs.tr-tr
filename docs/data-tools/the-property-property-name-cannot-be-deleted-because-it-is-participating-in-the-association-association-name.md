---
title: Özellik ilişkilendirmesine katıldığından silinemiyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 389873cc-92dd-48da-bfca-0f6c8e0ae3c2
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: 32eeef65eaf8cfebbce0458b90f954bf491f718a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54997968"
---
# <a name="the-property-ltproperty-namegt-cannot-be-deleted-because-it-is-participating-in-the-association-ltassociation-namegt"></a>Özellik &lt;özellik adı&gt; ilişkilendirmesine katıldığından silinemiyor &lt;ilişkilendirme adı&gt;

Seçilen özellik olarak ayarlandığından **ilişkilendirme** hata iletisinde belirtilen sınıfları arasında ilişkilendirme için. Veri sınıfları arasında ilişkilendirme katılan varsa özellikleri silinemez.

Ayarlama **ilişkilendirme** başarılı silinmesini istenen özelliği etkinleştirmek için veri sınıfın farklı bir özellik için.

## <a name="to-correct-this-error"></a>Bu hatayı düzeltmek için

1. İlişkilendirme çizgisi seçin **O/R Tasarımcısı** hata iletisinde belirtilen veri sınıfları bağlanır.

2. Satırı açmak için çift tıklatın **ilişkilendirme Düzenleyicisi** iletişim kutusu.

3. Özelliğinden kaldırılacak **ilişkilendirme özellikleri**.

4. Özelliği yeniden silmeyi deneyin.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)