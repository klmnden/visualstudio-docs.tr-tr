---
title: 'CA2105: Dizi alanları salt okunur olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2105
- ArrayFieldsShouldNotBeReadOnly
helpviewer_keywords:
- ArrayFieldsShouldNotBeReadOnly
- CA2105
ms.assetid: 0bdc3421-3ceb-4182-b30c-a992fbfcc35d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7407fcbe035d02992f414027114d69c257f5f390
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232918"
---
# <a name="ca2105-array-fields-should-not-be-read-only"></a>CA2105: Dizi alanları salt okunur olmamalıdır

|||
|-|-|
|TypeName|ArrayFieldsShouldNotBeReadOnly|
|CheckId|CA2105|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir diziyi tutan ortak veya korumalı bir alan salt okunurdur.

## <a name="rule-description"></a>Kural açıklaması

Bir dizi içeren bir `readonly` alana`ReadOnly` ( [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)]ın) değiştiricisini uyguladığınızda, alan farklı bir diziye başvuracak şekilde değiştirilemez. Bir dizinin öğeleri salt okunur bir alanda depolanmış olsa bile değiştirilebilir. Herkese açık bir şekilde erişilebilen salt yazılır bir dizinin öğelerine dayalı işlemler yapan veya kararları veren kod, açıktan yararlanılır bir güvenlik açığı içerebilir.

Ortak bir alana sahip olmanın CA1051 tasarım kuralını [da ihlal ettiğini unutmayın: Görünür örnek alanlarını](../code-quality/ca1051-do-not-declare-visible-instance-fields.md)bildirmeyin.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural tarafından tanımlanan güvenlik açığını gidermek için, herkese açık bir şekilde erişilebilen salt okunurdur. Aşağıdaki yordamlardan birini kullanmanız önemle önerilir:

- Diziyi, değiştirilemeyen türü kesin belirlenmiş bir koleksiyonla değiştirin. Daha fazla bilgi için bkz. <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>.

- Ortak alanı, özel dizinin bir kopyasını döndüren bir yöntem ile değiştirin. Kodunuz kopyaya bağlı olmadığından, öğeler değiştirilirse bir tehlike yoktur.

İkinci yaklaşımı seçerseniz, alanı bir özelliği ile değiştirmeyin; dizileri döndüren Özellikler performansı olumsuz etkiler. Daha fazla bilgi için bkz [. CA1819: Özellikler diziler](../code-quality/ca1819-properties-should-not-return-arrays.md)döndürmemelidir.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarının dışlanmasını kesinlikle önerilmez. Neredeyse bir salt okuma alanının içeriğinin önemli olmadığı neredeyse hiçbir senaryo meydana gelir. Bu durumda senaryonuz varsa, iletiyi dışlamak yerine `readonly` değiştiriciyi kaldırın.

## <a name="example-1"></a>Örnek 1

Bu örnek, bu kuralı ihlal eden tehlikeleri gösterir. İlk bölüm, güvenli olmayan iki alan ( `MyClassWithReadOnlyArrayField``grades` ve `privateGrades`) içeren bir türü olan örnek bir kitaplığı gösterir. Alan `grades` geneldir ve bu nedenle herhangi bir çağırana karşı savunmasız olur. Alan `privateGrades` özeldir, ancak `GetPrivateGrades` yöntem tarafından çağıranlara döndürüldüğünden hala güvenlik açığı vardır. Alan, `GetSecurePrivateGrades` yöntemi tarafından güvenli bir şekilde sunulur. `securePrivateGrades` İyi tasarım uygulamalarını izlemek için özel olarak bildirilmiştir. İkinci bölüm, `grades` ve `privateGrades` üyelerinde depolanan değerleri değiştiren kodu gösterir.

Örnek sınıf kitaplığı aşağıdaki örnekte görünür.

[!code-csharp[FxCop.Security.ArrayFieldsNotReadOnly#1](../code-quality/codesnippet/CSharp/ca2105-array-fields-should-not-be-read-only_1.cs)]

## <a name="example-2"></a>Örnek 2

Aşağıdaki kod, salt okuma dizisi güvenlik sorunlarını göstermek için örnek sınıf kitaplığını kullanır.

[!code-csharp[FxCop.Security.TestArrayFieldsRead#1](../code-quality/codesnippet/CSharp/ca2105-array-fields-should-not-be-read-only_2.cs)]

Bu örnekteki çıktı:

```text
Before tampering: Grades: 90, 90, 90 Private Grades: 90, 90, 90  Secure Grades, 90, 90, 90
After tampering: Grades: 90, 555, 90 Private Grades: 90, 555, 90  Secure Grades, 90, 90, 90
```

## <a name="related-rules"></a>İlgili kurallar

- [CA2104 Salt okuma kesilebilir başvuru türlerini bildirme](../code-quality/ca2104-do-not-declare-read-only-mutable-reference-types.md)

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Array?displayProperty=fullName>
- <xref:System.Collections.ReadOnlyCollectionBase?displayProperty=fullName>
