---
title: 'CA2233: İşleçler taşmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- OperationsShouldNotOverflow
- CA2233
helpviewer_keywords:
- OperationsShouldNotOverflow
- CA2233
ms.assetid: 3a2b06ba-6d1b-4666-9eaf-e053ef47ffaa
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: b99aae681dbe7bbeece557a15d78aed0b3f07f6f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71230825"
---
# <a name="ca2233-operations-should-not-overflow"></a>CA2233: İşleçler taşmamalıdır

|||
|-|-|
|TypeName|OperationsShouldNotOverflow|
|CheckId|CA2233|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir yöntem bir aritmetik işlem gerçekleştirir ve taşmayı engellemek için işleneni doğrulamaz.

## <a name="rule-description"></a>Kural açıklaması

İşlemin sonucunun, dahil edilen veri türleri için olası değerler aralığının dışında olmadığından emin olmak için, önce işlenenleri doğrulamadan aritmetik işlemler yapmayın. Yürütme bağlamına ve dahil edilen veri türlerine bağlı olarak, aritmetik taşma, sonucun bir <xref:System.OverflowException?displayProperty=fullName> veya en önemli bitlerinin iptal edilmesine yol açabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlal edildiğini onarmak için, işlemi gerçekleştirmeden önce işlenenleri doğrulayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

İşlenenlerin olası değerleri hiçbir şekilde aritmetik işlemin taşmasına neden olursa, bu kuraldan bir uyarı bastırılmaz.

## <a name="example-of-a-violation"></a>İhlalin örneği

Aşağıdaki örnekteki bir yöntem, bu kuralı ihlal eden bir tamsayıyı yönetir. [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]Bu, tetiklenmesi için tamsayı taşmasını **Kaldır** seçeneğinin devre dışı olmasını gerektirir.

[!code-vb[FxCop.Usage.OperationOverflow#1](../code-quality/codesnippet/VisualBasic/ca2233-operations-should-not-overflow_1.vb)]
[!code-csharp[FxCop.Usage.OperationOverflow#1](../code-quality/codesnippet/CSharp/ca2233-operations-should-not-overflow_1.cs)]

Bu örnekteki yöntem geçirilmemişse <xref:System.Int32.MinValue?displayProperty=fullName>, işlem alttan olur. Bu, sonucun en önemli bitinin atılmasına neden olur. Aşağıdaki kodda bunun nasıl gerçekleştiği gösterilmektedir.

```csharp
public static void Main()
{
    int value = int.MinValue;    // int.MinValue is -2147483648
    value = Calculator.Decrement(value);
    Console.WriteLine(value);
}
```

```vb
Public Shared Sub Main()
    Dim value = Integer.MinValue    ' Integer.MinValue is -2147483648
    value = Calculator.Decrement(value)
    Console.WriteLine(value)
End Sub
```

Çıktı:

```text
2147483647
```

## <a name="fix-with-input-parameter-validation"></a>Giriş parametresi doğrulaması ile onarma

Aşağıdaki örnek, girişin değerini doğrulayarak önceki ihlalin düzeltir.

[!code-csharp[FxCop.Usage.OperationOverflowFixed#1](../code-quality/codesnippet/CSharp/ca2233-operations-should-not-overflow_2.cs)]
[!code-vb[FxCop.Usage.OperationOverflowFixed#1](../code-quality/codesnippet/VisualBasic/ca2233-operations-should-not-overflow_2.vb)]

## <a name="fix-with-a-checked-block"></a>Denetlenen bir blok ile onarma

Aşağıdaki örnek, işlemi işaretli bir blokta sarmalayarak önceki ihlalin düzeltir. İşlem bir taşmaya neden oluyorsa, bir <xref:System.OverflowException?displayProperty=fullName> oluşturulur.

Denetlenen bloklar içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]desteklenmez.

[!code-csharp[FxCop.Usage.OperationOverflowChecked#1](../code-quality/codesnippet/CSharp/ca2233-operations-should-not-overflow_3.cs)]

## <a name="turn-on-checked-arithmetic-overflowunderflow"></a>Işaretli aritmetik taşmaya/yetersiz kalması etkinleştir

Üzerinde işaretli aritmetik taşma/aşağı taşması açarsanız C#, her tamsayı işlemini işaretlenmiş bir blokta sarmalamayı eşdeğerdir.

Üzerinde işaretli aritmetik taşma/aşağı taşması açmak için C#:

1. **Çözüm Gezgini**, projenize sağ tıklayın ve **Özellikler**' i seçin.

2. **Derleme** sekmesini seçin ve **Gelişmiş**' e tıklayın.

3. **Aritmetik taşma/yetersiz Için denetle** öğesini seçin ve **Tamam**' a tıklayın.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.OverflowException?displayProperty=fullName>
- [C# İşleçleri](/dotnet/csharp/language-reference/operators/index)
- [İşaretli ve İşaretsiz](/dotnet/csharp/language-reference/keywords/checked-and-unchecked)