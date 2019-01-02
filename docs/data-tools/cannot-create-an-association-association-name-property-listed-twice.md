---
title: Bir ilişkilendirme - özellik iki kere listelenmiş oluşturulamıyor
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 3ced8bda-210e-4caf-9d8f-96cdbba19251
author: gewarren
ms.author: gewarren
manager: douge
ms.prod: visual-studio-dev15
ms.workload:
- data-storage
ms.openlocfilehash: db36f6e15a219109fa60ffaed13a01890833ea82
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53910863"
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