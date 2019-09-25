---
title: 'CA1054: URI parametreleri dize olmamalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1054
- UriParametersShouldNotBeStrings
helpviewer_keywords:
- CA1054
- UriParametersShouldNotBeStrings
ms.assetid: 8e99d72b-a658-47a7-8dd5-9784ce2c30b8
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 49788b900eb8aed9fac6e4da4844377bae67efbf
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235553"
---
# <a name="ca1054-uri-parameters-should-not-be-strings"></a>CA1054: URI parametreleri dize olmamalıdır

|||
|-|-|
|TypeName|UriParametersShouldNotBeStrings|
|CheckId|CA1054|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür, adı "Uri", "Uri", "urn", "urn", "URL" veya "URL" içeren bir dize parametresine sahip bir yöntem bildirir ve tür, bir <xref:System.Uri?displayProperty=fullName> parametreyi alan karşılık gelen bir aşırı yükleme bildirmiyor.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bu kural, parametre adını ortası kuralı kuralına göre belirteçlere böler ve her belirtecin "Uri", "Uri", "urn", "urn", "URL" veya "URL" olarak eşit olup olmadığını denetler. Bir eşleşme varsa, kural parametrenin bir Tekdüzen Kaynak tanımlayıcısını (URI) temsil ettiğini varsayar. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. Bir yöntem bir URI 'nin dize gösterimini alırsa, bu hizmetleri güvenli ve güvenli bir şekilde sağlayan <xref:System.Uri> sınıfının bir örneğini alan karşılık gelen bir aşırı yükleme sağlanmalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için parametreyi bir <xref:System.Uri> tür olarak değiştirin; bu bir son değişiklik değildir. Alternatif olarak, bir <xref:System.Uri> parametre alan yöntemin aşırı yüklemesini sağlar; Bu, kırılmamış bir değişiklik değildir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Parametresi bir URI 'yi temsil etmediği takdirde bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1054.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı ihlal eden `ErrorProne`bir türü ve kuralını karşılayan bir `SaferWay`türü gösterir.

[!code-csharp[FxCop.Design.UriNotString#1](../code-quality/codesnippet/CSharp/ca1054-uri-parameters-should-not-be-strings_1.cs)]
[!code-vb[FxCop.Design.UriNotString#1](../code-quality/codesnippet/VisualBasic/ca1054-uri-parameters-should-not-be-strings_1.vb)]
[!code-cpp[FxCop.Design.UriNotString#1](../code-quality/codesnippet/CPP/ca1054-uri-parameters-should-not-be-strings_1.cpp)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1056 URI özellikleri dize olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)
- [CA1055 URI dönüş değerleri dize olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)
- [CA2234 Dizeler yerine System. Uri nesnelerini geçirme](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)
- [CA1057 String URI aşırı yüklerini çağırır System. Uri aşırı yüklemeleri](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)