---
title: 'CA1001: Atılabilen alanlara sahip türler atılabilir olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1001
- TypesThatOwnDisposableFieldsShouldBeDisposable
helpviewer_keywords:
- CA1001
- TypesThatOwnDisposableFieldsShouldBeDisposable
ms.assetid: c85c126c-2b16-4505-940a-b5ddf873fb22
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 3bda8fc80992a2246c30e28582eb93b4624ab81c
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71236688"
---
# <a name="ca1001-types-that-own-disposable-fields-should-be-disposable"></a>CA1001: Atılabilen alanlara sahip türler atılabilir olmalıdır

|||
|-|-|
|TypeName|TypesThatOwnDisposableFieldsShouldBeDisposable|
|CheckId|CA1001|
|Kategori|Microsoft.Design|
|Son değişiklik|Not-tür, derlemenin dışında görünmüyorsa bölünmez.<br /><br /> Parçalama-tür derleme dışında görünüyorsa.|

## <a name="cause"></a>Sebep
Bir sınıf, <xref:System.IDisposable?displayProperty=fullName> türü olan bir örnek alanı bildirir ve uygular ve sınıfı uygulamaz <xref:System.IDisposable>.

## <a name="rule-description"></a>Kural açıklaması
Bir sınıf, <xref:System.IDisposable> sahip olduğu yönetilmeyen kaynakların atılırken arabirimini uygular. <xref:System.IDisposable> Türü olan bir örnek alan, alanın yönetilmeyen bir kaynağa sahip olduğunu gösterir. Bir <xref:System.IDisposable> alanı, yönetilmeyen bir kaynağa dolaylı olarak bildiren ve <xref:System.IDisposable> arabirimini uygulaması gereken bir sınıf. Sınıf, hiçbir yönetilmeyen kaynağa doğrudan sahip değilse, bir Sonlandırıcı uygulamamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kuralın ihlalini onarmak için, <xref:System.IDisposable> <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> yöntemini uygulayın ve öğesinden, alan <xref:System.IDisposable.Dispose%2A> yöntemini çağırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralını ihlal eden bir sınıfı ve uygulayarak <xref:System.IDisposable>kuralını karşılayan bir sınıfı gösterir. Sınıf, hiçbir yönetilmeyen kaynağa doğrudan sahip olmadığından, sınıf bir Sonlandırıcı uygulamaz.

[!code-vb[FxCop.Design.DisposableFields#1](../code-quality/codesnippet/VisualBasic/ca1001-types-that-own-disposable-fields-should-be-disposable_1.vb)]
[!code-csharp[FxCop.Design.DisposableFields#1](../code-quality/codesnippet/CSharp/ca1001-types-that-own-disposable-fields-should-be-disposable_1.cs)]

## <a name="related-rules"></a>İlgili kurallar
[CA2213 Atılabilir alanlar atılmalıdır](../code-quality/ca2213-disposable-fields-should-be-disposed.md)

[CA2216 Atılabilir türler sonlandırıcıyı bildirmelidir](../code-quality/ca2216-disposable-types-should-declare-finalizer.md)

[CA2215 Dispose yöntemleri taban sınıf atmayı çağırmalıdır](../code-quality/ca2215-dispose-methods-should-call-base-class-dispose.md)

[CA1049 Yerel kaynaklara sahip türler atılabilir olmalıdır](../code-quality/ca1049-types-that-own-native-resources-should-be-disposable.md)