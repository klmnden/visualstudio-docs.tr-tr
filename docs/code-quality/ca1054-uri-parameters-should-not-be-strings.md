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
ms.openlocfilehash: 03d850eeb668f6c2b47d663b55e5461cabf9cbbf
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "57867467"
---
# <a name="ca1054-uri-parameters-should-not-be-strings"></a>CA1054: URI parametreleri dize olmamalıdır

|||
|-|-|
|TypeName|UriParametersShouldNotBeStrings|
|CheckId|CA1054|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Adında "URI", "Uri", "urn", "Urn", "url" veya "Url" içeren bir dize parametresi olan bir yöntem bir tür bildirir ve türü alan karşılık gelen aşırı bildirmiyor bir <xref:System.Uri?displayProperty=fullName> parametresi.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Bu kural, parametre adı belirteçleri camel casing standardına göre ayıran ve her belirteç "URI", "Uri", "urn", "Urn", "url" veya "Url" eşit olup olmadığını denetler. Bir eşleşme varsa, kural parametresi bir Tekdüzen Kaynak Tanımlayıcısı (URI) temsil ettiğini varsayar. Bir URI'nın dize sunumu ayrıştırma ve hataları kodlama eğilimindedir ve güvenlik açıklarına yol açabilir. Örneğini alan sağlanan URI dize gösterimi bir yöntemi alır, karşılık gelen aşırı olmalıdır <xref:System.Uri> bu hizmetleri güvenli bir şekilde sağlar sınıfını.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için parametreyi değiştirmek bir <xref:System.Uri> yazın; bir değişiklik budur. Alternatif olarak, alan yönteminin bir aşırı yüklemesini sağlayan bir <xref:System.Uri> parametre; bu hataya neden olmayan bir değişikliktir.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Parametre bir URI temsil etmiyorsa bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1054.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bir tür gösterir `ErrorProne`, bu kuralı ve bir tür ihlal `SaferWay`, bu kural karşılar.

[!code-csharp[FxCop.Design.UriNotString#1](../code-quality/codesnippet/CSharp/ca1054-uri-parameters-should-not-be-strings_1.cs)]
[!code-vb[FxCop.Design.UriNotString#1](../code-quality/codesnippet/VisualBasic/ca1054-uri-parameters-should-not-be-strings_1.vb)]
[!code-cpp[FxCop.Design.UriNotString#1](../code-quality/codesnippet/CPP/ca1054-uri-parameters-should-not-be-strings_1.cpp)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1056: URI özellikleri dizeler olmamalıdır](../code-quality/ca1056-uri-properties-should-not-be-strings.md)
- [CA1055: URI dönüş değerleri dizeler olmamalıdır](../code-quality/ca1055-uri-return-values-should-not-be-strings.md)
- [CA2234: Dizeler yerine System.Uri nesneleri geçirin](../code-quality/ca2234-pass-system-uri-objects-instead-of-strings.md)
- [CA1057: String URI aşırı yüklemeleri System.Uri aşırı yüklemelerini çağırır](../code-quality/ca1057-string-uri-overloads-call-system-uri-overloads.md)