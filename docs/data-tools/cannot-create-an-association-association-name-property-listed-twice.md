---
title: Bir ilişkilendirme - özellik iki kere listelenmiş oluşturulamıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 3ced8bda-210e-4caf-9d8f-96cdbba19251
author: gewarren
ms.author: gewarren
manager: jillfra
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: da5ee57dda360f9851737fe061ee02c6aeae4c8e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54954754"
---
# <a name="cannot-create-an-association-ltassociation-namegt---property-listed-twice"></a>Bir ilişki oluşturulamıyor &lt;ilişkilendirme adı&gt; -özellik iki kere listelenmiş

Bir ilişki oluşturulamıyor \<ilişkilendirme adı >. Aynı özellik birden fazla kez listeleniyor: \<özellik adı >.

İlişkilendirmeleri tanımlanmış tarafından seçilen **ilişkilendirme özellikleri** içinde **ilişkilendirme Düzenleyicisi** iletişim kutusu. Özellikler, ilişkilendirmenin her sınıf için yalnızca bir kez listelenebilir.

İleti özelliği üst veya alt sınıfın içinde birden fazla kez görünür **ilişkilendirme özellikleri**.

## <a name="to-resolve-this-condition"></a>Bu durumu düzeltmek için

- İletisini inceleyin ve message içinde belirtilen özelliğini not edin.

- Tıklayın **Tamam** ileti kutusunu kapatın.

- İnceleme **ilişkilendirme özellikleri** ve yinelenen girdileri kaldırın.

- **Tamam**'ı tıklatın.

## <a name="see-also"></a>Ayrıca bkz.

- [O/R Tasarımcısı iletileri](../data-tools/o-r-designer-messages.md)
- [Visual Studio'da LINQ to SQL araçları](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
- [Nasıl yapılır: LINQ to SQL sınıfları (O/R Tasarımcısı) arasında ilişkilendirme oluşturma](../data-tools/how-to-create-an-association-relationship-between-linq-to-sql-classes-o-r-designer.md)