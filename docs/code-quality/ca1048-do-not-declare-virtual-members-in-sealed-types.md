---
title: 'CA1048: Sealed türlerde virtual üyeler bildirmeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotDeclareVirtualMembersInSealedTypes
- CA1048
helpviewer_keywords:
- DoNotDeclareVirtualMembersInSealedTypes
- CA1048
ms.assetid: 5dcf4a30-6f98-48a8-b8cc-7b89ea757262
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: be0e1b4865b19930f8ddf7163a36b71123bb3a55
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235705"
---
# <a name="ca1048-do-not-declare-virtual-members-in-sealed-types"></a>CA1048: Sealed türlerde virtual üyeler bildirmeyin

|||
|-|-|
|TypeName|DoNotDeclareVirtualMembersInSealedTypes|
|CheckId|CA1048|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Ortak bir tür Sealed olur ve her ikisi de `virtual` (`Overridable` Visual Basic) ve son olmayan bir yöntem bildirir. Bu kural, bu düzene uymalıdır olması gereken temsilci türleri için ihlalleri raporlamaz.

## <a name="rule-description"></a>Kural açıklaması
Türler yöntemi sanal olarak bildirir, böylece devralan türler sanal yöntemin uygulanmasını geçersiz kılabilir. Tanım olarak, korumalı bir türden bir sanal yöntem anlamsız bir şekilde bir korumalı türden devralma yapılamaz.

Visual Basic ve C# derleyiciler, türlerin bu kuralı ihlal edeceğini izin vermez.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için, yöntemi sanal değil veya türü devralınabilir yapın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın. Türü geçerli durumunda bırakmak, bakım sorunlarına neden olabilir ve herhangi bir avantaj sağlamaz.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu kuralı ihlal eden bir türü gösterir.

[!code-cpp[FxCop.Design.SealedVirtual#1](../code-quality/codesnippet/CPP/ca1048-do-not-declare-virtual-members-in-sealed-types_1.cpp)]