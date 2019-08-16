---
title: 'CA2234: Dizeler yerine System.Uri nesneleri gönderin'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- PassSystemUriObjectsInsteadOfStrings
- CA2234
helpviewer_keywords:
- CA2234
- PassSystemUriObjectsInsteadOfStrings
ms.assetid: 14616b37-74c4-4286-b051-115d00aceb5f
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 74484c5f014c9a677c321a0d9fed649f016ea3c9
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69546876"
---
# <a name="ca2234-pass-systemuri-objects-instead-of-strings"></a>CA2234: Dizeler yerine System.Uri nesneleri gönderin

|||
|-|-|
|TypeName|PassSystemUriObjectsInsteadOfStrings|
|CheckId|CA2234|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Adı "Uri", "Uri", "urn", "urn", "URL" veya "URL", "urn", "URL" veya "URL" içeren bir dize parametresine sahip bir yönteme çağrı yapılır ve yöntemin bildirim türü, bir <xref:System.Uri?displayProperty=fullName> parametreye sahip karşılık gelen bir yöntem aşırı yüklemesini içeriyor.

Bu kural varsayılan olarak yalnızca dışarıdan görünen yöntemlere ve türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bir parametre adı, ortası büyük/küçük harf kuralına göre belirteçlere bölünür ve ardından "Uri", "Uri", "urn", "urn", "URL" veya "URL" olarak eşit olup olmadığını görmek için her belirteç denetlenir. Bir eşleşme varsa parametre bir Tekdüzen Kaynak tanımlayıcısını (URI) temsil eder. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. <xref:System.Uri> Sınıfı bu hizmetleri güvenli ve güvenli bir şekilde sağlar. Yalnızca bir URI gösterimi ile ilgili olan iki aşırı yükleme arasında seçim yapıldığında, Kullanıcı bir <xref:System.Uri> bağımsız değişken alan aşırı yüklemeyi seçmelidir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için <xref:System.Uri> bağımsız değişkenini alan aşırı yüklemeyi çağırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Dize parametresi bir URI 'yi temsil etmediği takdirde bu kuraldan bir uyarının bastırmasının güvenli hale gelir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca2234.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (kullanım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, yeniden `ErrorProne` <xref:System.Uri> yüklemeyi doğru çağıran kuralı ve `SaferWay`yöntemi ihlal eden bir yöntemi gösterir:

[!code-vb[FxCop.Usage.PassUri#1](../code-quality/codesnippet/VisualBasic/ca2234-pass-system-uri-objects-instead-of-strings_1.vb)]
[!code-cpp[FxCop.Usage.PassUri#1](../code-quality/codesnippet/CPP/ca2234-pass-system-uri-objects-instead-of-strings_1.cpp)]
[!code-csharp[FxCop.Usage.PassUri#1](../code-quality/codesnippet/CSharp/ca2234-pass-system-uri-objects-instead-of-strings_1.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1057 String URI aşırı yüklerini çağırır System. Uri aşırı yüklemeleri](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)
- [CA1056 URI özellikleri dize olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)
- [CA1054 URI parametreleri dize olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)
- [CA1055 URI dönüş değerleri dize olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)