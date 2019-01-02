---
title: 'CA2243: Öznitelik dize harfleri doğru çözümlenmelidir'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: b6c7aa4638a1a0a863bf53c85a5e182f57a366d8
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53939998"
---
# <a name="ca2243-attribute-string-literals-should-parse-correctly"></a>CA2243: Öznitelik dize harfleri doğru çözümlenmelidir

|||
|-|-|
|TypeName|AttributeStringLiteralsShouldParseCorrectly|
|CheckId|CA2243|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep
 Bir öznitelik dize literal parametresi, bir URL, GUID ya da sürüm için doğru ayrıştırmaz.

## <a name="rule-description"></a>Kural açıklaması
 Öğesinden türetilen öznitelikler bu yana <xref:System.Attribute?displayProperty=fullName>ve öznitelikleri derleme zamanında kullanılan, yalnızca sabit değerler için oluşturucuları geçirilebilir. URL, GUID ve sürümleri temsil etmelidir öznitelik parametreleri olamaz yazılı olarak <xref:System.Uri?displayProperty=fullName>, <xref:System.Guid?displayProperty=fullName>, ve <xref:System.Version?displayProperty=fullName>, bu tür sabitleri temsil edilemez. Bunun yerine, dizeler gösterilmelidir.

 Parametresi bir dize olarak yazıldığından, hatalı biçimlendirilmiş bir parametre derleme zamanında geçirilebilir mümkündür.

 Bu kural, bir Tekdüzen Kaynak Tanımlayıcısı (URI), sürüm veya bir genel benzersiz tanıtıcısı (GUID) temsil eden parametreleri bulmak için bir adlandırma buluşsal kullanır ve geçirilen değerin doğru olduğunu doğrular.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Parametre dizesi düzgün biçimlendirilmiş bir URL, GUID veya sürüm değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 URL, GUID ya da sürüm parametresi temsil etmiyorsa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek bu kuralı ihlal AssemblyFileVersionAttribute için kod gösterir.

 [!code-csharp[FxCop.Usage.AttributeStringLiteralsShouldParseCorrectly#1](../code-quality/codesnippet/CSharp/ca2243-attribute-string-literals-should-parse-correctly_1.cs)]

 Kural aşağıdaki parametreleri tarafından tetiklenir:

- 'Version' içerir ve için System.Version nelze analyzovat parametreler.

- 'GUID' içerir ve System.Guid için ayrıştırılamayan parametre.

- 'Uri', 'urn' veya 'url' içerir ve System.Uri olarak ayrıştırılamıyor. parametreler.

## <a name="see-also"></a>Ayrıca bkz.

- [CA1054: URI parametreleri dizeler olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)