---
title: 'CA1051: Görünür örnek alanlarını bildirmeyin'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- CA1051
- DoNotDeclareVisibleInstanceFields
helpviewer_keywords:
- CA1051
- DoNotDeclareVisibleInstanceFields
ms.assetid: 2805376c-824c-462c-81d1-c51aaf7cabe7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 56e5c8f0a0e703bfa2a2cc2419d1bd3be0b0f23a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54917231"
---
# <a name="ca1051-do-not-declare-visible-instance-fields"></a>CA1051: Görünür örnek alanlarını bildirmeyin

|||
|-|-|
|TypeName|DoNotDeclareVisibleInstanceFields|
|CheckId|CA1051|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Dışarıdan görünen bir tür bir dışarıdan görünür örnek alanı vardır.

## <a name="rule-description"></a>Kural açıklaması
 Bir alanın birincil kullanım alanının uygulama ayrıntısı olması gerekir. Alanlar olmalıdır `private` veya `internal` ve özelliklerini kullanmaya maruz kalması. Bir alana erişmek olduğu ve özellikleri türünde bozucu değişiklikler oluşturmaksızın genişlettikçe özellik erişimcileri kodda değiştirebilirsiniz bir özelliğe erişmek oldukça kolaydır. Yalnızca özel veya iç alan değerini döndüren özellikler, bir alana erişim özellik gerçekleştirmek için optimize edilmiş; çok az performans kazancı özellikler üzerinde dışarıdan görünen alanları kullanımı ile ilişkilidir.

 Dışarıdan görünen başvurduğu `public`, `protected`, ve `protected internal` (`Public`, `Protected`, ve `Protected Friend` Visual Basic'te) erişilebilirlik düzeyleri.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Bu kural ihlalini düzeltmek için alanın olmasını `private` veya `internal` ve dışarıdan görünen bir özelliğini kullanarak üzerinden kullanıma sunacaksınız.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın. Dışarıdan görünen alanlar, özellikler için kullanılabilir olan herhangi bir avantaj sağlamaz. Ayrıca, ortak alanları tarafından korunamaz [bağlantı talepleri](/dotnet/framework/misc/link-demands). Bkz: [CA2112: Güvenli türler alanları kullanıma](../code-quality/ca2112-secured-types-should-not-expose-fields.md).

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir tür gösterir (`BadPublicInstanceFields`), bu kuralı ihlal ediyor. `GoodPublicInstanceFields` Düzeltilen kod gösterilmektedir.

 [!code-csharp[FxCop.Design.TypesPublicInstanceFields#1](../code-quality/codesnippet/CSharp/ca1051-do-not-declare-visible-instance-fields_1.cs)]

## <a name="related-rules"></a>İlgili kuralları
 [CA2112: Güvenli türler alanları açığa çıkarmamalıdır](../code-quality/ca2112-secured-types-should-not-expose-fields.md)

## <a name="see-also"></a>Ayrıca bkz.
 [Bağlantı talepleri](/dotnet/framework/misc/link-demands)