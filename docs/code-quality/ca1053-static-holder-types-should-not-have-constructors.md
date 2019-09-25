---
title: 'CA1053: Static tutucu türlerin oluşturucuları olmamalıdır'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- StaticHolderTypesShouldNotHaveConstructors
- CA1053
helpviewer_keywords:
- CA1053
- StaticHolderTypesShouldNotHaveConstructors
ms.assetid: 10302b9a-fa5e-4935-a06a-513d9600f613
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 44bdb8c12b48a983b88e6a035fc1522856b306be
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235579"
---
# <a name="ca1053-static-holder-types-should-not-have-default-constructors"></a>CA1053: Statik tutucu türleri varsayılan oluşturuculara sahip olmamalıdır

|||
|-|-|
|TypeName|StaticHolderTypesShouldNotHaveConstructors|
|CheckId|CA1053|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

> [!NOTE]
> Rule CA1053, [CA1052 ile birleştirilmiştir: Statik tutucu türleri [FxCop çözümleyicileri](fxcop-analyzers.yml)içinde](ca1052-static-holder-types-should-be-sealed.md) mühürlenmelidir.

## <a name="cause"></a>Sebep

Ortak veya iç içe ortak tür yalnızca statik üyeleri bildirir ve varsayılan bir oluşturucuya sahiptir.

## <a name="rule-description"></a>Kural açıklaması

Statik üyeleri çağırmak türde bir örnek gerektirmediğinden, varsayılan Oluşturucu gereksizdir. Ayrıca, tür statik olmayan üyelere sahip olmadığından, örnek oluşturmak türün üyelerinden hiçbirine erişim sağlamaz.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlalini onarmak için varsayılan oluşturucuyu kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan uyarıyı bastırmayın. Varsayılan oluşturucunun varlığı, türün statik bir tür olmadığını önerir.