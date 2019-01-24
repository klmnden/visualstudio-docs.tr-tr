---
title: 'CA1055: URI dönüş değerleri dizeler olmamalıdır | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA1055
- UriReturnValuesShouldNotBeStrings
helpviewer_keywords:
- UriReturnValuesShouldNotBeStrings
- CA1055
ms.assetid: 40e39873-7872-4988-8195-9eb0ade9ece0
caps.latest.revision: 15
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 1b1cc26b0cd2884957a670b9c3aa0af25e51399d
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54753129"
---
# <a name="ca1055-uri-return-values-should-not-be-strings"></a>CA1055: URI dönüş değerleri dize olmamalıdır
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|UriReturnValuesShouldNotBeStrings|
|CheckId|CA1055|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bir yöntemin adı "uri", "Uri", "urn", "Urn", "url" veya "Url" içeren ve yöntem bir dize döndürür.

## <a name="rule-description"></a>Kural Tanımı
 Bu kural, Pascal casing standardına göre belirteçleri yöntem adı ayıran ve her belirteç "URI", "Uri", "urn", "Urn", "url" veya "Url" eşit olup olmadığını denetler. Bir eşleşme varsa, kural yöntem bir Tekdüzen Kaynak Tanımlayıcısı (URI) döndürür varsayar. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. <xref:System.Uri?displayProperty=fullName> Sınıfı bu hizmetleri güvenli bir biçimde sunar.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için geri dönüş için değiştirme bir <xref:System.Uri>.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Dönüş değeri bir URI temsil etmiyorsa, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir `ErrorProne`, bu kuralı ve bir tür ihlal `SaferWay`, bu kural karşılar.

 [!code-cpp[FxCop.Design.UriNotString#1](../snippets/cpp/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/cpp/FxCop.Design.UriNotString.cpp#1)]
 [!code-csharp[FxCop.Design.UriNotString#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/cs/FxCop.Design.UriNotString.cs#1)]
 [!code-vb[FxCop.Design.UriNotString#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.UriNotString/vb/FxCop.Design.UriNotString.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1056: URI özellikleri dizeler olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)

 [CA1054: URI parametreleri dizeler olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)

 [CA2234: Dizeler yerine System.Uri nesneleri geçirin](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)

 [CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)
