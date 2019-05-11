---
title: LINQ to bir foreach döngüsünü dönüştürme
ms.date: 02/20/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 7893ed676372cce94d883353139de91ef639aeb0
ms.sourcegitcommit: 614d5b99576ea27a41957cd94062dc95cbd29c1c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/10/2019
ms.locfileid: "65531844"
---
# <a name="convert-a-foreach-loop-to-linq"></a>LINQ to bir foreach döngüsünü dönüştürme

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Kolayca dönüştürmenize olanak tanır, *foreach* kullanan bir LINQ Sorgu ya da bir LINQ çağrı formu (LINQ yöntemi olarak da bilinir) bir IEnumerable döngüsünü.

**ne zaman:** Bir IEnumerable kullanan bir foreach döngüsü sahiptir ve LINQ sorgusu okumak için bu döngü istiyor.

**Neden:** LINQ söz dizimi yerine bir foreach döngüsü kullanmayı tercih eder. [LINQ](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq) birinci sınıf bir dile içinde oluşturmak için bir sorgu kolaylaştırır C#. LINQ, bir dosyada kod miktarını azaltmak, kodun okunmasını kolaylaştırmak ve benzer sorgu ifade desenleri farklı veri kaynaklarına izin.

> [!NOTE]
> LINQ söz dizimi, genellikle bir foreach döngüsü verimli değildir. Kodunuzun okunabilirliği artırmak için LINQ kullanırken oluşabilecek performansta düşüş dikkat daha iyidir.

## <a name="convert-a-foreach-loop-to-linq-refactoring"></a>LINQ yeniden düzenleme için bir foreach döngüsünü dönüştürme

1. İmlecinizi, `foreach` anahtar sözcüğü.

    ![Foreach kullanarak IEnumerable örnek](media/convert-foreach-to-LINQ.png)

2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

   ![LINQ menü örneğine Dönüştür](media/convert-foreach-to-LINQ-codefix.png)

3. Seçin **LINQ to dönüştürme** veya **LINQ to (çağrı formu) dönüştürme**.

   ![LINQ Sorgu sonuç örneği](media/convert-foreach-to-LINQ-result.png)

   ![LINQ çağrı form sonuç örneği](media/convert-foreach-to-LINQ-callform-result.png)

### <a name="sample-code"></a>Örnek kod

```csharp
using System.Collections.Generic;

public class Class1
{
    public void MyMethod()
    {
        var greetings = new List<string>()
            { "hi", "yo", "hello", "howdy" };

        IEnumerable<string> enumerable()
        {
            foreach (var greet in greetings)
            {
                if (greet.Length < 3)
                {
                    yield return greet;
                }
            }

            yield break;
        }
    }
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizle penceresi](../../ide/preview-changes.md)
- [.NET Geliştiricileri için İpuçları](../csharp-developer-productivity.md)
