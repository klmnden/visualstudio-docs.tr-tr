---
title: 'CA1007: Uygun yerlerde genel türleri kullanın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1007
- UseGenericsWhereAppropriate
helpviewer_keywords:
- CA1007
- UseGenericsWhereAppropriate
ms.assetid: eab780ea-3b1f-4d32-b15a-5d48da2df46b
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: ce4f72ba56b27d87d785ca561bad0de6e59dfdc2
ms.sourcegitcommit: 12f2851c8c9bd36a6ab00bf90a020c620b364076
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2019
ms.locfileid: "66744775"
---
# <a name="ca1007-use-generics-where-appropriate"></a>CA1007: Uygun yerlerde genel türleri kullanın

|||
|-|-|
|TypeName|UseGenericsWhereAppropriate|
|CheckId|CA1007|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Türü bir başvuru parametresi dışarıdan görünen bir yöntem içeren <xref:System.Object?displayProperty=fullName>, ve .NET Framework 2. 0'ı hedef alan derlemeyi içeren.

## <a name="rule-description"></a>Kural açıklaması
 Bir başvuru parametresi kullanılarak değiştirilebilir bir parametredir `ref` (`ByRef` içinde [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]) anahtar sözcüğü. Bir başvuru parametresi için sağlanan bağımsız değişken türü başvuru parametresi türünü tam olarak eşleşmelidir. Başvuru parametre türünden türetilmiş bir tür kullanmak için türü ilk dönüştürme ve başvuru parametresi türünü bir değişkene atanır. Genel yöntem tüm türleri ve başvuru parametresi türünü türüne atmadan yönteme iletilecek kısıtlamaları, izin verir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için yöntem genel yapın ve Değiştir <xref:System.Object> bir tür parametresini kullanarak parametre.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, jenerik olmayan ve genel yöntemler olarak uygulanan bir genel amaçlı takas yordam gösterir. Jenerik olmayan bir yönteme göre genel yöntemini kullanarak dizeleri nasıl verimli bir şekilde değiştirilir unutmayın.

 [!code-vb[FxCop.Design.UseGenerics#1](../code-quality/codesnippet/VisualBasic/ca1007-use-generics-where-appropriate_1.vb)]
 [!code-csharp[FxCop.Design.UseGenerics#1](../code-quality/codesnippet/CSharp/ca1007-use-generics-where-appropriate_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA1005: Genel türlerde aşırı parametrelerden kaçının](../code-quality/ca1005-avoid-excessive-parameters-on-generic-types.md)

 [CA1010: Koleksiyonlar genel arabirim uygulamalıdır](../code-quality/ca1010-collections-should-implement-generic-interface.md)

 [CA1000: Genel türlerde statik üyeleri bildirmeyin](../code-quality/ca1000-do-not-declare-static-members-on-generic-types.md)

 [CA1002: Genel listeleri gösterme](../code-quality/ca1002-do-not-expose-generic-lists.md)

 [CA1006: Üye imzalarında genel türleri iç içe kullanmayın](../code-quality/ca1006-do-not-nest-generic-types-in-member-signatures.md)

 [CA1004: Genel metotlar tür parametresi sağlamalıdır](../code-quality/ca1004-generic-methods-should-provide-type-parameter.md)

 [CA1003: Genel olay işleyici örnekleri kullan](../code-quality/ca1003-use-generic-event-handler-instances.md)

## <a name="see-also"></a>Ayrıca bkz.
 [Genel Türler](/dotnet/csharp/programming-guide/generics/index)