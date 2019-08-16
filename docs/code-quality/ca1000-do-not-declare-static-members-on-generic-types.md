---
title: 'CA1000: Genel türlerde statik üyeler belirtme'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- CA1000
- DoNotDeclareStaticMembersOnGenericTypes
helpviewer_keywords:
- DoNotDeclareStaticMembersOnGenericTypes
- CA1000
ms.assetid: 5c0da594-f8d0-4f40-953d-56bf7fbd2087
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: f10433330642ee06dd7f705cdd8e35333cd8a79d
ms.sourcegitcommit: 209ed0fcbb8daa1685e8d6b9a97f3857a4ce1152
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "69547917"
---
# <a name="ca1000-do-not-declare-static-members-on-generic-types"></a>CA1000: Genel türlerde statik üyeler belirtme

|||
|-|-|
|TypeName|DoNotDeclareStaticMembersOnGenericTypes|
|CheckId|CA1000|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Genel tür bir `static` (`Shared` Visual Basic) üyesine sahiptir.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

Genel türün `static` bir üyesi çağrıldığında tür bağımsız değişkeni türü için belirtilmelidir. Destek çıkarımı desteklenmeyen genel örnek üyesi çağrıldığında tür bağımsız değişkeni üye için belirlenmelidir. Aşağıdaki çağrılar gösterildiği gibi, bu iki durumda tür bağımsız değişkenini belirtmenin sözdizimi farklı ve kolayca karıştırılır:

```vb
' Shared method in a generic type.
GenericType(Of Integer).SharedMethod()

' Generic instance method that does not support inference.
someObject.GenericMethod(Of Integer)()
```

```csharp
// Static method in a generic type.
GenericType<int>.StaticMethod();

// Generic instance method that does not support inference.
someObject.GenericMethod<int>();
```

Genellikle, tür bağımsız değişkeninin üye çağrıldığında belirtilmesi gerekmez, ancak önceki bildirimlerin her ikisi de kaçınılmalıdır. Bu, genel türler için sözdiziminden farklı olmayan genel türlerde üyeleri çağırmaya yönelik bir söz dizimine neden olur. Daha fazla bilgi için bkz [. CA1004: Genel metotlar tür parametresi](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)sağlamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için statik üyeyi kaldırın veya bir örnek üyesine değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Anlaşılması kolay ve kullanımı kolay bir sözdiziminde genel türler sağlamak, yeni kitaplıkların benimseme oranını öğrenmek ve artmak için gereken süreyi azaltır.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1000.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="related-rules"></a>İlgili kurallar

- [CA1005 Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)
- [CA1010 Koleksiyonlar genel arabirimi uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)
- [CA1002 Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)
- [CA1006 Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)
- [CA1004 Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)
- [CA1003 Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)
- [CA1007 Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Genel Türler](/dotnet/csharp/programming-guide/generics/index)