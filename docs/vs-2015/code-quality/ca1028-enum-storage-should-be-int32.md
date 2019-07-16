---
title: 'CA1028: Numaralandırma depolaması Int32 olmalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1028
- EnumStorageShouldBeInt32
helpviewer_keywords:
- EnumStorageShouldBeInt32
- CA1028
ms.assetid: 87160825-9f39-4142-8d7f-a31fe7ac7b84
caps.latest.revision: 21
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e79eb7e0ed33184103cc772c13515959cf973ecc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68192805"
---
# <a name="ca1028-enum-storage-should-be-int32"></a>CA1028: Sabit listesi depolaması Int32 olmalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|EnumStorageShouldBeInt32|
|CheckId|CA1028|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Genel bir sabit listesi türünü temel değil <xref:System.Int32?displayProperty=fullName>.

## <a name="rule-description"></a>Kural Tanımı
 Bir numaralandırma ilişkili adlandırılmış sabitler kümesini tanımlayan değer türüdür. Varsayılan olarak, <xref:System.Int32?displayProperty=fullName> veri türü sabit değerleri depolamak için kullanılır. Olsa da, temel alınan türü değiştirebilirsiniz, bu çoğu senaryo için gerekli veya önerilen değil. Hiçbir önemli bir performans kazancı elde ettiği değerinden küçük olan bir veri türü kullanarak Not <xref:System.Int32>. Varsayılan veri türü kullanamıyorsanız, bir ortak dil System (CLS) birini kullanmanız gerekir-uyumlu tam sayı türleri <xref:System.Byte>, <xref:System.Int16>, <xref:System.Int32>, veya <xref:System.Int64> numaralandırma tüm değerleri içinde gösterilebilen emin olmak için CLS uyumlu programlama dili.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Boyut veya uyumluluk sorunları var sürece bu kural ihlalini düzeltmek için kullanın <xref:System.Int32>. Durumlar için burada <xref:System.Int32> kullanın değerleri tutmak için yeterli büyüklükte değil <xref:System.Int64>. Geriye dönük uyumluluk daha küçük bir veri türü gerektiriyorsa, kullanın <xref:System.Byte> veya <xref:System.Int16>.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Yalnızca geriye dönük uyumluluk için gerekirse bu kuraldan bir uyarıyı gizler. Uygulamalar, bu kurala genellikle uygun hatası sorununa neden olmaz. Diller arası çalışabilirlik gerekli olduğu kitaplıklarında, bu kurala uygun hatası kullanıcılarınız olumsuz etkileyebilir.

## <a name="example-of-a-violation"></a>Bir ihlali örneği

### <a name="description"></a>Açıklama
 Aşağıdaki örnek, önerilen temel alınan veri türünü kullanmayın iki sabit listeleri gösterir.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Design.EnumIntegralType#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.EnumIntegralType/cs/FxCop.Design.EnumIntegralType.cs#1)]
 [!code-vb[FxCop.Design.EnumIntegralType#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.EnumIntegralType/vb/FxCop.Design.EnumIntegralType.vb#1)]

## <a name="example-of-how-to-fix"></a>İlişkin bir örnek için düzeltme

### <a name="description"></a>Açıklama
 Aşağıdaki örnek, temel alınan veri türüne değiştirerek önceki ihlali giderir <xref:System.Int32>.

### <a name="code"></a>Kod
 [!code-csharp[FxCop.Design.EnumIntegralTypeFixed#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.EnumIntegralTypeFixed/cs/FxCop.Design.EnumIntegralTypeFixed.cs#1)]
 [!code-vb[FxCop.Design.EnumIntegralTypeFixed#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.EnumIntegralTypeFixed/vb/FxCop.Design.EnumIntegralTypeFixed.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1008: Numaralandırmalar sıfır değerine sahip olmalıdır](../code-quality/ca1008-enums-should-have-zero-value.md)

 [CA1027: Sabit listelerini FlagsAttribute ile işaretleyin](../code-quality/ca1027-mark-enums-with-flagsattribute.md)

 [CA2217: Sabit listelerini FlagsAttribute ile işaretlemeyin](../code-quality/ca2217-do-not-mark-enums-with-flagsattribute.md)

 [CA1700: Numaralandırma değerlerini 'Reserved' olarak adlandırmayın](../code-quality/ca1700-do-not-name-enum-values-reserved.md)

 [CA1712: Enum değerleri için tür adıyla önek kullanmayın](../code-quality/ca1712-do-not-prefix-enum-values-with-type-name.md)

## <a name="see-also"></a>Ayrıca Bkz.
 <xref:System.Byte?displayProperty=fullName><xref:System.Int16?displayProperty=fullName>
 <xref:System.Int32?displayProperty=fullName>
 <xref:System.Int64?displayProperty=fullName>
