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
ms.openlocfilehash: eadad8fdbec990607450b374a32758547194f734
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58160280"
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

## <a name="see-also"></a>Ayrıca bkz.

- [Yeniden Düzenleme](../refactoring-in-visual-studio.md)
- [Değişiklikleri Önizleme](../../ide/preview-changes.md)
- [.NET Geliştiricileri için İpuçları](../../ide/visual-studio-2017-for-dotnet-developers.md)