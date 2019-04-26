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
ms.openlocfilehash: eff7b4b880526909c293e16aa32ae7045bcdf297
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62780040"
---
# <a name="ca1003-use-generic-event-handler-instances"></a>CA1003: Genel olay işleyicisi örnekleri kullan

|||
|-|-|
|TypeName|UseGenericEventHandlerInstances|
|CheckId|CA1003|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür, imzası iki parametre (Birincisi nesne ve ikincisi Eventargs'a atanamaz türü) ve içeren derleme hedefleri .NET içerir ve void döndüren bir temsilci içerir.

Varsayılan olarak, bu kural yalnızca dışarıdan görülebilen türler görünür, ancak bu [yapılandırılabilir](#configurability).

## <a name="rule-description"></a>Kural açıklaması

.NET önce olay işleyicisine özel bilgi geçirmek için yeni bir temsilci öğesinden türetilen bir sınıf belirtilen bildirilmesi gerekiyordu <xref:System.EventArgs?displayProperty=fullName> sınıfı. Bu artık .NET içinde geçerli değildir. .NET Framework sunulan <xref:System.EventHandler%601?displayProperty=fullName> temsilci, türetilen herhangi bir sınıf izin veren bir genel temsilci <xref:System.EventArgs> olay işleyicisi ile birlikte kullanılacak.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için temsilci kaldırın ve kullanımını koyacağınız <xref:System.EventHandler%601?displayProperty=fullName> temsilci.

Visual Basic derleyici tarafından otomatik olarak oluşturulan temsilci ise olay bildirimi, kullanılacak söz dizimi değiştirilebilir <xref:System.EventHandler%601?displayProperty=fullName> temsilci.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu kuraldan uyarıyı bastırmayın.

## <a name="configurability"></a>Etkiler ve yapılandırma

Bu kuraldan çalıştırıyorsanız [FxCop Çözümleyicileri](install-fxcop-analyzers.md) (ve statik kod analizi üzerinden değil), hangi parçalarının yapılandırabilirsiniz, bu kuralı çalıştırmak için kod tabanı, kendi erişilebilirliği temel. Örneğin, kural yalnızca genel olmayan API yüzeyi karşı çalışması gerektiğini belirtmek için projenizi bir .editorconfig dosyasında şu anahtar-değer çifti ekleyin:

```
dotnet_code_quality.ca1003.api_surface = private, internal
```

Bu kategoride (tasarımı), bu seçenek yalnızca bu kural, tüm kuralları veya tüm kuralları yapılandırabilirsiniz. Daha fazla bilgi için [yapılandırma FxCop Çözümleyicileri](configure-fxcop-analyzers.md).

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralını ihlal eden bir temsilci gösterir. Visual Basic örnek kural karşılamak için örnek değiştirme açıklamaları açıklanmaktadır. C# örnek için değiştirilen kodunu gösteren bir örnek izler.

[!code-vb[FxCop.Design.CustomEventHandler#1](../code-quality/codesnippet/VisualBasic/ca1003-use-generic-event-handler-instances_1.vb)]
[!code-csharp[FxCop.Design.CustomEventHandler#1](../code-quality/codesnippet/CSharp/ca1003-use-generic-event-handler-instances_1.cs)]

Aşağıdaki kod parçacığı, kural karşılayan önceki örnekte, temsilci bildirimi kaldırır. Kullanımını değiştirir `ClassThatRaisesEvent` ve `ClassThatHandlesEvent` yöntemleri kullanarak <xref:System.EventHandler%601?displayProperty=fullName> temsilci.

[!code-csharp[FxCop.Design.GenericEventHandler#1](../code-quality/codesnippet/CSharp/ca1003-use-generic-event-handler-instances_2.cs)]

## <a name="related-rules"></a>İlgili kuralları

- [CA1005: Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)
- [CA1010: Koleksiyonlar genel arabirim uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)
- [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)
- [CA1002: Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)
- [CA1006: Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)
- [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)
- [CA1007: Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Genel Türler](/dotnet/csharp/programming-guide/generics/index)