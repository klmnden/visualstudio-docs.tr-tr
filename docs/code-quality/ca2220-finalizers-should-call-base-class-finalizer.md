---
title: 'CA2220: Sonlandırıcılar taban tür sonlandırıcıları çağırmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2220
- FinalizersShouldCallBaseClassFinalizer
helpviewer_keywords:
- CA2220
- FinalizersShouldCallBaseClassFinalizer
ms.assetid: 48329f42-170d-45ee-a381-e33f55a240c5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e5af6b7872f0fa05183334e6acd2bc4922f84990
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71231167"
---
# <a name="ca2220-finalizers-should-call-base-class-finalizer"></a>CA2220: Sonlandırıcılar taban tür sonlandırıcıları çağırmalıdır

|||
|-|-|
|TypeName|FinalizersShouldCallBaseClassFinalizer|
|CheckId|CA2220|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Geçersiz kılan <xref:System.Object.Finalize%2A?displayProperty=fullName> bir tür, <xref:System.Object.Finalize%2A> kendi temel sınıfında yöntemini çağırmaz.

## <a name="rule-description"></a>Kural açıklaması

Sonlandırılma, devralma hiyerarşisi aracılığıyla gönderilmelidir. Bunun için, türlerin kendi <xref:System.Object.Finalize%2A> <xref:System.Object.Finalize%2A> metodu içinden temel sınıf yöntemini çağırması gerekir. C# Derleyici, çağrıyı temel sınıf sonlandırıcısını otomatik olarak ekler.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, <xref:System.Object.Finalize%2A> <xref:System.Object.Finalize%2A> yöntemden temel türün yöntemini çağırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Ortak dil çalışma zamanını hedefleyen bazı derleyiciler, temel türün sonlandırıcısını Microsoft ara dili 'ne (MSIL) bir çağrı ekler. Bu kuraldaki bir uyarı bildirilmezse, derleyicisinde çağrı eklemez ve kodunuza eklemeniz gerekir.

## <a name="example"></a>Örnek

Aşağıdaki Visual Basic örnek, temel sınıfında `TypeB` <xref:System.Object.Finalize%2A> yöntemini doğru şekilde çağıran bir türü gösterir.

[!code-vb[FxCop.Usage.IDisposableBaseCalled#1](../code-quality/codesnippet/VisualBasic/ca2220-finalizers-should-call-base-class-finalizer_1.vb)]

## <a name="see-also"></a>Ayrıca bkz.

- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)