---
title: 'CA1005: Genel türlerde aşırı parametre kullanmaktan kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AvoidExcessiveParametersOnGenericTypes
- CA1005
helpviewer_keywords:
- AvoidExcessiveParametersOnGenericTypes
- CA1005
ms.assetid: 372b2f28-5c59-4815-9753-6c65b2bb3589
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ffc94a04d708315cc143afd1556cb8a2f0072e91
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923293"
---
# <a name="ca1005-avoid-excessive-parameters-on-generic-types"></a>CA1005: Genel türlerde aşırı parametre kullanmaktan kaçının

|||
|-|-|
|TypeName|AvoidExcessiveParametersOnGenericTypes|
|CheckId|CA1005|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Dışarıdan görülebilen genel tür, ikiden fazla tür parametresine sahiptir.

## <a name="rule-description"></a>Kural açıklaması
Daha çok tip parametresi, genel tip içerir, bilmek daha zordur ve hangi tip parametrelerinin temsil ettiğini anımsamak zordur. Genellikle, içinde `List<T>`olduğu gibi tek bir tür parametresiyle ve içinde `Dictionary<TKey, TValue>`olduğu gibi iki tür parametresiyle bazı durumlarda belirgin bir şekilde açıktır. İkiden fazla tür parametresi varsa, zorluk çoğu kullanıcı için çok büyük hale `TooManyTypeParameters<T, K, V>` gelir (örneğin, C# veya `TooManyTypeParameters(Of T, K, V)` içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]).

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için tasarımı, ikiden fazla tür parametresi kullanmak üzere değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Tasarım kesinlikle ikiden fazla tür parametresi gerektirmedikçe bu kuraldan bir uyarıyı bastırmayın. Anlaşılması kolay ve kullanımı kolay bir sözdiziminde genel türler sağlamak, yeni kitaplıkların benimseme oranını öğrenmek ve artmak için gereken süreyi azaltır.

## <a name="related-rules"></a>İlgili kurallar
[CA1010 Koleksiyonlar genel arabirimi uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

[CA1000 Genel türlerde statik üye bildirme](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

[CA1002 Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)

[CA1006 Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)

[CA1004 Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

[CA1003 Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)

[CA1007 Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.
[Genel Türler](/dotnet/csharp/programming-guide/generics/index)