---
title: 'CA1307: StringComparison belirt'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1307
- SpecifyStringComparison
helpviewer_keywords:
- CA1307
- SpecifyStringComparison
ms.assetid: 9b0d5e71-1683-4a0d-bc4a-68b2fbd8af71
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e352eea1b7fcf82cb948315affeae6e30690a4aa
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234969"
---
# <a name="ca1307-specify-stringcomparison"></a>CA1307: StringComparison belirt

|||
|-|-|
|TypeName|SpecifyStringComparison|
|CheckId|CA1307|
|Kategori|Microsoft. Globalization|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Dize karşılaştırma işlemi, <xref:System.StringComparison> parametre ayarlanmamış bir yöntem aşırı yüklemesi kullanır.

## <a name="rule-description"></a>Kural açıklaması
Çoğu <xref:System.String.Compare%2A> dize işlemi, ve <xref:System.String.Equals%2A> yöntemleri, bir <xref:System.StringComparison> sabit listesi değerini parametre olarak kabul eden bir aşırı yükleme sağlar.

Bir <xref:System.StringComparison> parametre alan aşırı yükleme olduğunda, bu parametreyi almayan aşırı yükleme yerine kullanılmalıdır. Bu parametreyi açıkça ayarlayarak, kodunuz genellikle daha net ve bakım daha kolay hale getirilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için dize karşılaştırma yöntemlerini bir parametre olarak <xref:System.StringComparison> numaralandırmayı kabul eden aşırı yüklemeleri değiştirin. Örneğin: olarak `String.Compare(str1, str2, StringComparison.Ordinal)`değiştirin `String.Compare(str1, str2)` .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Kitaplık veya uygulama sınırlı bir yerel hedef kitle için tasarlanıyorsa ve bu nedenle yerelleştirilmez, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="see-also"></a>Ayrıca bkz.

- [Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)
- [CA1309: Sıralı StringComparison kullanın](../code-quality/ca1309-use-ordinal-stringcomparison.md)