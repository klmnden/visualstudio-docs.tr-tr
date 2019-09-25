---
title: 'CA1003: Genel olay işleyicisi örnekleri kullan'
ms.date: 03/11/2019
ms.topic: reference
f1_keywords:
- UseGenericEventHandlerInstances
- CA1003
helpviewer_keywords:
- CA1003
- UseGenericEventHandlerInstances
ms.assetid: 402101b6-555d-4cf7-b223-1d9fdfaaf1cd
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c654da177e4a9cf820887cf74977a4c3da5a57b6
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236655"
---
# <a name="ca1003-use-generic-event-handler-instances"></a>CA1003: Genel olay işleyicisi örnekleri kullan

|||
|-|-|
|TypeName|UseGenericEventHandlerInstances|
|CheckId|CA1003|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür, void döndüren ve imzası iki parametre (ilk bir nesne ve ikinci bir tür EventArgs 'a atanabilen bir tür) içeren bir temsilci içerir ve kapsayan derleme .NET ' i hedefler.

Bu kural varsayılan olarak yalnızca dışarıdan görünür türlere bakar, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

.NET öncesinde, özel bilgileri olay işleyicisine geçirmek için, <xref:System.EventArgs?displayProperty=fullName> sınıftan türetilmiş bir sınıf belirtilmiş yeni bir temsilcinin bildirilmesini gerekiyordu. .Net ' te, genel <xref:System.EventHandler%601?displayProperty=fullName> temsilci, ' den <xref:System.EventArgs> türetilmiş tüm sınıfın olay işleyicisiyle birlikte kullanılmasına izin verir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için temsilciyi kaldırın ve <xref:System.EventHandler%601?displayProperty=fullName> temsilciyi kullanarak kullanımını değiştirin.

Temsilci Visual Basic Derleyicisi tarafından otomatik olarak oluşturulduğunda, <xref:System.EventHandler%601?displayProperty=fullName> temsilciyi kullanmak için olay bildiriminin sözdizimini değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="configurability"></a>Yapılandırılabilirlik

Bu kuralı [FxCop çözümleyicilerinin](install-fxcop-analyzers.md) (eski analizler olmadan) çalıştırıyorsanız, kod tabanınızın hangi bölümlerinin bu kuralı çalıştırmak için erişilebilirliğini temel alarak yapılandırabilirsiniz. Örneğin, kuralın yalnızca genel olmayan API yüzeyine karşı çalışması gerektiğini belirtmek için, aşağıdaki anahtar-değer çiftini projenizdeki bir. editorconfig dosyasına ekleyin:

```ini
dotnet_code_quality.ca1003.api_surface = private, internal
```

Bu seçeneği yalnızca bu kural için, tüm kurallar için veya bu kategorideki tüm kurallar (tasarım) için yapılandırabilirsiniz. Daha fazla bilgi için bkz. [FxCop çözümleyicileri yapılandırma](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralı ihlal eden bir temsilciyi gösterir. Visual Basic örnekte, açıklamalar, kuralı karşılamak için örneğin nasıl değiştirileceği açıklanır. C# Örnek için, değiştirilen kodu gösteren bir örnek aşağıda verilmiştir.

[!code-vb[FxCop.Design.CustomEventHandler#1](../code-quality/codesnippet/VisualBasic/ca1003-use-generic-event-handler-instances_1.vb)]
[!code-csharp[FxCop.Design.CustomEventHandler#1](../code-quality/codesnippet/CSharp/ca1003-use-generic-event-handler-instances_1.cs)]

Aşağıdaki kod parçacığı, kuralını karşılayan önceki örnekteki temsilci bildirimini kaldırır. Bu, `ClassThatRaisesEvent` ve `ClassThatHandlesEvent` yöntemlerinde kullanımını <xref:System.EventHandler%601?displayProperty=fullName> temsilciyi kullanarak değiştirir.

[!code-csharp[FxCop.Design.GenericEventHandler#1](../code-quality/codesnippet/CSharp/ca1003-use-generic-event-handler-instances_2.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA1005 Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)
- [CA1010 Koleksiyonlar genel arabirimi uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)
- [CA1000 Genel türlerde statik üye bildirme](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)
- [CA1002 Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)
- [CA1006 Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)
- [CA1004 Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)
- [CA1007 Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Genel Türler](/dotnet/csharp/programming-guide/generics/index)