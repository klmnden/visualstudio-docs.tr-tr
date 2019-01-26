---
title: 'CA1065: Beklenmeyen konumlarda özel durum harekete geçirmeyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: bfdb12dfbe5bf0f0bee035e79f1b8442db0bbf71
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55031532"
---
# <a name="ca1065-do-not-raise-exceptions-in-unexpected-locations"></a>CA1065: Beklenmeyen konumlarda özel durum harekete geçirmeyin

|||
|-|-|
|TypeName|DoNotRaiseExceptionsInUnexpectedLocations|
|CheckId|CA1065|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Bozucu olmayan|

## <a name="cause"></a>Sebep

İstisna atılmasını beklemeyen yöntem bir istisna atar.

## <a name="rule-description"></a>Kural açıklaması

Özel durum oluşturması beklenmiyor yöntemleri gibi kategorilere ayrılabilir:

- Özellik Get yöntemleri

- Olay erişimci metotları

- Equals yöntemi

- GetHashCode Methods

- ToString yöntemi

- Statik Oluşturucular

- Sonlandırıcılar

- Dispose yöntemi

- Eşitlik İşleçleri

- Örtük dönüştürme işleçleri

Aşağıdaki bölümlerde, bu yöntem türleri açıklanmaktadır.

### <a name="property-get-methods"></a>Özellik Get yöntemleri

Özellikler, temelde akıllı alanlardır. Bu nedenle, bir alan mümkün olduğunca gibi davranırlar. Alanlar, özel durumlar yok ve birinin diğerinden özellikleri gerekir. Özel durum oluşturan bir özellik varsa, bu bir yöntem yapmayı göz önüne alın.

Bir özellik get yöntemi aşağıdaki özel durumlar atılabilir:

- <xref:System.InvalidOperationException?displayProperty=fullName> ve tüm türevleri (dahil olmak üzere <xref:System.ObjectDisposedException?displayProperty=fullName>)

- <xref:System.NotSupportedException?displayProperty=fullName> ve tüm türevleri

- <xref:System.ArgumentException?displayProperty=fullName> (yalnızca get dizinlenmiş)

- <xref:System.Collections.Generic.KeyNotFoundException> (yalnızca get dizinlenmiş)

### <a name="event-accessor-methods"></a>Olay erişimci metotları

Olay erişimcileri, özel durumlar yok basit işlemler olmalıdır. Bir olay, bir olay işleyicisi ekleyip çalıştığınızda bir özel durum oluşturmamalıdır.

Olay erişimci aşağıdaki özel durumlar atılabilir:

- <xref:System.InvalidOperationException?displayProperty=fullName> ve tüm türevleri (dahil olmak üzere <xref:System.ObjectDisposedException?displayProperty=fullName>)

- <xref:System.NotSupportedException?displayProperty=fullName> ve tüm türevleri

- <xref:System.ArgumentException> ve türevleri

### <a name="equals-methods"></a>Equals yöntemi

Aşağıdaki **eşittir** yöntemleri, özel durum oluşturmamalıdır:

- <xref:System.Object.Equals%2A?displayProperty=fullName>

- <xref:System.IEquatable%601.Equals%2A>

Bir **eşittir** yöntemi döndürmelidir `true` veya `false` yerine bir özel durum. Örneğin, eşittir geçirilir, eşleşmeyen iki tür yalnızca döndürmelidir `false` oluşturmak yerine bir <xref:System.ArgumentException>.

### <a name="gethashcode-methods"></a>GetHashCode Methods

Aşağıdaki **GetHashCode** yöntemleri genellikle özel durum oluşturmamalıdır:

- <xref:System.Object.GetHashCode%2A>

- <xref:System.Collections.IEqualityComparer.GetHashCode%2A>

**GetHashCode** her zaman bir değer döndürmesi gerekir. Aksi takdirde karma tablosundaki öğeleri kaybedebilir.

Sürümleri **GetHashCode** bağımsız değişken throw süren bir <xref:System.ArgumentException>. Ancak, **Object.GetHashCode** hiçbir zaman özel bir durum oluşturmamalıdır.

### <a name="tostring-methods"></a>ToString yöntemi

Hata ayıklayıcı kullanan <xref:System.Object.ToString%2A?displayProperty=fullName> dize biçiminde nesneleri hakkındaki bilgileri görüntülemek amacıyla. Bu nedenle, **ToString** bir nesne durumunu değiştirmemesi gerekir ve özel durumlar olmamalıdır.

### <a name="static-constructors"></a>Statik Oluşturucular

Statik oluşturucu özel durumları atma türü geçerli uygulama etki alanında kullanılamaz hale gelmesine neden olur. Statik Oluşturucu bir özel durum için geçerli bir nedeniniz (örneğin, bir güvenlik sorunu) olmalıdır.

### <a name="finalizers"></a>Sonlandırıcılar

Bir sonlandırıcı bir özel durum, işlemi çıkarmadan CLR hızlı başarısız olmasına neden olur. Bu nedenle, özel durumları atma içindeki bir sonlandırıcı her zaman kaçınılmalıdır.

### <a name="dispose-methods"></a>Dispose yöntemi

A <xref:System.IDisposable.Dispose%2A?displayProperty=fullName> yöntemi bir özel durum oluşturmamalıdır. Dispose temizleme mantık parçası olarak çağırılır genellikle bir `finally` yan tümcesi. Bu nedenle, özel durum işleme içine eklenecek kullanıcıyı açıkça Dispose ' bir özel durum zorlar `finally` yan tümcesi.

**Dispose(false)** kod yolu hiçbir zaman throw özel durumlar, Dispose neredeyse her zaman bir sonlandırıcı çağrıldığı için.

### <a name="equality-operators--"></a>Eşitlik işleçleri (==,! =)

Equals yöntemler gibi eşitlik işleçleri ya da döndürmelidir `true` veya `false`ve özel durum oluşturmamalıdır.

### <a name="implicit-cast-operators"></a>Örtük dönüştürme işleçleri

Örtük dönüştürme işleci tarafından oluşturulan bir özel durum, kullanıcı genellikle bir örtük dönüştürme işleci çağrıldıktan farkında olduğundan beklenmiyor. Bu nedenle, hiçbir özel durum örtük dönüştürme işleçleri durumun oluşturulması gerekir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Özellik alıcılar için ya da mantığını artık özel durum veya özelliği bir yönteme sahip olacak şekilde değiştirin.

Daha önce listelenen tüm diğer yöntemi türleri için mantığını artık özel durum oluşturması gerekir geçirmeyecek şekilde değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

İhlali tarafından oluşturulan bir özel durum yerine bir özel durum bildirimi nedeniyle oluştu, bu kuraldan bir uyarıyı bastırmak güvenlidir.

## <a name="related-rules"></a>İlgili kuralları

- [CA2219: Özel durum yan tümceleri içinde özel durum harekete geçirmeyin](../code-quality/ca2219-do-not-raise-exceptions-in-exception-clauses.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Tasarım Uyarıları](../code-quality/design-warnings.md)