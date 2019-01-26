---
title: 'CA1034: İç içe türler görünür olmamalıdır'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- NestedTypesShouldNotBeVisible
- CA1034
helpviewer_keywords:
- NestedTypesShouldNotBeVisible
- CA1034
ms.assetid: e9789a2c-2540-42a1-8705-ae7104011194
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CPP
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: e82189d496e6f9aaa651e59d98ce0f3ab17153c1
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54958140"
---
# <a name="ca1034-nested-types-should-not-be-visible"></a>CA1034: İç içe türler görünür olmamalıdır

|||
|-|-|
|TypeName|NestedTypesShouldNotBeVisible|
|CheckId|CA1034|
|Kategori|Microsoft.Design|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Dışarıdan görünen tür dışarıdan görünen tür bildirimi içerir. İç içe geçmiş sabit listeleri ve korumalı türler, bu kuralın dışındadır.

## <a name="rule-description"></a>Kural açıklaması
 İç içe türü başka bir tür kapsamı içinde bildirilen bir türdür. İç içe geçmiş türler, içeren türde özel uygulama ayrıntılarını kapsüllemek için kullanışlıdır. Bu amaçla kullanılan, iç içe türün dışarıdan görünür olmaması gerekir.

 Dışarıdan görünen bir iç içe geçmiş türler, mantıksal gruplandırma veya ad çakışmalarını önlemek için kullanmayın; Bunun yerine, ad alanları kullanın.

 İç içe türler bazı programcılar açıkça anlaşılmıyor üye erişilebilirliği, kavramını içerir.

 Korumalı türler, alt sınıfların ve iç içe geçmiş türler Gelişmiş özelleştirme senaryolarda kullanılabilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 İç içe türün dışarıdan görünür olmasını düşünmüyorsanız, türün erişilebilirliği değiştirin. Aksi takdirde, iç içe türün üst öğesinden kaldırın. İç içe amacı, iç içe türün kategorilere ayırmak için ise, bunun yerine bir hiyerarşi oluşturmak için bir ad kullanın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
 Aşağıdaki örnek kuralını ihlal eden bir tür gösterir.

 [!code-cpp[FxCop.Design.NestedTypes#1](../code-quality/codesnippet/CPP/ca1034-nested-types-should-not-be-visible_1.cpp)]
 [!code-csharp[FxCop.Design.NestedTypes#1](../code-quality/codesnippet/CSharp/ca1034-nested-types-should-not-be-visible_1.cs)]
 [!code-vb[FxCop.Design.NestedTypes#1](../code-quality/codesnippet/VisualBasic/ca1034-nested-types-should-not-be-visible_1.vb)]