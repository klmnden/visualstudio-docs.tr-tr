---
title: 'CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1057
- StringUriOverloadsCallSystemUriOverloads
helpviewer_keywords:
- StringUriOverloadsCallSystemUriOverloads
- CA1057
ms.assetid: ef1e983e-9ca7-404b-82d7-65740ba0ce20
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 41d3db6e4807c77236868e3ab5746da971ddce6c
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68922485"
---
# <a name="ca1057-string-uri-overloads-call-systemuri-overloads"></a>CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır

|||
|-|-|
|TypeName|StringUriOverloadsCallSystemUriOverloads|
|CheckId|CA1057|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir tür, yalnızca bir <xref:System.Uri?displayProperty=fullName> parametre içeren bir dize parametresinin yerine geçen ve dize parametresini alan aşırı yükleme, <xref:System.Uri> parametreyi alan aşırı yüklemeyi çağırmayan Yöntem yüklerini bildirir.

## <a name="rule-description"></a>Kural açıklaması
Aşırı yüklemeler yalnızca dize veya <xref:System.Uri> parametre tarafından farklı olduğundan, dize bir Tekdüzen Kaynak tanımlayıcısını (URI) temsil edecek şekilde kabul edilir. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. <xref:System.Uri> Sınıfı bu hizmetleri güvenli ve güvenli bir şekilde sağlar. <xref:System.Uri> Sınıfının avantajlarından yararlanmak için, dize aşırı yüklemesi dize bağımsız değişkenini kullanarak <xref:System.Uri> aşırı yüklemeyi çağırmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
URI 'nin dize gösterimini kullanan yöntemi, dize bağımsız değişkenini kullanarak <xref:System.Uri> sınıfın bir örneğini oluşturacak şekilde yeniden uygulayın ve sonra <xref:System.Uri> nesneyi <xref:System.Uri> parametresi olan aşırı yüklemeye geçirir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Dize parametresi bir URI 'yi temsil etmediği takdirde bu kuraldan bir uyarının bastırmasının güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, doğru şekilde uygulanan bir dize aşırı yüklemesini göstermektedir.

[!code-csharp[FxCop.Design.CallUriOverload#1](../code-quality/codesnippet/CSharp/ca1057-string-uri-overloads-call-system-uri-overloads_1.cs)]
[!code-cpp[FxCop.Design.CallUriOverload#1](../code-quality/codesnippet/CPP/ca1057-string-uri-overloads-call-system-uri-overloads_1.cpp)]
[!code-vb[FxCop.Design.CallUriOverload#1](../code-quality/codesnippet/VisualBasic/ca1057-string-uri-overloads-call-system-uri-overloads_1.vb)]

## <a name="related-rules"></a>İlgili kurallar
[CA2234 Dizeler yerine System. Uri nesnelerini geçirme](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)

[CA1056 URI özellikleri dize olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)

[CA1054 URI parametreleri dize olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)

[CA1055 URI dönüş değerleri dize olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)