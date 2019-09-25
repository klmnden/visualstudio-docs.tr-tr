---
title: "CA1816: GC.SuppressFinalize'ı doğru çağırın"
ms.date: 06/30/2018
ms.topic: reference
f1_keywords:
- CA1816
- DisposeMethodsShouldCallSuppressFinalize
helpviewer_keywords:
- DisposeMethodsShouldCallSuppressFinalize
- CA1816
ms.assetid: 47915fbb-103f-4333-b157-1da16bf49660
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 3fdd20df37586e50b5236872f1d84de48d08c87a
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71233526"
---
# <a name="ca1816-call-gcsuppressfinalize-correctly"></a>CA1816: GC.SuppressFinalize'ı doğru çağırın

|||
|-|-|
|TypeName|CallGCSuppressFinalizeCorrectly|
|CheckId|CA1816|
|Kategori|MICROSOFT. Kullanım|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Bu kuralın ihlalleri şunlar olabilir:

- Bir uygulama <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> olan ve çağırımeyen <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>bir yöntem.

- <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> Ve çağrısı<xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>olmayan bir yöntem.

- [BuC#()](/dotnet/csharp/language-reference/keywords/this) veya <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> [ben (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass#me)dışında bir öğe çağıran ve ileten bir yöntem.

## <a name="rule-description"></a>Kural açıklaması

Yöntemi <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> , kullanıcıların nesne çöp toplama için kullanılabilir hale gelmeden önce kaynakları serbest bırakmasına olanak tanır. <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> Yöntemi çağrılırsa, nesnesinin kaynaklarını boşaltır. Bu, sonlandırılmasını gereksiz hale getirir. <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType><xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> çöp toplayıcı nesnenin sonlandırıcısını çağırmaması için çağrılmalıdır.

Sonlandırıcılarla türetilmiş türlerin yeniden uygulanması <xref:System.IDisposable> ve çağırmasını engellemek için, sonlandırıcılar olmayan korumasız türler yine de çağırmalıdır. <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için:

- Yöntemi bir uygulama <xref:System.IDisposable.Dispose%2A>ise, öğesine <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>bir çağrı ekleyin.

- Yöntemi bir uygulama <xref:System.IDisposable.Dispose%2A>değilse, <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> çağrısını kaldırın ya da türün <xref:System.IDisposable.Dispose%2A> uygulamasına taşıyın.

- [ThisC#()](/dotnet/csharp/language-reference/keywords/this) veya <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> [Me (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass#me)iletmek için tüm çağrıları değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Yalnızca diğer nesnelerin ömrünü denetlemek için kasıtlı olarak kullanıyorsanız <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> , bu kuraldan bir uyarı gizleyin. Bir uygulama <xref:System.IDisposable.Dispose%2A> çağrımazsa <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>bu kuraldan bir uyarıyı bastırmayın. Bu durumda, sonlandırmadan performansı düşürür ve hiçbir avantaj sağlamaz.

## <a name="example-that-violates-ca1816"></a>CA1816 ihlal eden örnek

Bu kod, çağıran <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>bir yöntemi gösterir, ancak [bunu (C#)](/dotnet/csharp/language-reference/keywords/this) veya [beni (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass#me)geçirmez. Sonuç olarak, bu kod CA1816 kuralını ihlal ediyor.

[!code-vb[FxCop.Usage.CallGCSuppressFinalizeCorrectly#1](../code-quality/codesnippet/VisualBasic/ca1816-call-gc-suppressfinalize-correctly_1.vb)]
[!code-csharp[FxCop.Usage.CallGCSuppressFinalizeCorrectly#1](../code-quality/codesnippet/CSharp/ca1816-call-gc-suppressfinalize-correctly_1.cs)]

## <a name="example-that-satisfies-ca1816"></a>CA1816 karşılayan örnek

Bu örnek, <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType> [Bu (C#)](/dotnet/csharp/language-reference/keywords/this) veya [Me (Visual Basic)](/dotnet/visual-basic/programming-guide/program-structure/me-my-mybase-and-myclass#me)geçirerek doğru şekilde çağıran bir yöntemi gösterir.

[!code-vb[FxCop.Usage.CallGCSuppressFinalizeCorrectly2#1](../code-quality/codesnippet/VisualBasic/ca1816-call-gc-suppressfinalize-correctly_2.vb)]
[!code-csharp[FxCop.Usage.CallGCSuppressFinalizeCorrectly2#1](../code-quality/codesnippet/CSharp/ca1816-call-gc-suppressfinalize-correctly_2.cs)]

## <a name="related-rules"></a>İlgili kurallar

- [CA2215 Dispose yöntemleri taban sınıf atmayı çağırmalıdır](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)
- [CA2216 Atılabilir türler sonlandırıcıyı bildirmelidir](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Dispose kriteri](/dotnet/standard/design-guidelines/dispose-pattern)