---
title: 'CA1309: Sıralı StringComparison kullanın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- UseOrdinalStringComparison
- CA1309
helpviewer_keywords:
- UseOrdinalStringComparison
- CA1309
ms.assetid: 19be0854-cb6e-4efd-a4c8-a5c1fc6f7a71
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eff846cfacb30d97c28cadd14b86f7724b1d2ce4
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234931"
---
# <a name="ca1309-use-ordinal-stringcomparison"></a>CA1309: Sıralı StringComparison kullanın

|||
|-|-|
|TypeName|UseOrdinalStringComparison|
|CheckId|CA1309|
|Kategori|Microsoft. Globalization|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Dilsel olmayan bir dize karşılaştırma işlemi, <xref:System.StringComparison> parametreyi **Ordinal** veya **OrdinalIgnoreCase**olarak ayarlamayın.

## <a name="rule-description"></a>Kural açıklaması
Çok sayıda dize işlemi, en önemlisi <xref:System.String.Compare%2A?displayProperty=fullName> ve <xref:System.String.Equals%2A?displayProperty=fullName> yöntemleri, artık bir <xref:System.StringComparison?displayProperty=fullName> sabit listesi değerini parametre olarak kabul eden bir aşırı yükleme sağlar.

**StringComparison. Ordinal** ya da **StringComparison. OrdinalIgnoreCase**belirttiğinizde, dize karşılaştırma dil değil. Yani, doğal dile özgü özellikler, karşılaştırma kararları verilirken yok sayılır. Doğal dil özelliklerini yok sayarak, kararlar, kültüre göre parametreli büyük/küçük harf veya denklik tablolarda değil basit bayt karşılaştırmaları temel alır. Sonuç olarak, parametresini **StringComparison. Ordinal** ya da **StringComparison. OrdinalIgnoreCase**olarak ayarlayarak, kodunuz genellikle hızlanır, doğruluk artar ve daha güvenilir hale gelir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, dize karşılaştırma yöntemini bir parametre olarak <xref:System.StringComparison?displayProperty=fullName> numaralandırmayı kabul eden bir aşırı yükleme olarak değiştirin ve **Ordinal** ya da **OrdinalIgnoreCase**belirtin. Örneğin, olarak `String.Compare(str1, str2, StringComparison.Ordinal)`değiştirin `String.Compare(str1, str2)` .

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Kitaplık veya uygulama sınırlı bir yerel hedef kitle için tasarlanıyorsa veya geçerli kültürün semantiğinin kullanılması gerektiğinde, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="see-also"></a>Ayrıca bkz.

- [Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)
- [CA1307 StringComparison belirt](../code-quality/ca1307-specify-stringcomparison.md)