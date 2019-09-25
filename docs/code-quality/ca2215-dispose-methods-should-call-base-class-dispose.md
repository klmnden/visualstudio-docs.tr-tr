---
title: 'CA2215: Atma metotları taban sınıf atmayı çağırmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2215
- DisposeMethodsShouldCallBaseClassDispose
- Dispose methods should call base class dispose
helpviewer_keywords:
- DisposeMethodsShouldCallBaseClassDispose
- CA2215
ms.assetid: c772e7a6-a87e-425c-a70e-912664ae9042
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 468b63ca554ea126bbd621a2502e54540e6ed068
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231274"
---
# <a name="ca2215-dispose-methods-should-call-base-class-dispose"></a>CA2215: Atma metotları taban sınıf atmayı çağırmalıdır

|||
|-|-|
|TypeName|DisposeMethodsShouldCallBaseClassDispose|
|CheckId|CA2215|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep
Uygulayan <xref:System.IDisposable?displayProperty=fullName> bir tür, Ayrıca uygulayan <xref:System.IDisposable>bir türden devralır. <xref:System.IDisposable.Dispose%2A> Devralan türün <xref:System.IDisposable.Dispose%2A> yöntemi üst tür yöntemini çağırmıyor.

## <a name="rule-description"></a>Kural açıklaması
Bir tür atılabilir bir türden devralırsa, kendi <xref:System.IDisposable.Dispose%2A> <xref:System.IDisposable.Dispose%2A> yönteminin içinde temel türün yöntemini çağırmalıdır. Temel tür metodunu çağırmak, temel tür tarafından oluşturulan kaynakların serbest bırakıldığını sağlar.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için çağrısı `base`yapın.<xref:System.IDisposable.Dispose%2A> <xref:System.IDisposable.Dispose%2A> metodunda.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Çağrısı varsa, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir `base`.<xref:System.IDisposable.Dispose%2A> kural denetimlerinden daha derin bir çağrı düzeyinde gerçekleşir.

## <a name="example"></a>Örnek
Aşağıdaki örnek, uygulayan `TypeA` <xref:System.IDisposable>bir türü gösterir.

[!code-csharp[FxCop.Usage.IDisposablePattern#1](../code-quality/codesnippet/CSharp/ca2215-dispose-methods-should-call-base-class-dispose_1.cs)]

## <a name="example"></a>Örnek
Aşağıdaki örnek, türünden `TypeB` `TypeA` devralan ve <xref:System.IDisposable.Dispose%2A> metodunu doğru şekilde çağıran bir türü gösterir.

[!code-vb[FxCop.Usage.IDisposableBaseCalled#1](../code-quality/codesnippet/VisualBasic/ca2215-dispose-methods-should-call-base-class-dispose_2.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable?displayProperty=fullName>
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)