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
ms.openlocfilehash: b00accdbdb08e4267bbca2b7e5fab8002f539f1d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62546485"
---
# <a name="ca1309-use-ordinal-stringcomparison"></a>CA1309: Sıralı StringComparison kullanın

|||
|-|-|
|TypeName|UseOrdinalStringComparison|
|CheckId|CA1309|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep

Nonlinguistic bir dize karşılaştırma işlemi ayarlı değil <xref:System.StringComparison> ya da parametre **sıra** veya **Ordinalıgnorecase**.

## <a name="rule-description"></a>Kural açıklaması
 Çoğu dize işlemleri, en önemlisi <xref:System.String.Compare%2A?displayProperty=fullName> ve <xref:System.String.Equals%2A?displayProperty=fullName> yöntemleri artık kabul eden bir aşırı sağlayan bir <xref:System.StringComparison?displayProperty=fullName> numaralandırma değeri olarak bir parametre.

 Belirttiğinizde ya da **StringComparison.Ordinal** veya **Stringcomparison.ordinalıgnorecase**, dilsel olmayan dize karşılaştırması. Diğer bir deyişle, karşılaştırma kararlar verildiğinde doğal dile özgü özellikleri göz ardı edilir. Doğal dil özellikleri yoksayılıyor kararları basit bayt karşılaştırmalarını ve büyük/küçük harf veya kültür tarafından parametre haline getirilen denklik tablolar üzerinde dayalı anlamına gelir. Sonuç olarak, açıkça ya da parametre ayarı tarafından **StringComparison.Ordinal** veya **Stringcomparison.ordinalıgnorecase**, kodunuzu genellikle hız kazandığı doğruluğu artırır ve olur daha güvenilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için dize karşılaştırma yöntemini kabul eden bir aşırı değiştirin <xref:System.StringComparison?displayProperty=fullName> , parametre olarak numaralandırması belirtin **sıra** veya **Ordinalıgnorecase**. Örneğin, değiştirme `String.Compare(str1, str2)` için `String.Compare(str1, str2, StringComparison.Ordinal)`.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Uygulama ve kitaplık yerel sınırlı bir kitle için kullanılacaksa, ya da geçerli kültürü semantiği kullanılmalıdır bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="see-also"></a>Ayrıca bkz.

- [Genelleştirme Uyarıları](../code-quality/globalization-warnings.md)
- [CA1307: StringComparison belirtin](../code-quality/ca1307-specify-stringcomparison.md)