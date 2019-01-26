---
title: 'CA1306: Veri türleri için yereli ayarlayın'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1306
- SetLocaleForDataTypes
helpviewer_keywords:
- CA1306
- SetLocaleForDataTypes
ms.assetid: 104297b2-5806-4de0-a8d9-c589380a796c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: aa74ce81e7923115cf4fa07aba26be171e187690
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54946561"
---
# <a name="ca1306-set-locale-for-data-types"></a>CA1306: Veri türleri için yereli ayarlayın

|||
|-|-|
|TypeName|SetLocaleForDataTypes|
|CheckId|CA1306|
|Kategori|Microsoft.Globalization|
|Yeni Değişiklik|Bölünemez|

## <a name="cause"></a>Sebep
 Yöntem veya Oluşturucu oluşturulan bir veya daha fazla <xref:System.Data.DataTable?displayProperty=fullName> veya <xref:System.Data.DataSet?displayProperty=fullName> örnekler ve yerel ayar özelliğini açıkça ayarlamamış (<xref:System.Data.DataTable.Locale%2A?displayProperty=fullName> veya <xref:System.Data.DataSet.Locale%2A?displayProperty=fullName>).

## <a name="rule-description"></a>Kural açıklaması
 Yerel ayar sayısal değerleri, para birimi simgeleri ve sıralama için kullanılan biçimlendirme gibi veriler için kültüre özgü sunu öğelerini belirler. Oluştururken bir <xref:System.Data.DataTable> veya <xref:System.Data.DataSet>, yerel ayarı açık olarak ayarlamanız gerekir. Varsayılan olarak, bu tür için bir yerel ayar geçerli kültür ' dir. Bir veritabanı veya dosya depolanır ve genel olarak paylaşılan veri yerel ayarı normalde sabit kültür için ayarlanmalıdır (<xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>). Varsayılan yerel ayarı kullanarak veri kültürler arası paylaşıldığında içeriğini açabilir <xref:System.Data.DataTable> veya <xref:System.Data.DataSet> sunulan ya da yanlış yorumlanır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için açık yerel olarak <xref:System.Data.DataTable> veya <xref:System.Data.DataSet>.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Kitaplık veya uygulama yerel sınırlı bir kitle için olduğunda, veriler paylaşılmayan veya varsayılan ayar tüm desteklenen senaryolar istenen davranışı verir. Bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek iki oluşturur <xref:System.Data.DataTable> örnekleri.

 [!code-csharp[FxCop.Globalization.DataTable#1](../code-quality/codesnippet/CSharp/ca1306-set-locale-for-data-types_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Data.DataTable?displayProperty=fullName>
- <xref:System.Data.DataSet?displayProperty=fullName>
- <xref:System.Globalization.CultureInfo?displayProperty=fullName>
- <xref:System.Globalization.CultureInfo.CurrentUICulture%2A?displayProperty=fullName>
- <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>