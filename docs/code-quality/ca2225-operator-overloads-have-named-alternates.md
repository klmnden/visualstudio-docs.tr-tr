---
title: 'CA2225: İşleç aşırı yüklemeleri adlandırılmış alternatiflere sahiptir'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- OperatorOverloadsHaveNamedAlternates
- CA2225
helpviewer_keywords:
- OperatorOverloadsHaveNamedAlternates
- CA2225
ms.assetid: af8f7ab1-63ad-4861-afb9-b7a7a2be15e1
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a8a1c7015421b686d47bfea4c3341ec76748f8ad
ms.sourcegitcommit: f7c401a376ce410336846835332a693e6159c551
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/14/2019
ms.locfileid: "57873074"
---
# <a name="ca2225-operator-overloads-have-named-alternates"></a>CA2225: İşleç aşırı yüklemeleri adlandırılmış alternatiflere sahiptir

|||
|-|-|
|TypeName|OperatorOverloadsHaveNamedAlternates|
|CheckId|CA2225|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Operatör aşırı yüklemesi algılandı ve beklenen adlandırılmış Alternatif yöntem bulunamadı.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

İşleç aşırı yüklemesi hesaplamaları için bir türü temsil etmek için semboller kullanımına izin verir. Örneğin, eklenmesi için (+) artı simgesini aşırı bir türü genellikle 'Ekle' adlı alternatif bir üye yoktur. Adlandırılmış alternatif üye işleci ile aynı işlevlere erişim sağlar ve aşırı yüklenmiş operatörlere destek olmayan dilleri içinde program geliştiriciler için sağlanır.

Bu kural aşağıdaki tabloda listelenen işleçlerden inceler.

|C#|Visual Basic|C++|Diğer adı|
|---------|------------------|-----------|--------------------|
|+ (ikili)|+|+ (ikili)|Ekle|
|+=|+=|+=|Ekle|
|&|And|&|BitwiseAnd|
|&=|Ve =|&=|BitwiseAnd|
|&#124;|Or|&#124;|BitwiseOr|
|&#124;=|Veya =|&#124;=|BitwiseOr|
|--|Yok|--|Azaltma|
|/|/|/|Bölme|
|/=|/=|/=|Bölme|
|==|=|==|Eşittir|
|^|Xor|^|Xor|
|^=|Xor =|^=|Xor|
|>|>|>|{1&gt;Karşılaştır&lt;1}|
|>=|>=|>=|{1&gt;Karşılaştır&lt;1}|
|++|Yok|++|Artırma|
|<>|!=|Eşittir|
|<<|<<|<<|LeftShift|
|<<=|<<=|<<=|LeftShift|
|<|<|<|{1&gt;Karşılaştır&lt;1}|
|<=|<=|\<=|{1&gt;Karşılaştır&lt;1}|
|&&|Yok|&&|LogicalAnd|
|&#124;&#124;|Yok|&#124;&#124;|LogicalOr|
|!|Yok|!|LogicalNot|
|%|Mod|%|Mod veya kalan|
|%=|Yok|%=|Mod|
|* (ikili)|*|*|Çarp|
|*=|Yok|*=|Çarp|
|~|değil|~|OnesComplement|
|>>|>>|>>|RightShift|
=|Yok|>>=|RightShift|
|-(ikili)|-(ikili)|-(ikili)|Çıkarma|
|-=|Yok|-=|Çıkarma|
|true|IsTrue|Yok|IsTrue (özellik)|
|-(tekli)|Yok|-|negate|
|+ (tekli)|Yok|+|artı|
|false|IsFalse|False|IsTrue (özellik)|

Yok == seçtiğiniz dilde aşırı yüklenemez.

Kural türü örtük ve açık dönüştürme işleçleri de denetler (`SomeType`) adlı yöntemleri için işaretleyerek `ToSomeType` ve `FromSomeType`.

İkili İşleç aşırı C# ' ta karşılık gelen bir atama işleci varsa, aynı zamanda örtük olarak aşırı yüklenmiş olur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için alternatif yöntem için işleç uygulayın; önerilen alternatif adını kullanarak adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Paylaşılan bir kitaplık uyguluyorsanız, bu kuraldan bir uyarıyı bastırmayın. Uygulamalar bu kuraldan bir uyarıyı yok sayabilirsiniz.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca2225.api_surface = private, internal
```

Bu kategoride (kullanım), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek bu kuralı ihlal eden bir yapı tanımlar. Örnek düzeltmek için bir genel ekleme `Add(int x, int y)` yapısına yöntemi.

[!code-csharp[FxCop.Usage.OperatorOverloadsHaveNamedAlternates#1](../code-quality/codesnippet/CSharp/ca2225-operator-overloads-have-named-alternates_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1046: Başvuru türlerinde eşittir işleçlerini aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)
- [CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)
- [CA2224: Eşittir işlecini aşırı yüklemesi üzerinde geçersiz kılma değerine eşittir](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2218: Gethashcode'u eşittir geçersiz kılmada geçersiz kıl](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)
- [CA2231: Eşittir işlecini ValueType.equals'ı geçersiz kılarak üzerinde](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)