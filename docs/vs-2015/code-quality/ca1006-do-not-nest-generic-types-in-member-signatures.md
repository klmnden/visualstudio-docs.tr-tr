---
title: 'CA1006: Üye imzalarında genel türleri iç içe kullanmayın | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- DoNotNestGenericTypesInMemberSignatures
- CA1006
helpviewer_keywords:
- CA1006
- DoNotNestGenericTypesInMemberSignatures
ms.assetid: dfc867bc-f4af-45d7-b071-db04a248f9fc
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: 2c8c35180bdff0b76ee8a66a5e1d27bfd915016c
ms.sourcegitcommit: 08fc78516f1107b83f46e2401888df4868bb1e40
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "65694443"
---
# <a name="ca1006-do-not-nest-generic-types-in-member-signatures"></a>CA1006: Üye imzalarında genel türleri iç içe kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

|||
|-|-|
|TypeName|DoNotNestGenericTypesInMemberSignatures|
|CheckId|CA1006|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir üye iç içe geçmiş tür bağımsız değişkeni içeren bir imza içeriyor.

## <a name="rule-description"></a>Kural Tanımı
 Bir yuvalanmış bağımsız değişken aynı zamanda genel tip olan bir tip bağımsız değişkendir. Yuvalanmış tip bağımsız değişkeni içeren imzası olan bir üye çağırmak için, kullanıcı bir genel tipi örneklemeli ve bu tipi ikinci bir genel tipin yapıcısına geçirmelidir. Gerekli yordam ve sözdizimi karmaşıktır ve kaçınılmalıdır.

## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?
 Bu kural ihlalini düzeltmek için iç içe geçmiş tür bağımsız değişkeni kaldırmak için tasarım değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar Bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Genel türler anlaşılması ve kullanımı kolay bir sözdizimindeki sağlama öğrenmek için gerekli olan ve yeni kitaplıkları benimseme oranını artırır süreyi azaltır.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kuralını ihlal eden bir yöntem ve ihlal eden yöntemini çağırmak için gerekli sözdizimi gösterilir.

 [!code-csharp[FxCop.Design.NestedGenerics#1](../snippets/csharp/VS_Snippets_CodeAnalysis/FxCop.Design.NestedGenerics/cs/FxCop.Design.NestedGenerics.cs#1)]
 [!code-vb[FxCop.Design.NestedGenerics#1](../snippets/visualbasic/VS_Snippets_CodeAnalysis/FxCop.Design.NestedGenerics/vb/FxCop.Design.NestedGenerics.vb#1)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1005: Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)

 [CA1010: Koleksiyonlar genel arabirim uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

 [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

 [CA1002: Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)

 [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

 [CA1003: Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)

 [CA1007: Uygun yerlerde genel türleri kullanın](../code-quality/ca1007-use-generics-where-appropriate.md)

## <a name="see-also"></a>Ayrıca Bkz.
 [Genel Türler](https://msdn.microsoft.com/library/75ea8509-a4ea-4e7a-a2b3-cf72482e9282)
