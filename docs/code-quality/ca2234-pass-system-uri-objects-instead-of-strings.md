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
ms.openlocfilehash: 97b73793d0c473727960dbde8fe32fc584ff6dd5
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57869212"
---
# <a name="ca2234-pass-systemuri-objects-instead-of-strings"></a>CA2234: Dizeler yerine System.Uri nesneleri gönderin

|||
|-|-|
|TypeName|PassSystemUriObjectsInsteadOfStrings|
|CheckId|CA2234|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Adında "URI", "Uri", "urn", "Urn", "url" veya "Url" içeren bir dize parametresi olan bir yönteme bir çağrı yapılır ve metodun bildirim türü olan bir aşırı yüklemeye uyan yöntemi içerir. bir <xref:System.Uri?displayProperty=fullName> parametresi.

Varsayılan olarak, bu kural yalnızca dışarıdan görünen yöntemi ve türleri görünüyor, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Parametre adları camel casing standardına göre belirteçleri bölün ve ardından her belirteç "URI", "Uri", "urn", "Urn", "url" veya "Url" eşit olup olmadığını görmek için denetlenir. Bir eşleşme varsa, parametre bir Tekdüzen Kaynak Tanımlayıcısı (URI) gösterdiği kabul edilir. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. <xref:System.Uri> Sınıfı bu hizmetleri güvenli bir biçimde sunar. URI ilgili yalnızca farklı iki aşırı yükler arasında bir seçim olduğunda kullanıcı alan aşırı yüklemesini seçmelidir bir <xref:System.Uri> bağımsız değişken.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için alan aşırı yüklemesini çağırmak <xref:System.Uri> bağımsız değişken.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Dize parametresi bir URI temsil etmiyorsa, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca2234.api_surface = private, internal
```

Bu kategoride (kullanım), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek bir yöntemi gösterir `ErrorProne`, kural ve bir yöntem ihlal `SaferWay`, doğru çağrılarının <xref:System.Uri> aşırı yükleme:

[!code-vb[FxCop.Usage.PassUri#1](../code-quality/codesnippet/VisualBasic/ca2234-pass-system-uri-objects-instead-of-strings_1.vb)]
[!code-cpp[FxCop.Usage.PassUri#1](../code-quality/codesnippet/CPP/ca2234-pass-system-uri-objects-instead-of-strings_1.cpp)]
[!code-csharp[FxCop.Usage.PassUri#1](../code-quality/codesnippet/CSharp/ca2234-pass-system-uri-objects-instead-of-strings_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)
- [CA1056: URI özellikleri dizeler olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)
- [CA1054: URI parametreleri dizeler olmamalıdır](../code-quality/ca1054-uri-parameters-should-not-be-strings.md)
- [CA1055: URI dönüş değerleri dizeler olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)