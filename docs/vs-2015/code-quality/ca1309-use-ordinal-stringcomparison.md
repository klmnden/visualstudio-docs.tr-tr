---
title: 'CA1309: Sıralı StringComparison kullanın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- UseOrdinalStringComparison
- CA1309
helpviewer_keywords:
- UseOrdinalStringComparison
- CA1309
ms.assetid: 19be0854-cb6e-4efd-a4c8-a5c1fc6f7a71
caps.latest.revision: 17
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 7b491cf06528b67c96f90f314210e61800e0cab1
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54762763"
---
# <a name="ca1309-use-ordinal-stringcomparison"></a>CA1309: Sıralı StringComparison kullanın
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|UseOrdinalStringComparison|
|CheckId|CA1309|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Nonlinguistic bir dize karşılaştırma işlemi ayarlı değil <xref:System.StringComparison> ya da parametre **sıra** veya **Ordinalıgnorecase**.

## <a name="rule-description"></a>Kural Tanımı
 Çoğu dize işlemleri, en önemli <xref:System.String.Compare%2A?displayProperty=fullName> ve <xref:System.String.Equals%2A?displayProperty=fullName> yöntemleri artık kabul eden bir aşırı sağlayan bir <xref:System.StringComparison?displayProperty=fullName> numaralandırma değeri olarak bir parametre.

 Belirttiğinizde ya da **StringComparison.Ordinal** veya **Stringcomparison.ordinalıgnorecase**, dize karşılaştırması nonlinguistic olacaktır. Diğer bir deyişle, karşılaştırma kararlar verildiğinde doğal dile özgü özellikleri göz ardı edilir. Bu kararların basit bayt karşılaştırmalarını temel alır ve kültür tarafından parametre haline getirilen büyük/küçük harf ya da denklik tabloları yoksay anlamına gelir. Sonuç olarak, açıkça ya da parametre ayarı tarafından **StringComparison.Ordinal** veya **Stringcomparison.ordinalıgnorecase**, kodunuzu genellikle hız kazandığı doğruluğu artırır ve olur daha güvenilir.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için dize karşılaştırma yöntemini kabul eden bir aşırı değiştirin <xref:System.StringComparison?displayProperty=fullName> , parametre olarak numaralandırması belirtin **sıra** veya **Ordinalıgnorecase**. Örneğin, değiştirme `String.Compare(str1, str2)` için `String.Compare(str1, str2, StringComparison.Ordinal)`.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Sınırlı bir yerel hedef kitle için veya geçerli kültürü semantiği kullanılmalıdır kitaplık veya uygulamanın amaçlanan bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="see-also"></a>Ayrıca Bkz.
 [Genelleştirme uyarıları](../code-quality/globalization-warnings.md) [CA1307: StringComparison belirtin](../code-quality/ca1307-specify-stringcomparison.md)
