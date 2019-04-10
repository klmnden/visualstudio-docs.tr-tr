---
title: foreach döngüsünü LINQ’ya dönüştürme
ms.date: 02/20/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 1d6b575e88349c71f1234950d4efaf77d23518c1
ms.sourcegitcommit: 0a2fdc23faee77187e10a1c19665ba5a1ac68e72
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/10/2019
ms.locfileid: "59477508"
---
# <a name="convert-foreach-loop-to-linq"></a>foreach döngüsünü LINQ’ya dönüştürme

Bu yeniden düzenleme için geçerlidir:

- C#

**Ne:** Foreach döngülerinizde IEnumerables LINQ sorgusu veya LINQ çağrı formu (LINQ yöntemi olarak da bilinir) kullanarak kolayca dönüştürmenize olanak tanır.

**ne zaman:** LINQ sorgusu okumak için tercih ettiğiniz bir IEnumerable kullanan bir foreach döngüsü olduğunda.

**Neden:** Kullanıcılar LINQ söz dizimi yerine kullandığı bir foreach döngüsü tercih edebilirsiniz bazen. [LINQ](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq) sorguyu bir birinci sınıf dil hale oluşturmak C#. LINQ dosyasındaki kod miktarını azaltmak okunmalarını kolaylaştırmak ve benzer sorgu ifade desenleri farklı veri kaynaklarına izin.

> [!NOTE]
> LINQ, foreach döngü daha az yüksek performanslı sözdizimidir. Tüm performansı dengenin, dikkat edilmesi gereken onun iyi LINQ ile kod okunurluğunu neden olabilir.

## <a name="convert-foreach-loop-to-linq-refactoring"></a>LINQ yeniden düzenleme için foreach döngüsünü dönüştürme

1. İmlecinizi, `foreach` anahtar sözcüğü.

    ![Foreach kullanarak IEnumerable](media/convert-foreach-to-LINQ.png)

2. Tuşuna **Ctrl**+**.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

   ![LINQ menüye dönüştürme](media/convert-foreach-to-LINQ-codefix.png)

3. Seçin **LINQ to dönüştürme** veya **(çağrı formu) LINQ to Dönüştür**

   ![LINQ Sorgu sonucu](media/convert-foreach-to-LINQ-result.png)
   
   ![LINQ çağrı form sonucu](media/convert-foreach-to-LINQ-callform-result.png)
   
 ### <a name="sample-code"></a>Örnek Kod

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

- [Yeniden Düzenle](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
- [.NET geliştiricileri için ipuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)
