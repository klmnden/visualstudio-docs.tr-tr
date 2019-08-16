---
title: 'CA1028: Sabit listesi depolaması Int32 olmalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1028
- EnumStorageShouldBeInt32
helpviewer_keywords:
- EnumStorageShouldBeInt32
- CA1028
ms.assetid: 87160825-9f39-4142-8d7f-a31fe7ac7b84
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c91de575abe8b19a5d8f6fca864e2bc452da7cb2
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547650"
---
# <a name="ca1028-enum-storage-should-be-int32"></a>CA1028: Sabit listesi depolaması Int32 olmalıdır

|||
|-|-|
|TypeName|EnumStorageShouldBeInt32|
|CheckId|CA1028|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir numaralandırmanın temel alınan türü değil <xref:System.Int32?displayProperty=fullName>.

Varsayılan olarak, bu kural yalnızca genel numaralandırmalara bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir numaralandırma ilişkili adlandırılmış sabitler kümesini tanımlayan değer türüdür. Varsayılan olarak, <xref:System.Int32?displayProperty=fullName> veri türü sabit değeri depolamak için kullanılır. Bu temel türü değiştirebilse de, çoğu senaryo için gerekli değildir veya önerilmez. ' Den <xref:System.Int32>küçük bir veri türü kullanılarak önemli bir performans kazancı elde değildir. Varsayılan veri türünü kullanamadığı takdirde, numaralandırmanın tüm değerlerinin temsil edilebilmesi için ortak dil sistemi <xref:System.Byte>(CLS) uyumlu integral türlerinden <xref:System.Int16> <xref:System.Int32>birini,,, veya <xref:System.Int64> ' i kullanmanız gerekir. CLS uyumlu programlama dilleri.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Boyut veya uyumluluk sorunları mevcut olmadığı takdirde bu kuralın ihlal edildiğini gidermek için kullanın <xref:System.Int32>. Değerleri tutmak için <xref:System.Int32> yeterince büyük olmayan durumlar için, kullanın. <xref:System.Int64> Geriye dönük uyumluluk için daha küçük bir veri türü gerekiyorsa <xref:System.Byte> , <xref:System.Int16>veya kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yalnızca geri uyumluluk sorunları gerektiriyorsa, bu kuraldan bir uyarı gizleyin. Uygulamalarda, bu kurala uyamaması genellikle soruna neden olmaz. Dillerde birlikte çalışabilirliğin gerekli olduğu kitaplıklarda, bu kurala uyamaması, kullanıcılarınızı olumsuz etkileyebilir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1028.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example-of-a-violation"></a>İhlalin örneği

Aşağıdaki örnek, önerilen temel veri türünü kullanmayan iki sabit listesi gösterir.

[!code-vb[FxCop.Design.EnumIntegralType#1](../code-quality/codesnippet/VisualBasic/ca1028-enum-storage-should-be-int32_1.vb)]
[!code-csharp[FxCop.Design.EnumIntegralType#1](../code-quality/codesnippet/CSharp/ca1028-enum-storage-should-be-int32_1.cs)]

## <a name="example-of-how-to-fix"></a>Nasıl düzeltileceğini gösteren örnek

Aşağıdaki örnek, temel alınan veri türünü olarak <xref:System.Int32>değiştirerek önceki ihlalin düzeltir.

[!code-csharp[FxCop.Design.EnumIntegralTypeFixed#1](../code-quality/codesnippet/CSharp/ca1028-enum-storage-should-be-int32_2.cs)]
[!code-vb[FxCop.Design.EnumIntegralTypeFixed#1](../code-quality/codesnippet/VisualBasic/ca1028-enum-storage-should-be-int32_2.vb)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1008 Numaralandırmalar sıfır değerine sahip olmalıdır](../code-quality/ca1008-enums-should-have-zero-value.md)
- [CA1027 Numaralandırmaları FlagsAttribute ile işaretle](../code-quality/ca1027-mark-enums-with-flagsattribute.md)
- [CA2217 Numaralandırmaları FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)
- [CA1700 ' Ayrılmış ' Enum değerlerini adlandırma](../code-quality/ca1700-do-not-name-enum-values-reserved.md)
- [CA1712 Tür adı ile Enum değerlerini önek olarak kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Byte?displayProperty=fullName>
- <xref:System.Int16?displayProperty=fullName>
- <xref:System.Int32?displayProperty=fullName>
- <xref:System.Int64?displayProperty=fullName>