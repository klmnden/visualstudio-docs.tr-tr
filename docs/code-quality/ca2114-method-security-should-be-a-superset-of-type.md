---
title: 'CA2114: Metot güvenliği türün bir üst kümesi olmalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- MethodSecurityShouldBeASupersetOfType
- CA2114
helpviewer_keywords:
- CA2114
- MethodSecurityShouldBeASupersetOfType
ms.assetid: 663f7aa4-8be5-4bd5-be92-4e9444f07077
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 536e676a1b2527c466aae741ca7117be507bfb9a
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71232747"
---
# <a name="ca2114-method-security-should-be-a-superset-of-type"></a>CA2114: Metot güvenliği türün bir üst kümesi olmalıdır

|||
|-|-|
|TypeName|MethodSecurityShouldBeASupersetOfType|
|CheckId|CA2114|
|Kategori|Microsoft.Security|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir tür bildirime dayalı güvenliğe sahiptir ve yöntemlerinden biri aynı güvenlik eylemi için bildirim güvenliğine sahiptir ve güvenlik eylemi [bağlantı taleplerine](/dotnet/framework/misc/link-demands)değildir ve tür tarafından denetlenen izinler, yöntemi tarafından denetlenen izinlerin bir alt kümesi değildir.

## <a name="rule-description"></a>Kural açıklaması
Bir yöntemde aynı eylem için hem Yöntem düzeyinde hem de tür düzeyinde bildirime sahip bir güvenlik bulunmalıdır. İki denetim birleştirilmez; yalnızca Yöntem düzeyi talep uygulanır. Örneğin, bir tür taleplerine izin `X`varsa ve metotlarından biri izin `Y`isterse, kodun yöntemi yürütme izni `X` olması gerekmez.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Her iki eylemin de gerekli olduğundan emin olmak için kodunuzu gözden geçirin. Her iki eylem de gerekliyse, yöntem düzeyi eyleminin tür düzeyinde belirtilen güvenliği içerdiğinden emin olun. Örneğin, `X`türü için izin talebinde bulunursa ve yöntemi de isteğe bağlı izin `Y`içeriyorsa, yöntemi açık bir şekilde talep `X` etmelidir ve `Y`olmalıdır.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Yöntemin tür tarafından belirtilen güvenliği gerektirmiyorsa, bu kuraldan bir uyarıyı gizlemek güvenlidir. Ancak, bu sıradan bir senaryo değildir ve dikkatli bir tasarım incelemesi gereksinimini gösterebilir.

## <a name="example-1"></a>Örnek 1

Aşağıdaki örnek, bu kuralı ihlal eden tehlikeleri göstermek için ortam izinlerini kullanır. Bu örnekte, uygulama kodu tür için gereken izni reddetmeden önce güvenli türde bir örnek oluşturur. Gerçek hayatta bir tehdit senaryosunda, uygulamanın bir nesne örneği elde etmek için başka bir yol gerekir.

Aşağıdaki örnekte, kitaplık bir yöntem için yazma izni talep ediyor ve bir yöntem için okuma iznine sahip.

[!code-csharp[FxCop.Security.MethodLevelSecurity#1](../code-quality/codesnippet/CSharp/ca2114-method-security-should-be-a-superset-of-type_1.cs)]

## <a name="example-2"></a>Örnek 2

Aşağıdaki uygulama kodu, tür düzeyi güvenlik gereksinimini karşılamadığında bile yöntemi çağırarak kitaplığın güvenlik açığını gösterir.

[!code-csharp[FxCop.Security.TestMethodLevelSecurity#1](../code-quality/codesnippet/CSharp/ca2114-method-security-should-be-a-superset-of-type_2.cs)]

Bu örnek aşağıdaki çıktıyı üretir:

```txt
[All permissions] Personal information: 6/16/1964 12:00:00 AM
[No write permission (demanded by type)] Personal information: 6/16/1964 12:00:00 AM
[No read permission (demanded by method)] Could not access personal information: Request failed.
```

## <a name="see-also"></a>Ayrıca bkz.

- [Güvenli Kodlama Yönergeleri](/dotnet/standard/security/secure-coding-guidelines)
- [Bağlantı talepleri](/dotnet/framework/misc/link-demands)
- [Veri ve Modelleme](/dotnet/framework/data/index)