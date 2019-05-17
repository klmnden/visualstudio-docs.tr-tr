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
ms.openlocfilehash: b38157fcc23561b47a919151aa78a71f98b3909b
ms.sourcegitcommit: 283f2dbce044a18e9f6ac6398f6fc78e074ec1ed
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "65805005"
---
# <a name="ca2213-disposable-fields-should-be-disposed"></a>CA2213: Atılabilen alanlar atılmalıdır

|||
|-|-|
|TypeName|DisposableFieldsShouldBeDisposed|
|CheckId|CA2213|
|Kategori|Microsoft.Usage|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

Uygulayan bir tür <xref:System.IDisposable?displayProperty=fullName> ayrıca uygulayan türler alanlar bildirir <xref:System.IDisposable>. <xref:System.IDisposable.Dispose%2A> Alanının yöntemi çağrılmaz <xref:System.IDisposable.Dispose%2A> bildirim türü yöntemi.

## <a name="rule-description"></a>Kural açıklaması

Bir tür için kendi yönetilmeyen tüm kaynaklarını atma sorumludur. CA2213 çekleri atılabilen bir tür olup olmadığını görmek için rule (uygulayan bir diğer bir deyişle, <xref:System.IDisposable>) `T` bir alan bildirir `F` atılabilir bir türün diğer bir deyişle bir örneğini `FT`. Her bir alan için `F` başlatıcıları, kapsayan tür veya yöntemler içinde yerel olarak oluşturulan bir nesneye atanmış `T`, kural için bir çağrı bulmaya çalışır `FT.Dispose`. Kural çağrılan yöntemler arar `T.Dispose` ve daha düşük bir düzey (diğer bir deyişle, çağrılan yöntemler tarafından çağrılan yöntemler `T.Dispose`).

> [!NOTE]
> Dışındaki [özel durumlar](#special-cases), kuralı içeren türün yöntemlerini ve başlatıcıları içinde yerel olarak oluşturulan bir atılabilir nesneye atanmış olan alanlar için CA2213 ateşlenir. Nesne oluşturulduğunda veya bildirim türünün dışından atanan varsa `T`, kuralı değil başlatılamıyor. Bu, kapsayan tür nesnesinin elden sorumluluğunu sahip olduğu durumlar için gürültü azaltır.

### <a name="special-cases"></a>Özel durumlar

Atanmış oldukları nesnenin yerel olarak oluşturulamayacağını bile kural CA2213 ayrıca aşağıdaki türlerde alanlar için bu özelliği kullanabilirsiniz:

- <xref:System.IO.Stream?displayProperty=nameWithType>
- <xref:System.IO.TextReader?displayProperty=nameWithType>
- <xref:System.IO.TextWriter?displayProperty=nameWithType>
- <xref:System.Resources.IResourceReader?displayProperty=nameWithType>

Şu türlerden birinde bir nesne için bir oluşturucu geçirerek ve bir alan atayarak gösteren bir *sahipliğinin aktarılmasını dispose* yeni oluşturulan tür için. Diğer bir deyişle, yeni oluşturulan tür artık nesnesinin elden için sorumludur. Nesne bırakılmıyor CA2213 ihlalini oluşur.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu kural ihlalini düzeltmek için çağrı <xref:System.IDisposable.Dispose%2A> uygulayan türler alanlar üzerinde <xref:System.IDisposable>.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu, bu kuraldan bir uyarıyı bastırmak güvenli değil:

- Kaynağı serbest bırakarak alanı tarafından tutulan bayraklı türü sorumlu değildir (diğer bir deyişle, tür olmayan *sahipliği dispose*)
- Çağrı <xref:System.IDisposable.Dispose%2A> kural denetimleri daha derin arama düzeyinde gerçekleşir.

## <a name="example"></a>Örnek

Aşağıdaki kod parçacığı bir türü gösterir `TypeA` uygulayan <xref:System.IDisposable>.

[!code-csharp[FxCop.Usage.IDisposablePattern#1](../code-quality/codesnippet/CSharp/ca2213-disposable-fields-should-be-disposed_1.cs)]

Aşağıdaki kod parçacığı bir türü gösterir `TypeB` , ihlal kural CA2213 alan bildirerek `aFieldOfADisposableType` tek kullanımlık bir tür olarak (`TypeA`) ve değil çağırma <xref:System.IDisposable.Dispose%2A> alanı.

[!code-csharp[FxCop.Usage.IDisposableFields#1](../code-quality/codesnippet/CSharp/ca2213-disposable-fields-should-be-disposed_2.cs)]

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.IDisposable?displayProperty=fullName>
- [Dispose Deseni](/dotnet/standard/design-guidelines/dispose-pattern)