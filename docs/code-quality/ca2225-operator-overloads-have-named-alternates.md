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
ms.openlocfilehash: c027bc4581919f814b4d93eacba77248349fdf8b
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231082"
---
# <a name="ca2225-operator-overloads-have-named-alternates"></a>CA2225: İşleç aşırı yüklemeleri adlandırılmış alternatiflere sahiptir

|||
|-|-|
|TypeName|OperatorOverloadsHaveNamedAlternates|
|CheckId|CA2225|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir işleç aşırı yüklemesi algılandı ve beklenen adlandırılmış alternatif yöntem bulunamadı.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

İşleç aşırı yüklemesi, bir tür için hesaplamaları göstermek üzere simgelerin kullanılmasına izin verir. Örneğin, ek için artı simgesini (+) aşırı yükleyen bir tür, genellikle ' Add ' adlı alternatif bir üyeye sahip olur. Adlandırılmış alternatif üye, işleçle aynı işlevselliğe erişim sağlar ve aşırı yüklenmiş işleçleri desteklemeyen dillerde programlayan geliştiriciler için sağlanır.

Bu kural, aşağıdaki tabloda listelenen işleçleri inceler.

|C#|Visual Basic|C++|Alternatif ad|
|---------|------------------|-----------|--------------------|
|+ (ikili)|+|+ (ikili)|Ekle|
|+=|+=|+=|Ekle|
|&|And|&|Bitwiseve|
|&=|Ve =|&=|Bitwiseve|
|&#124;|Veya|&#124;|Bitwiseveya|
|&#124;=|Or =|&#124;=|Bitwiseveya|
|--|Yok|--|Azaltma|
|/|/|/|Sayısına|
|/=|/=|/=|Sayısına|
|==|=|==|Eşittir|
|^|XOR|^|XOR|
|^=|XOR =|^=|XOR|
|>|>|>|{1&gt;Karşılaştır&lt;1}|
|>=|>=|>=|{1&gt;Karşılaştır&lt;1}|
|++|Yok|++|Ilamadı|
|<>|!=|Eşittir|
|<<|<<|<<|Leftshıft|
|<<=|<<=|<<=|Leftshıft|
|<|<|<|{1&gt;Karşılaştır&lt;1}|
|<=|<=|\<=|{1&gt;Karşılaştır&lt;1}|
|&&|Yok|&&|LogicalAnd|
|&#124;&#124;|Yok|&#124;&#124;|LogicalOr|
|!|Yok|!|LogicalNot|
|%|Mod|%|Mod veya geri kalanı|
|%=|Yok|%=|Mod|
|* (ikili)|*|*|Bilirsiniz|
|*=|Yok|*=|Bilirsiniz|
|~|değil|~|Onestamamlayıcısı|
|>>|>>|>>|Sağa kaydırma|
=|Yok|>>=|Sağa kaydırma|
|-(ikili)|-(ikili)|-(ikili)|Çıkarma|
|-=|Yok|-=|Çıkarma|
|true|IsTrue|Yok|IsTrue (özellik)|
|-(birli)|Yok|-|Negate|
|+ (birli)|Yok|+|Artı|
|false|IsFalse|False|IsTrue (özellik)|

Seçili dilde N/A = = aşırı yüklenemez.

Kural Ayrıca, ve`SomeType` `ToSomeType` `FromSomeType`adlı yöntemleri denetleyerek bir tür () içinde örtük ve açık tür dönüştürme işleçlerini da kontrol eder.

' C#De, bir ikili işleç aşırı yüklendiğinde, varsa karşılık gelen atama işleci de dolaylı olarak aşırı yüklenmiştir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, işleci için alternatif yöntemi uygulayın; Önerilen alternatif adı kullanarak adlandırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Paylaşılan bir kitaplık uygulamadıysanız bu kuraldan bir uyarıyı bastırmayın. Uygulamalar bu kuraldan bir uyarıyı yok sayabilir.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca2225.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (kullanım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı ihlal eden bir yapıyı tanımlar. Örneği düzeltmek için, yapıya ortak `Add(int x, int y)` bir yöntem ekleyin.

[!code-csharp[FxCop.Usage.OperatorOverloadsHaveNamedAlternates#1](../code-quality/codesnippet/CSharp/ca2225-operator-overloads-have-named-alternates_1.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1046 Eşittir işlecini başvuru türlerinde aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)
- [CA2226 İşleçler, simetrik aşırı yüklemeleri içermelidir](../code-quality/ca2226-operators-should-have-symmetrical-overloads.md)
- [CA2224 Aşırı yükleme işlecinin eşittir ile eşittir geçersiz kıl](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2218 Geçersiz kılma için GetHashCode geçersiz kılma](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)
- [CA2231 ValueType. Equals geçersiz kılınırken aşırı yükleme işleci Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)