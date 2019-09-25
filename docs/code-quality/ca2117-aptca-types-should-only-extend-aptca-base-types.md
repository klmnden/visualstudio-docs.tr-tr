---
title: 'CA2117: APTCA türleri yalnızca APTCA taban türlerini genişletmelidir'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA2117
- AptcaTypesShouldOnlyExtendAptcaBaseTypes
helpviewer_keywords:
- AptcaTypesShouldOnlyExtendAptcaBaseTypes
- CA2117
ms.assetid: c505b586-2f1e-47cb-98ee-a5afcbeda70f
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 832d2c9fc1d4b9138a7cd1bc39868b3c4bf1b814
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232648"
---
# <a name="ca2117-aptca-types-should-only-extend-aptca-base-types"></a>CA2117: APTCA türleri yalnızca APTCA taban türlerini genişletmelidir

|||
|-|-|
|TypeName|AptcaTypesShouldOnlyExtendAptcaBaseTypes|
|CheckId|CA2117|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

<xref:System.Security.AllowPartiallyTrustedCallersAttribute?displayProperty=fullName> Özniteliği içeren bir derlemede ortak veya korumalı tür özniteliği olmayan bir derlemede belirtilen türden devralır.

## <a name="rule-description"></a>Kural açıklaması

Varsayılan olarak, tanımlayıcı adlara sahip derlemelerde ortak veya korumalı türler tam güven için bir [InheritanceDemand](xref:System.Security.Permissions.SecurityAction#System_Security_Permissions_SecurityAction_InheritanceDemand) tarafından örtük olarak korunur. <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (Aptca) özniteliğiyle işaretlenen tanımlayıcı adlı derlemelerin bu koruması yoktur. Öznitelik, devralma talebini devre dışı bırakır. Devralma talebi olmadan bir derlemede belirtilen açığa çıkarılan türler, tam güvene sahip olmayan türler tarafından devralınabilir.

APTCA özniteliği tam olarak güvenilen bir derlemede olduğunda ve derlemedeki bir tür, kısmen güvenilen çağıranlara izin verilmeyen bir türden devralırsa, bir güvenlik açığından yararlanma olasılığı vardır. İki tür `T1` varsa ve `T2` aşağıdaki koşullara uyuyorsa, kötü amaçlı çağıranlar, koruduğu `T1` `T2`örtük tam güven devralma talebini atlamak için türünü kullanabilir:

- `T1`, APTCA özniteliğine sahip tam güvenilir bir derlemede tanımlanmış ortak bir tür.

- `T1`kendi derlemesi dışındaki bir `T2` türden devralır.

- `T2`derlemesi APTCA özniteliğine sahip değil ve bu nedenle kısmen güvenilen derlemelerdeki türlere devredilemez.

Kısmen güvenilen bir tür `X` öğesinden `T1`devralınabilir ve bu, içinde `T2`belirtilen devralınan üyelere erişim sağlar. Aptca özniteliğine sahip olmadığından, hemen türetilmiş türü (`T1`) tam güven için bir devralma talebini karşılamalıdır; `T2` `T1` tam güvene sahiptir ve bu nedenle bu denetimi karşılar. Güvenlik riski `X` , güvenilir olmayan altsınıflama karşı koruyan `T2` devralma talebini karşılamadığına katılmaz. Bu nedenle, APTCA özniteliğine sahip türler özniteliği olmayan türleri genişletmemelidir.

Diğer bir güvenlik sorunu ve belki de daha yaygın bir şekilde, türetilmiş türün (`T1`), programcı hatası aracılığıyla, tam güven gerektiren türden korumalı üyeleri kullanıma sunmasıdır (`T2`). Bu pozlama gerçekleştiğinde, güvenilmeyen çağıranlar yalnızca tam güvenilir türler için kullanılabilir olması gereken bilgilere erişim elde edebilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

İhlalin tarafından bildirilen tür APTCA özniteliğini gerektirmeyen bir derlemede ise, kaldırın.

APTCA özniteliği gerekliyse, türe tam güven için bir devralma talebi ekleyin. Devralma talebi güvenilmeyen türlerin devralınmasını önler.

İhlalin tarafından bildirilen temel türlerin Derlemeleriyle APTCA özniteliğini ekleyerek ihlalin düzeltilmesi mümkündür. Bu, öncelikle derlemelerdeki tüm kodun ve derlemelere bağlı olan tüm kodun yoğun bir güvenlik incelemesi yapmadan bunu kullanmayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı güvenle bastırmak için, sizin oluşturduğunuz korumalı üyelerin, güvenilmeyen çağıranların, zararlı bir şekilde kullanılabilecek gizli bilgilere, işlemlere veya kaynaklara erişmesine doğrudan veya dolaylı olarak izin vermediğinden emin olmanız gerekir.

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kural tarafından algılanan güvenlik açıklarını göstermek için iki derleme ve bir test uygulaması kullanır. İlk derleme aptca özniteliğine sahip değil ve kısmen güvenilen türler (önceki tartışmada temsil edilen `T2` ) tarafından devredilemez olmalıdır.

[!code-csharp[FxCop.Security.NoAptcaInherit#1](../code-quality/codesnippet/CSharp/ca2117-aptca-types-should-only-extend-aptca-base-types_1.cs)]

Önceki tartışmaya göre `T1` temsil edilen ikinci derleme, tamamen güvenilirdir ve kısmen güvenilen çağıranlara izin verir.

[!code-csharp[FxCop.Security.YesAptcaInherit#1](../code-quality/codesnippet/CSharp/ca2117-aptca-types-should-only-extend-aptca-base-types_2.cs)]

Önceki tartışmaya göre `X` temsil edilen test türü kısmen güvenilen bir derlemede bulunur.

[!code-csharp[FxCop.Security.TestAptcaInherit#1](../code-quality/codesnippet/CSharp/ca2117-aptca-types-should-only-extend-aptca-base-types_3.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
Meet at the shady glen 2/22/2003 12:00:00 AM!
From Test: sunny meadow
Meet at the sunny meadow 2/22/2003 12:00:00 AM!
```

## <a name="related-rules"></a>İlgili kurallar

[CA2116Ç APTCA yöntemleri yalnızca APTCA yöntemlerini çağırmalıdır](../code-quality/ca2116-aptca-methods-should-only-call-aptca-methods.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
- [Kısmen güvenilen koddan kitaplıkları kullanma](/dotnet/framework/misc/using-libraries-from-partially-trusted-code)
