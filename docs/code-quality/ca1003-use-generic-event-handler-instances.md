---
title: 'CA1003: Genel olay işleyici örnekleri kullan'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
manager: douge
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 26630aa008e944f0af3fdcc66a16dc4c08bd4e8b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53887342"
---
# <a name="ca1003-use-generic-event-handler-instances"></a>CA1003: Genel olay işleyici örnekleri kullan

|||
|-|-|
|TypeName|UseGenericEventHandlerInstances|
|CheckId|CA1003|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Void döndüren, imzası iki parametre (Birincisi nesne ve ikincisi Eventargs'a atanamaz türü) ve içeren derleme hedefleri içeren bir temsilci türü içeren [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)].

## <a name="rule-description"></a>Kural açıklaması
 Önce [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)]olay işleyicisine özel bilgi geçirmek için yeni bir temsilci öğesinden türetilen bir sınıf belirtilen bildirilmesi gerekiyordu <xref:System.EventArgs?displayProperty=fullName> sınıfı. Bu artık geçerlidir [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)], sunulan <xref:System.EventHandler%601?displayProperty=fullName> temsilci. Bu genel temsilcinin türetilen herhangi bir sınıf sağlar <xref:System.EventArgs> olay işleyicisi ile birlikte kullanılacak.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için temsilci kaldırın ve kullanımını koyacağınız <xref:System.EventHandler%601?displayProperty=fullName> temsilci. Temsilci tarafından otomatik olarak oluşturulan ise [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] derleyici, olay bildirimi, kullanılacak söz dizimi değiştirilebilir <xref:System.EventHandler%601?displayProperty=fullName> temsilci.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, kuralını ihlal eden bir temsilci gösterir. İçinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] örnek, Yorumlar kural karşılamak için örnek değiştirmek nasıl açıklanmaktadır. C# örnek için değiştirilen kodunu gösteren bir örnek izler.

 [!code-vb[FxCop.Design.CustomEventHandler#1](../code-quality/codesnippet/VisualBasic/ca1003-use-generic-event-handler-instances_1.vb)]
 [!code-csharp[FxCop.Design.CustomEventHandler#1](../code-quality/codesnippet/CSharp/ca1003-use-generic-event-handler-instances_1.cs)]

## <a name="example"></a>Örnek
 Aşağıdaki örnek, önceki örnekte, kural karşılar ve kullanımını değiştirir temsilci bildirimi kaldırır. `ClassThatRaisesEvent` ve `ClassThatHandlesEvent` yöntemleri kullanarak <xref:System.EventHandler%601?displayProperty=fullName> temsilci.

 [!code-csharp[FxCop.Design.GenericEventHandler#1](../code-quality/codesnippet/CSharp/ca1003-use-generic-event-handler-instances_2.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1005: Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)

 [CA1010: Koleksiyonlar genel arabirim uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

 [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

 [CA1002: Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)

 [CA1006: Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)

 [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

 [CA1007: Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Genel Türler](/dotnet/csharp/programming-guide/generics/index)