---
title: 'CA1065: Beklenmeyen konumlarda özel durum harekete geçirmeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1065
- DoNotRaiseExceptionsInUnexpectedLocations
helpviewer_keywords:
- DoNotRaiseExceptionsInUnexpectedLocations
- CA1065
ms.assetid: 4e1bade4-4ca2-4219-abc3-c7b2d741e157
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 257100be0eb2766ef413854795c934b230e29370
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235239"
---
# <a name="ca1065-do-not-raise-exceptions-in-unexpected-locations"></a>CA1065: Beklenmeyen konumlarda özel durum harekete geçirmeyin

|||
|-|-|
|TypeName|DoNotRaiseExceptionsInUnexpectedLocations|
|CheckId|CA1065|
|Kategori|Microsoft.Design|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

İstisna atılmasını beklemeyen yöntem bir istisna atar.

## <a name="rule-description"></a>Kural açıklaması

Özel durum oluşturması beklenmeyen yöntemler aşağıdaki şekilde kategorize edilebilir:

- Özellik get yöntemleri

- Olay erişimci yöntemleri

- Eşittir yöntemleri

- GetHashCode yöntemleri

- ToString yöntemleri

- Statik Oluşturucular

- Sonlandırıcılar

- Dispose yöntemleri

- Eşitlik İşleçleri

- Örtük atama Işleçleri

Aşağıdaki bölümler bu yöntem türlerini tartışır.

### <a name="property-get-methods"></a>Özellik get yöntemleri

Özellikler temel olarak akıllı alanlardır. Bu nedenle, mümkün olduğunca bir alan gibi davranmalıdır. Alanlar özel durum oluşturmaz ve özelliklerden hiçbirine gerek kalmaz. Özel durum oluşturan bir özelliğe sahipseniz, bunu bir yöntemi yapmayı düşünün.

Bir özellik Get yönteminden aşağıdaki özel durumlar oluşturulabilir:

- <xref:System.InvalidOperationException?displayProperty=fullName>ve tüm türetme (dahil <xref:System.ObjectDisposedException?displayProperty=fullName>)

- <xref:System.NotSupportedException?displayProperty=fullName>ve tüm türetme

- <xref:System.ArgumentException?displayProperty=fullName>(yalnızca dizinli Get 'ten)

- <xref:System.Collections.Generic.KeyNotFoundException>(yalnızca dizinli Get 'ten)

### <a name="event-accessor-methods"></a>Olay erişimci yöntemleri

Olay erişimcileri özel durum oluşturmayan basit işlemler olmalıdır. Olay işleyicisi eklemeyi veya kaldırmayı denediğinizde bir olay özel durum oluşturmaz.

Aşağıdaki özel durumlar bir olay erişimcisinde oluşturulabilir:

- <xref:System.InvalidOperationException?displayProperty=fullName>ve tüm türetme (dahil <xref:System.ObjectDisposedException?displayProperty=fullName>)

- <xref:System.NotSupportedException?displayProperty=fullName>ve tüm türetme

- <xref:System.ArgumentException>ve türetme

### <a name="equals-methods"></a>Eşittir yöntemleri

Aşağıdaki **eşittir** yöntemleri özel durum oluşturmaz:

- <xref:System.Object.Equals%2A?displayProperty=fullName>

- <xref:System.IEquatable%601.Equals%2A>

Bir **Equals** yöntemi, özel `true` durum `false` oluşturmak yerine veya döndürmelidir. Örneğin, eşittir iki eşleşmeyen tür geçirtiyse, oluşturmak yerine `false` <xref:System.ArgumentException>yalnızca döndürmelidir.

### <a name="gethashcode-methods"></a>GetHashCode yöntemleri

Aşağıdaki **GetHashCode** yöntemleri genellikle özel durum oluşturmaz:

- <xref:System.Object.GetHashCode%2A>

- <xref:System.Collections.IEqualityComparer.GetHashCode%2A>

**GetHashCode** her zaman bir değer döndürmelidir. Aksi takdirde, karma tablodaki öğeleri kaybedebilirsiniz.

Bağımsız değişken alan **GetHashCode** sürümleri bir <xref:System.ArgumentException>oluşturabilir. Ancak **Object. GetHashCode** asla bir özel durum oluşturmaz.

### <a name="tostring-methods"></a>ToString yöntemleri

Hata ayıklayıcı, <xref:System.Object.ToString%2A?displayProperty=fullName> dize biçimindeki nesneler hakkında bilgi görüntülemeye yardımcı olmak için kullanır. Bu nedenle, **ToString** bir nesnenin durumunu değiştirmemelidir ve özel durum oluşturmaz.

### <a name="static-constructors"></a>Statik Oluşturucular

Statik bir oluşturucudan özel durumlar oluşturmak, türün geçerli uygulama etki alanında kullanılamaz hale gelmesine neden olur. Statik bir oluşturucudan özel durum oluşturmak için iyi bir nedeniniz (güvenlik sorunu gibi) olmalıdır.

### <a name="finalizers"></a>Sonlandırıcılar

Sonlandırıcının bir özel durum oluşturmak, CLR 'nin hızlı bir şekilde başarısız olmasına neden olur ve bu da işlemi kapatır. Bu nedenle, bir sonlandırıcının özel durumların oluşturulması her zaman kaçınılmalıdır.

### <a name="dispose-methods"></a>Dispose yöntemleri

Bir <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> Yöntem özel durum oluşturmaz. Dispose, genellikle bir yan tümcedeki Temizleme mantığının bir `finally` parçası olarak çağırılır. Bu nedenle, Dispose 'ten özel bir durum açıkça oluşturmak, kullanıcının `finally` yan tümce içinde özel durum işleme eklemesini zorlar.

Dispose **(false)** kod yolu hiçbir zaman özel durum oluşturmaz, çünkü Dispose bir sonlandırıcının neredeyse her zaman çağrılır.

### <a name="equality-operators--"></a>Eşitlik Işleçleri (= =,! =)

Eşittir yöntemlerine benzer şekilde, eşitlik işleçleri `true` veya `false`döndürmelidir ve özel durumlar oluşturmamalıdır.

### <a name="implicit-cast-operators"></a>Örtük atama Işleçleri

Kullanıcı genellikle örtük bir atama işlecinin çağrıldığı farkında olduğundan, örtük atama işleci tarafından oluşturulan özel durum beklenmiyor. Bu nedenle, örtük atama işleçlerinden hiçbir özel durum atılmamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Özellik kodlayıcıları için, mantığı, artık özel durum oluşturmak zorunda olmayacak şekilde değiştirin ya da özelliği bir yönteme değiştirin.

Daha önce listelenen diğer tüm yöntem türleri için mantığı, artık özel durum oluşturması için değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

İhlalin oluşan özel durum yerine bir özel durum bildirimi neden olduysa, bu kuraldan bir uyarının görüntülenmesini güvenli hale gelir.

## <a name="related-rules"></a>İlgili kurallar

- [CA2219 Özel durum yan tümcelerinde özel durum yükseltmeyin](../code-quality/ca2219-do-not-raise-exceptions-in-exception-clauses.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Tasarım Uyarıları](../code-quality/design-warnings.md)