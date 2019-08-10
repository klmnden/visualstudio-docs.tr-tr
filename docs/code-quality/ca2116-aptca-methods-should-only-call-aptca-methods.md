---
title: 'CA2116: APTCA metotları yalnızca APTCA metotlarını çağırmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AptcaMethodsShouldOnlyCallAptcaMethods
- CA2116
helpviewer_keywords:
- AptcaMethodsShouldOnlyCallAptcaMethods
- CA2116
ms.assetid: 8b91637e-891f-4dde-857b-bf8012270ec4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f55c48583e47a4602f33d69799d1d86a6c9c3e56
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921153"
---
# <a name="ca2116-aptca-methods-should-only-call-aptca-methods"></a>CA2116: APTCA metotları yalnızca APTCA metotlarını çağırmalıdır

|||
|-|-|
|TypeName|AptcaMethodsShouldOnlyCallAptcaMethods|
|CheckId|CA2116|
|Kategori|Microsoft.Security|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

<xref:System.Security.AllowPartiallyTrustedCallersAttribute?displayProperty=fullName> Özniteliği olan derlemedeki bir yöntem özniteliği olmayan bir derlemede bir yöntemi çağırır.

## <a name="rule-description"></a>Kural açıklaması

Varsayılan olarak, tanımlayıcı adlara sahip derlemelerde ortak veya korumalı Yöntemler, tam güven için [bağlantı taleplerine](/dotnet/framework/misc/link-demands) dolaylı olarak korunur; yalnızca tam güvenilir çağıranlar, tanımlayıcı adlı bir derlemeye erişebilir. <xref:System.Security.AllowPartiallyTrustedCallersAttribute> (Aptca) özniteliğiyle işaretlenen tanımlayıcı adlı derlemelerin bu koruması yoktur. Öznitelik, bir intranet veya Internet 'ten çalıştırılan kod gibi, derlemeyi tam güvene sahip olmayan çağıranlar için erişilebilir hale getirerek bağlantı talebini devre dışı bırakır.

APTCA özniteliği tam olarak güvenilen bir derlemede olduğunda ve derleme kodu, kısmen güvenilen çağıranlara izin verilmeyen başka bir derlemede yürüttüğünde, bir güvenlik açığından yararlanma olasılığı vardır. İki yöntem `M1` ve `M2` aşağıdaki koşulları karşılıyorsa, kötü amaçlı arayanlar, koruduğu `M2`örtük tam `M1` güven bağlantısı talebini atlamak için yöntemini kullanabilir:

- `M1`, APTCA özniteliğine sahip tam güvenilir bir derlemede bildirildiği ortak bir yöntemdir.

- `M1`derleme dışında `M2` `M1`bir yöntemi çağırır.

- `M2`derlemesinin APTCA özniteliği yok ve bu nedenle, kısmen güvenilen çağıranlar adına veya tarafından yürütülmemelidir.

Kısmen güvenilen bir çağıran `X` yöntemi `M1`çağırabilir ve çağrıya `M2`neden `M1` olur. Aptca özniteliğine sahip olmadığı için, hemen çağıranın (`M1`) tam güven için bir bağlantı talebini karşılaması gerekir; `M2` `M1` tam güvene sahiptir ve bu nedenle bu denetimi karşılar. Güvenlik riski `X` , güvenilmeyen çağıranların koruduğu `M2` bağlantı talebini karşılamadığına katılmaz. Bu nedenle, APTCA özniteliğine sahip Yöntemler özniteliği olmayan yöntemleri çağırmamalıdır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
APCTA özniteliği gerekliyse, tam güven derlemesine çağıran yöntemi korumak için bir talep kullanın. Talep ettiğiniz tam izinler, yönteminiz tarafından sunulan işlevlere bağlıdır. Mümkünse, temel işlevselliğin kısmen güvenilen çağıranlara açık olmamasını sağlamak için yöntemi tam güven için bir talep ile koruyun. Bu mümkün değilse, sunulan işlevleri etkin bir şekilde koruyan bir izin kümesi seçin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan bir uyarıyı güvenle bastırmak için, yönteminiz tarafından sunulan işlevselliğin doğrudan veya dolaylı olarak, çağıranların bozucu bir şekilde kullanılabilecek gizli bilgilere, işlemlere veya kaynaklara erişmesine izin vermez.

## <a name="example-1"></a>Örnek 1
Aşağıdaki örnek, bu kural tarafından algılanan güvenlik açıklarını göstermek için iki derleme ve bir test uygulaması kullanır. İlk derleme aptca özniteliğine sahip değil ve kısmen güvenilen çağıranlar tarafından erişilememelidir (önceki tartışmada tarafından `M2` temsil edilir).

[!code-csharp[FxCop.Security.NoAptca#1](../code-quality/codesnippet/CSharp/ca2116-aptca-methods-should-only-call-aptca-methods_1.cs)]

## <a name="example-2"></a>Örnek 2
İkinci derleme tamamen güvenilirdir ve kısmen güvenilen çağıranlar (önceki tartışmada tarafından `M1` temsil edilir) sağlar.

[!code-csharp[FxCop.Security.YesAptca#1](../code-quality/codesnippet/CSharp/ca2116-aptca-methods-should-only-call-aptca-methods_2.cs)]

## <a name="example-3"></a>Örnek 3
Test uygulaması (önceki tartışmada `X` tarafından temsil edilir) kısmen güvenilirdir.

[!code-csharp[FxCop.Security.TestAptcaMethods#1](../code-quality/codesnippet/CSharp/ca2116-aptca-methods-should-only-call-aptca-methods_3.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
Demand for full trust:Request failed.
ClassRequiringFullTrust.DoWork was called.
```

## <a name="related-rules"></a>İlgili kurallar

- [CA2117 APTCA türleri yalnızca APTCA taban türlerini genişletmelidir](../code-quality/ca2117-aptca-types-should-only-extend-aptca-base-types.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
- [Kısmen güvenilen koddan kitaplıkları kullanma](/dotnet/framework/misc/using-libraries-from-partially-trusted-code)
- [Bağlantı talepleri](/dotnet/framework/misc/link-demands)
- [Veri ve Modelleme](/dotnet/framework/data/index)