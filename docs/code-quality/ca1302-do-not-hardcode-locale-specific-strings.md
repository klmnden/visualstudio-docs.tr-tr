---
title: 'CA1302: Yerel özel dizeleri doğrudan programın içine gömmeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotHardcodeLocaleSpecificStrings
- CA1302
helpviewer_keywords:
- DoNotHardcodeLocaleSpecificStrings
- CA1302
ms.assetid: 05ed134a-837d-43d7-bf97-906edeac44ce
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 69b6256f2c6ae54467eb21cc17d50119b3c67a9f
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235183"
---
# <a name="ca1302-do-not-hardcode-locale-specific-strings"></a>CA1302: Yerel özel dizeleri doğrudan programın içine gömmeyin

|||
|-|-|
|TypeName|DoNotHardcodeLocaleSpecificStrings|
|CheckId|CA1302|
|Kategori|Microsoft. Globalization|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Bir yöntem, belirli sistem klasörlerinin yolunun bir bölümünü temsil eden bir dize sabiti kullanır.

## <a name="rule-description"></a>Kural açıklaması
<xref:System.Environment.SpecialFolder?displayProperty=fullName> Sabit Listesi özel sistem klasörlerine başvuran Üyeler içerir. Bu klasörlerin konumları farklı işletim sistemlerinde farklı değerlere sahip olabilir, Kullanıcı konumların bazılarını değiştirebilir ve konumlar yerelleştirilir. Özel bir klasöre örnek olarak "C:\WINDOWS\system32 [!INCLUDE[winxp](../code-quality/includes/winxp_md.md)] " ve üzerinde "C:\WINNT\SYSTEM32 [!INCLUDE[win2kfamily](../code-quality/includes/win2kfamily_md.md)]" olan sistem klasörü bulunur. Yöntemi, <xref:System.Environment.SpecialFolder> numaralandırmada ilişkili konumları döndürür. <xref:System.Environment.GetFolderPath%2A?displayProperty=fullName> Tarafından <xref:System.Environment.GetFolderPath%2A> döndürülen konumlar yerelleştirilmiştir ve çalışmakta olan bilgisayar için uygundur.

Bu kural, <xref:System.Environment.GetFolderPath%2A> metodu ayrı Dizin düzeylerine kullanarak alınan klasör yollarını simgeleştirir. Her dize sabit değeri belirteçlerle karşılaştırılır. Bir eşleşme bulunursa, yöntemin belirteçle ilişkili sistem konumuna başvuran bir dize oluşturmakta olduğu varsayılır. Taşınabilirlik ve Yerelleştirilebilirlik için, dize sabit <xref:System.Environment.GetFolderPath%2A> değerlerini kullanmak yerine özel sistem klasörlerinin konumlarını almak için yöntemini kullanın.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, <xref:System.Environment.GetFolderPath%2A> yöntemini kullanarak konumu alın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Dize sabit değeri, <xref:System.Environment.SpecialFolder> numaralandırmada ilişkili sistem konumlarından birine başvurmak için kullanılmıyorsa, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuraldan üç uyarı üreten ortak uygulama verileri klasörünün yolunu oluşturur. Daha sonra örnek, <xref:System.Environment.GetFolderPath%2A> yöntemini kullanarak yolunu alır.

[!code-csharp[FxCop.Globalization.HardcodedLocaleStrings#1](../code-quality/codesnippet/CSharp/ca1302-do-not-hardcode-locale-specific-strings_1.cs)]
[!code-vb[FxCop.Globalization.HardcodedLocaleStrings#1](../code-quality/codesnippet/VisualBasic/ca1302-do-not-hardcode-locale-specific-strings_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA1303 Sabit değerleri yerelleştirilmiş parametreler olarak geçirmeyin](../code-quality/ca1303-do-not-pass-literals-as-localized-parameters.md)