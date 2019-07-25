---
title: Foreach döngüsünü LINQ 'a Dönüştür
descritpion: Convert any foreach loop that uses an IEnumerable to a LINQ query or a LINQ call form (also known as a LINQ method).
ms.date: 02/20/2019
ms.topic: reference
author: kendrahavens
ms.author: kehavens
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: baa1f32bb981e6d244555baef2a00d03933cdd6c
ms.sourcegitcommit: 0f5f7955076238742f2071d286ad8e896f3a6cad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68483712"
---
# <a name="convert-a-foreach-loop-to-linq"></a>Foreach döngüsünü LINQ 'a Dönüştür

Bu yeniden düzenleme için geçerlidir:

- C#

**Yazdırılacak** IEnumerable kullanan *foreach* DÖNGÜNÜZÜ bir LINQ SORGUSUNA veya LINQ çağrı formuna (LINQ yöntemi olarak da bilinir) kolayca dönüştürmenize olanak sağlar.

**Oluşturulurken** IEnumerable kullanan bir foreach döngüsüne sahipsiniz ve bu döngünün LINQ sorgusu olarak okunmasını istiyorsunuz.

**Kaydol** Bir foreach döngüsü yerine LINQ sözdizimini kullanmayı tercih edersiniz. [LINQ](/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq) , içindeki C#ilk sınıf dil yapısına bir sorgu oluşturur. LINQ bir dosyadaki kod miktarını azaltabilir, kodu daha kolay okunabilir hale getirir ve farklı veri kaynaklarının benzer sorgu ifadesi desenlerine sahip olmasına izin verir.

> [!NOTE]
> LINQ sözdizimi genellikle bir foreach döngüsünden daha az verimlidir. Kodunuzun okunabilirliğini geliştirmek için LINQ kullandığınızda oluşabilecek herhangi bir performans zorunluluğunu getirir dikkat etmeniz iyidir.

## <a name="convert-a-foreach-loop-to-linq-refactoring"></a>Foreach döngüsünü LINQ yeniden düzenlemeye Dönüştür

1. İmlecinizi `foreach` anahtar sözcüğe yerleştirin.

    ![IEnumerable örneği kullanan foreach](media/convert-foreach-to-LINQ.png)

2. Tuşuna **Ctrl**+ **.** Tetikleyici için **hızlı Eylemler ve yeniden düzenlemeler** menüsü.

   ![LINQ menü örneğine Dönüştür](media/convert-foreach-to-LINQ-codefix.png)

3. **LINQ 'A Dönüştür** veya **LINQ 'a Dönüştür (çağrı formu)** seçeneğini belirleyin.

   ![LINQ sorgu sonucu örneği](media/convert-foreach-to-LINQ-result.png)

   ![LINQ Call form sonuç örneği](media/convert-foreach-to-LINQ-callform-result.png)

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
