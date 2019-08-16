---
title: 'CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- OperatorsShouldHaveSymmetricalOverloads
- CA2226
helpviewer_keywords:
- OperatorsShouldHaveSymmetricalOverloads
- CA2226
ms.assetid: d202401a-ea14-4559-b15e-0ea4f5b68789
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 4557b61afab08c7db05c734c6f2ac927a40edb71
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69546858"
---
# <a name="ca2226-operators-should-have-symmetrical-overloads"></a>CA2226: İşleçler simetrik aşırı yüklemelere sahip olmalıdır

|||
|-|-|
|TypeName|OperatorsShouldHaveSymmetricalOverloads|
|CheckId|CA2226|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bir tür, eşitlik ya da eşitsizlik operatörünü uygular ve ters işleci uygulamaz.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Eşitlik veya eşitsizlik bir tür örneklerine uygulanabilir olduğu ve ters işleç tanımsız olduğu durumlar yoktur. Türler, genellikle eşitlik işlecinin negated Value değerini döndürerek eşitsizlik işlecini uygular.

C# Derleyici bu kuralın ihlalleri için bir hata verir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için hem eşitlik hem de eşitsizlik işleçlerini uygulayın veya var olan birini kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Bunu yaparsanız, tipi .NET ile tutarlı bir şekilde çalışmaz.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca2226.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (kullanım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="related-rules"></a>İlgili kurallar

- [CA1046 Eşittir işlecini başvuru türlerinde aşırı yüklemeyin](../code-quality/ca1046-do-not-overload-operator-equals-on-reference-types.md)
- [CA2225 İşleç aşırı yüklemelerinin adlandırılmış alternatifleri var](../code-quality/ca2225-operator-overloads-have-named-alternates.md)
- [CA2224 Aşırı yükleme işlecinin eşittir ile eşittir geçersiz kıl](../code-quality/ca2224-override-equals-on-overloading-operator-equals.md)
- [CA2218 Geçersiz kılma için GetHashCode geçersiz kılma](../code-quality/ca2218-override-gethashcode-on-overriding-equals.md)
- [CA2231 ValueType. Equals geçersiz kılınırken aşırı yükleme işleci Equals](../code-quality/ca2231-overload-operator-equals-on-overriding-valuetype-equals.md)