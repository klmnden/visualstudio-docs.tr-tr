---
title: 'CA1306: Veri türleri için yereli ayarlayın'
ms.date: 11/04/2016
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
ms.openlocfilehash: 893844741c848bee759f56dd027c9976a21902e8
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922784"
---
# <a name="ca1306-set-locale-for-data-types"></a>CA1306: Veri türleri için yereli ayarlayın

|||
|-|-|
|TypeName|SetLocaleForDataTypes|
|CheckId|CA1306|
|Kategori|Microsoft. Globalization|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir yöntem veya Oluşturucu bir veya daha fazla <xref:System.Data.DataTable?displayProperty=fullName> veya <xref:System.Data.DataSet?displayProperty=fullName> örnek oluşturdu ve yerel ayar özelliğini (<xref:System.Data.DataTable.Locale%2A?displayProperty=fullName> veya <xref:System.Data.DataSet.Locale%2A?displayProperty=fullName>) açıkça ayarlamadı.

## <a name="rule-description"></a>Kural açıklaması
Yerel ayar, sayısal değerler, para birimi sembolleri ve sıralama düzeni için kullanılan biçimlendirme gibi veriler için kültüre özgü sunum öğelerini belirler. Bir <xref:System.Data.DataTable> veya<xref:System.Data.DataSet>oluşturduğunuzda yerel ayarı açıkça ayarlamanız gerekir. Varsayılan olarak, bu türlerin yerel ayarı geçerli kültürdür. Bir veritabanında veya dosyada depolanan ve global olarak paylaşılan veriler için, yerel ayar normalde sabit kültür (<xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>) olarak ayarlanmalıdır. Veriler kültürler arasında paylaşıldığında, varsayılan yerel ayarı kullanmak <xref:System.Data.DataTable> veya <xref:System.Data.DataSet> içeriğinin yanlış olarak sunulmasına veya yorumlanmasına neden olabilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, <xref:System.Data.DataTable> veya <xref:System.Data.DataSet>için yerel ayarı açıkça ayarlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Kitaplık veya uygulama sınırlı bir yerel hedef kitle için olduğunda, bu kuraldan gelen bir uyarıyı gizlemek güvenlidir, veriler paylaşılmaz veya varsayılan ayar, tüm desteklenen senaryolarda istenen davranışı verir.

## <a name="example"></a>Örnek
Aşağıdaki örnek iki <xref:System.Data.DataTable> örnek oluşturur.

[!code-csharp[FxCop.Globalization.DataTable#1](../code-quality/codesnippet/CSharp/ca1306-set-locale-for-data-types_1.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Data.DataTable?displayProperty=fullName>
- <xref:System.Data.DataSet?displayProperty=fullName>
- <xref:System.Globalization.CultureInfo?displayProperty=fullName>
- <xref:System.Globalization.CultureInfo.CurrentUICulture%2A?displayProperty=fullName>
- <xref:System.Globalization.CultureInfo.InvariantCulture%2A?displayProperty=fullName>