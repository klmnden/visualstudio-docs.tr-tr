---
title: 'CA2213: Atılabilen alanlar atılmalıdır'
ms.date: 05/14/2019
ms.topic: reference
f1_keywords:
- DisposableFieldsShouldBeDisposed
- CA2213
helpviewer_keywords:
- CA2213
- DisposableFieldsShouldBeDisposed
ms.assetid: e99442c9-70e2-47f3-b61a-d8ac003bc6e5
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 675206bb58e27110af79c46b1d61e9489f7661f2
ms.sourcegitcommit: 0f44ec8ba0263056ad04d2d0dc904ad4206ce8fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/06/2019
ms.locfileid: "70766090"
---
# <a name="ca2213-disposable-fields-should-be-disposed"></a>CA2213: Atılabilen alanlar atılmalıdır

|||
|-|-|
|TypeName|DisposableFieldsShouldBeDisposed|
|CheckId|CA2213|
|Kategori|Microsoft. Usage|
|Yeni Değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Uygulayan <xref:System.IDisposable?displayProperty=fullName> bir tür, de uygulayan <xref:System.IDisposable>türler olan alanları bildirir. Alan yöntemi, bildirim türünün <xref:System.IDisposable.Dispose%2A> yöntemi tarafından çağrılmaz. <xref:System.IDisposable.Dispose%2A>

## <a name="rule-description"></a>Kural açıklaması

Bir tür, yönetilmeyen tüm kaynakların elden atılırken sorumludur. Rule CA2213, bir atılabilir türünün (yani, <xref:System.IDisposable>uygulayan) `T` bir atılabilir türünün `FT`örneği olan bir alan `F` bildirip bildirilmediğini denetler. Yöntem veya kapsayan `F` türün `T`başlatıcıları içinde yerel olarak oluşturulmuş bir nesne atanan her alan için, kural, öğesine `FT.Dispose`bir çağrı bulmaya çalışır. Kural, tarafından `T.Dispose` çağrılan yöntemleri ve bir düzey daha düşük (diğer bir deyişle, tarafından `T.Dispose`çağrılan yöntemler tarafından çağrılan yöntemleri) arar.

> [!NOTE]
> [Özel durumlar](#special-cases)dışında, Rule CA2213 yalnızca, kapsayan türün yöntemleri ve başlatıcıları içinde yerel olarak oluşturulmuş bir atılabilir nesnesi atanmış alanlar için ateşlenir. Nesne oluşturulmuş veya türü `T`dışında atanırsa, kural başlatılmıyor. Bu, kapsayan türün nesneyi elden atma sorumluluğunu karşılamabileceği durumlarda paraziti azaltır.

### <a name="special-cases"></a>Özel durumlar

Atandıkları nesne yerel olarak oluşturulsa da Rule CA2213 aşağıdaki türlerin alanları için de tetikde olabilir:

- <xref:System.IO.Stream?displayProperty=nameWithType>
- <xref:System.IO.TextReader?displayProperty=nameWithType>
- <xref:System.IO.TextWriter?displayProperty=nameWithType>
- <xref:System.Resources.IResourceReader?displayProperty=nameWithType>

Bu türlerden birine ait bir nesnenin bir oluşturucuya geçirilmesi ve sonra bir alana atanması, yeni oluşturulan türe bir *atma sahipliğinin aktarılmasını* gösterir. Diğer bir deyişle, yeni oluşturulan tür artık nesnenin elden atılırken sorumludur. Nesne atılmaz, CA2213 ihlali oluşur.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için, uygulayan <xref:System.IDisposable.Dispose%2A> <xref:System.IDisposable>türler olan alanlarda çağırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Şu durumlarda bu kuraldan bir uyarı bastırmak güvenlidir:

- Bayraklı tür, alan tarafından tutulan kaynağı serbest bırakmaktan sorumlu değildir (yani, tür, *atma sahipliğini*içermez)
- Çağrısı, kural <xref:System.IDisposable.Dispose%2A> denetimlerinden daha derin bir çağrı düzeyinde gerçekleşir

## <a name="example"></a>Örnek

Aşağıdaki kod parçacığı, uygulayan `TypeA` <xref:System.IDisposable>bir türü gösterir.

[!code-csharp[FxCop.Usage.IDisposablePattern#1](../code-quality/codesnippet/CSharp/ca2213-disposable-fields-should-be-disposed_1.cs)]

Aşağıdaki kod parçacığında, alanı bir `TypeB` atılabilir Type (`TypeA`) `aFieldOfADisposableType` olarak bildirerek ve alan üzerinde çağrılmadan <xref:System.IDisposable.Dispose%2A> kural CA2213 ihlal eden bir tür gösterilmektedir.

[!code-csharp[FxCop.Usage.IDisposableFields#1](../code-quality/codesnippet/CSharp/ca2213-disposable-fields-should-be-disposed_2.cs)]

İhlalin giderilmesi için atılabilir alanını `Dispose()` çağırın:

```csharp
protected virtual void Dispose(bool disposing)
{
   if (!disposed)
   {
      // Dispose of resources held by this instance.
      aFieldOfADisposableType.Dispose();

      disposed = true;

      // Suppress finalization of this disposed instance.
      if (disposing)
      {
          GC.SuppressFinalize(this);
      }
   }
}
```

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable?displayProperty=fullName>
- [Dispose kriteri](/dotnet/standard/design-guidelines/dispose-pattern)