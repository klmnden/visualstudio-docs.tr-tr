---
title: 'CA2222: Devralınan üye görünürlüğünü azaltmayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotDecreaseInheritedMemberVisibility
- CA2222
helpviewer_keywords:
- DoNotDecreaseInheritedMemberVisibility
- CA2222
ms.assetid: 066c8675-381f-43cc-956c-d757cc494028
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: c737a30569ab4cd59931a3fca0e500ebe96e62de
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71230979"
---
# <a name="ca2222-do-not-decrease-inherited-member-visibility"></a>CA2222: Devralınan üye görünürlüğünü azaltmayın

|||
|-|-|
|TypeName|DoNotDecreaseInheritedMemberVisibility|
|CheckId|CA2222|
|Kategori|Microsoft. Usage|
|Son değişiklik|Kırılmamış|

## <a name="cause"></a>Sebep

Korumasız bir türdeki özel bir yöntem, bir temel tür içinde belirtilen ortak bir yöntemle aynı imzaya sahip. Özel yöntem son değil.

## <a name="rule-description"></a>Kural açıklaması

Devralınan Üyeler için erişim değiştiricisini değiştirmeyin. Devralınmış bir üyeyi özel olarak değiştirme, arayanların yöntemin temel sınıf uygulamasına erişmesini engellemez. Üye özel hale getirilme ve tür korumasız ise, devralan türler, devralma hiyerarşisindeki metodun son ortak uygulamasını çağırabilir. Erişim değiştiricisini değiştirmeniz gerekiyorsa, yöntemin geçersiz olarak işaretlenmesi gerekir ya da yöntemin geçersiz kılınmasını engellemek için türünün mühürlü olması gerekir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kural ihlalini onarmak için erişimi özel olmayan şekilde değiştirin. Alternatif olarak, programlama diliniz destekliyorsa, yöntemi son haline getirebilirsiniz.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek

Aşağıdaki örnek, bu kuralı ihlal eden bir türü gösterir.

[!code-vb[FxCop.Usage.InheritedPublic#1](../code-quality/codesnippet/VisualBasic/ca2222-do-not-decrease-inherited-member-visibility_1.vb)]
[!code-csharp[FxCop.Usage.InheritedPublic#1](../code-quality/codesnippet/CSharp/ca2222-do-not-decrease-inherited-member-visibility_1.cs)]