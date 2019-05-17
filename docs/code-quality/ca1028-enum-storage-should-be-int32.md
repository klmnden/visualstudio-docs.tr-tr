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
ms.openlocfilehash: eee81a96e6841aa77e2056a95bd18979724b62e5
ms.sourcegitcommit: 2ee11676af4f3fc5729934d52541e9871fb43ee9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/17/2019
ms.locfileid: "65842403"
---
# <a name="ca1028-enum-storage-should-be-int32"></a>CA1028: Sabit listesi depolaması Int32 olmalıdır

|||
|-|-|
|TypeName|EnumStorageShouldBeInt32|
|CheckId|CA1028|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Temel alınan türü bir numaralandırmanın <xref:System.Int32?displayProperty=fullName>.

Varsayılan olarak, bu kural ortak numaralandırmalar yalnızca görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir numaralandırma ilişkili adlandırılmış sabitler kümesini tanımlayan değer türüdür. Varsayılan olarak, <xref:System.Int32?displayProperty=fullName> veri türü sabit değerleri depolamak için kullanılır. Olsa da, temel alınan türü değiştirebilirsiniz, bu çoğu senaryo için gerekli veya önerilen değil. Hiçbir önemli bir performans kazancı daha küçük olan bir veri türü kullanarak elde edebilirsiniz <xref:System.Int32>. Varsayılan veri türü kullanamıyorsanız, bir ortak dil System (CLS) birini kullanmanız gerekir-uyumlu tam sayı türleri <xref:System.Byte>, <xref:System.Int16>, <xref:System.Int32>, veya <xref:System.Int64> numaralandırma tüm değerleri içinde gösterilebilen emin olmak için CLS uyumlu programlama dili.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Boyut veya uyumluluk sorunları var sürece bu kural ihlalini düzeltmek için kullanın <xref:System.Int32>. Durumlar için burada <xref:System.Int32> kullanın değerleri tutmak için yeterli büyüklükte değil <xref:System.Int64>. Geriye dönük uyumluluk daha küçük bir veri türü gerektiriyorsa, kullanın <xref:System.Byte> veya <xref:System.Int16>.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Yalnızca geriye dönük uyumluluk için gerekirse bu kuraldan bir uyarıyı gizler. Uygulamalar, bu kurala genellikle uygun hatası sorununa neden olmaz. Diller arası çalışabilirlik gerekli olduğu kitaplıklarında, bu kurala uygun hatası kullanıcılarınız olumsuz etkileyebilir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```ini
dotnet_code_quality.ca1028.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example-of-a-violation"></a>Bir ihlali örneği

Aşağıdaki örnek, önerilen temel alınan veri türünü kullanmayın iki sabit listeleri gösterir.

[!code-vb[FxCop.Design.EnumIntegralType#1](../code-quality/codesnippet/VisualBasic/ca1028-enum-storage-should-be-int32_1.vb)]
[!code-csharp[FxCop.Design.EnumIntegralType#1](../code-quality/codesnippet/CSharp/ca1028-enum-storage-should-be-int32_1.cs)]

## <a name="example-of-how-to-fix"></a>Nasıl düzeltileceğini örneği

Aşağıdaki örnek, temel alınan veri türüne değiştirerek önceki ihlali giderir <xref:System.Int32>.

[!code-csharp[FxCop.Design.EnumIntegralTypeFixed#1](../code-quality/codesnippet/CSharp/ca1028-enum-storage-should-be-int32_2.cs)]
[!code-vb[FxCop.Design.EnumIntegralTypeFixed#1](../code-quality/codesnippet/VisualBasic/ca1028-enum-storage-should-be-int32_2.vb)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1008: Numaralandırmalar sıfır değerine sahip olmalıdır](../code-quality/ca1008-enums-should-have-zero-value.md)
- [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)
- [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)
- [CA1700: Numaralandırma değerlerini 'Reserved' olarak adlandırmayın](../code-quality/ca1700-do-not-name-enum-values-reserved.md)
- [CA1712: Enum değerleri için tür adıyla önek kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Byte?displayProperty=fullName>
- <xref:System.Int16?displayProperty=fullName>
- <xref:System.Int32?displayProperty=fullName>
- <xref:System.Int64?displayProperty=fullName>