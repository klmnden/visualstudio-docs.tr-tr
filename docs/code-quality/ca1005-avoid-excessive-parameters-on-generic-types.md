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
ms.openlocfilehash: 0f206d7f02fff2b7e1c1a373ab06bb7462b48705
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55924581"
---
# <a name="ca1005-avoid-excessive-parameters-on-generic-types"></a>CA1005: Genel türlerde aşırı parametre kullanmaktan kaçının

|||
|-|-|
|TypeName|AvoidExcessiveParametersOnGenericTypes|
|CheckId|CA1005|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir genel tür, ikiden fazla tür parametresine sahip.

## <a name="rule-description"></a>Kural açıklaması
 Daha çok tip parametresi, genel tip içerir, bilmek daha zordur ve hangi tip parametrelerinin temsil ettiğini anımsamak zordur. Bu genellikle görüldüğü tek tip parametre ile açıktır `List<T>`ve bazı durumlarda görüldüğü gibi iki tip parametre ile `Dictionary<TKey, TValue>`. İkiden fazla tür parametreleri varsa zorluk çoğu kullanıcı için çok büyük hale gelir (örneğin, `TooManyTypeParameters<T, K, V>` C# veya `TooManyTypeParameters(Of T, K, V)` içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]).

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için ikiden fazla tür parametreleri kullanmak bir tasarım değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Tasarım kesinlikle ikiden fazla tür parametreleri gerektirmediği sürece bu kuraldan bir uyarıyı bastırmayın. Genel türler anlaşılması ve kullanımı kolay bir sözdizimindeki sağlama öğrenmek için gerekli olan ve yeni kitaplıkları benimseme oranını artırır süreyi azaltır.

## <a name="related-rules"></a>İlgili kuralları
 [CA1010: Koleksiyonlar genel arabirim uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

 [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

 [CA1002: Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)

 [CA1006: Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)

 [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

 [CA1003: Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)

 [CA1007: Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.
 [Genel Türler](/dotnet/csharp/programming-guide/generics/index)