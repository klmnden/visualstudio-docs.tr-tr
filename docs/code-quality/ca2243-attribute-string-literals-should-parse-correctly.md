---
title: 'CA2243: Öznitelik dize harfleri doğru çözümlenmelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2243
- AttributeStringLiteralsShouldParseCorrectly
helpviewer_keywords:
- AttributeStringLiteralsShouldParseCorrectly
- CA2243
ms.assetid: bfadb366-379d-4ee4-b17b-c4a09bf1106b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2627e94dbdd0504b164fee3ecd95dc99b3094db7
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71237827"
---
# <a name="ca2243-attribute-string-literals-should-parse-correctly"></a>CA2243: Öznitelik dize harfleri doğru çözümlenmelidir

|||
|-|-|
|TypeName|AttributeStringLiteralsShouldParseCorrectly|
|CheckId|CA2243|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Özniteliğin dize sabit değeri bir URL, GUID veya sürüm için doğru ayrıştırılmadı.

## <a name="rule-description"></a>Kural açıklaması
Öznitelikleri öğesinden <xref:System.Attribute?displayProperty=fullName>türetildiğinden ve öznitelikleri derleme zamanında kullanıldığından, kurucularına yalnızca sabit değerler geçirilebilir. Bu türler sabitler olarak temsil edilemediğinden, URL 'leri, GUID 'leri ve sürümleri <xref:System.Uri?displayProperty=fullName>temsil <xref:System.Guid?displayProperty=fullName>etmesi gereken <xref:System.Version?displayProperty=fullName>öznitelik parametreleri,, ve olarak türlenemez. Bunun yerine, dizeler tarafından temsil etmelidir.

Parametresi bir dize olarak yazıldığı için, derleme zamanında hatalı biçimlendirilmiş bir parametrenin geçirilmesi mümkündür.

Bu kural bir Tekdüzen Kaynak tanımlayıcısı (URI), bir genel benzersiz tanımlayıcı (GUID) veya sürüm temsil eden parametreleri bulmak için bir adlandırma buluşsal yöntemi kullanır ve geçilen değerin doğru olduğunu doğrular.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Parametre dizesini doğru biçimlendirilmiş bir URL, GUID veya sürüm olarak değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Parametresi bir URL, GUID veya sürüm temsil etmediği takdirde bu kuraldan bir uyarının bastırmasının güvenli hale gelir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden AssemblyFileVersionAttribute için kodu gösterir.

[!code-csharp[FxCop.Usage.AttributeStringLiteralsShouldParseCorrectly#1](../code-quality/codesnippet/CSharp/ca2243-attribute-string-literals-should-parse-correctly_1.cs)]

Kural aşağıdaki parametreler tarafından tetiklenir:

- ' Version ' içeren ve System. Version olarak ayrıştırılabilecek parametreler.

- ' Guid ' içeren ve System. Guid olarak ayrıştırılabilen parametreler.

- ' Uri ', ' urn ' veya ' URL ' içeren parametreler, System. Uri olarak ayrıştırılamıyor.

## <a name="see-also"></a>Ayrıca bkz.

- [CA1054 URI parametreleri dize olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)