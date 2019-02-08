---
title: 'CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DisposableTypesShouldDeclareFinalizer
- CA2216
helpviewer_keywords:
- CA2216
- DisposableTypesShouldDeclareFinalizer
ms.assetid: 0cabcc5e-b526-452b-8c2a-0cbe3b93c0ef
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e4baee9f532c0351feeced07ce9403245ccee14a
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55927704"
---
# <a name="ca2216-disposable-types-should-declare-finalizer"></a>CA2216: Atılabilir türler sonlandırıcıyı bildirmelidir

|||
|-|-|
|TypeName|DisposableTypesShouldDeclareFinalizer|
|CheckId|CA2216|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Uygulayan bir tür <xref:System.IDisposable?displayProperty=fullName>ve yönetilmeyen kaynakların kullanımını öneren alanlar, bir sonlandırıcı açıklandığı uygulamıyor <xref:System.Object.Finalize%2A?displayProperty=fullName>.

## <a name="rule-description"></a>Kural açıklaması

Atılabilir türü aşağıdaki türlerde alanlar içeriyorsa bu kural ihlalini bildirilir:

- <xref:System.IntPtr?displayProperty=fullName>

- <xref:System.UIntPtr?displayProperty=fullName>

- <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName>

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için çağıran bir sonlandırıcı uygulamak, <xref:System.IDisposable.Dispose%2A> yöntemi.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Türü uygulamazsa bu kuraldan bir uyarıyı bastırmak güvenlidir <xref:System.IDisposable> yönetilmeyen kaynakları serbest bırakmak amacıyla.

## <a name="example"></a>Örnek

Aşağıdaki örnek bu kuralı ihlal eden bir tür gösterir.

[!code-csharp[FxCop.Usage.DisposeNoFinalize#1](../code-quality/codesnippet/CSharp/ca2216-disposable-types-should-declare-finalizer_1.cs)]

## <a name="related-rules"></a>İlgili kuralları

[CA2115: GC çağırın. Yerel kaynaklar kullanırken KeepAlive](../code-quality/ca2115-call-gc-keepalive-when-using-native-resources.md)

[CA1816: GC çağırın. IDisposable.Dispose doğru](../code-quality/ca1816-call-gc-suppressfinalize-correctly.md)

[CA1049: Yerel kaynaklara sahip türler atılabilir olmalıdır](../code-quality/ca1049-types-that-own-native-resources-should-be-disposable.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable?displayProperty=fullName>
- <xref:System.IntPtr?displayProperty=fullName>
- <xref:System.Runtime.InteropServices.HandleRef?displayProperty=fullName>
- <xref:System.UIntPtr?displayProperty=fullName>
- <xref:System.Object.Finalize%2A?displayProperty=fullName>
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)