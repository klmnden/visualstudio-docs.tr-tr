---
title: 'CA1061: Temel sınıf metotlarını gizlemeyin'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1061
- DoNotHideBaseClassMethods
helpviewer_keywords:
- DoNotHideBaseClassMethods
- CA1061
ms.assetid: 0bda9dc8-87b4-4038-ab9d-563298387466
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eacd20dee0758ff481b259807ba52bb78b26f5d2
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71235384"
---
# <a name="ca1061-do-not-hide-base-class-methods"></a>CA1061: Temel sınıf metotlarını gizlemeyin

|||
|-|-|
|TypeName|DoNotHideBaseClassMethods|
|CheckId|CA1061|
|Kategori|Microsoft.Design|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep
Türetilmiş bir tür, aynı ada sahip ve temel yöntemlerinden biri ile aynı sayıda parametreye sahip bir yöntem bildirir; bir veya daha fazla parametre, temel yöntemde karşılık gelen parametrenin temel türüdür; ve kalan parametrelerde, temel yöntemde karşılık gelen parametrelerle özdeş olan türler vardır.

## <a name="rule-description"></a>Kural açıklaması
Türetilmiş yöntemin parametre imzası yalnızca temel yöntemin parametre imzasında karşılık gelen türlerden daha zayıf olan türlere göre farklılık gösterdiğinde, temel türdeki bir yöntem türetilmiş bir tür içinde aynı adlı bir yöntem tarafından gizlenir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Bu kural ihlalini onarmak için yöntemi kaldırın veya yeniden adlandırın ya da yöntemin temel yöntemi gizlemez şekilde parametre imzasını değiştirin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kuraldan uyarıyı bastırmayın.

## <a name="example"></a>Örnek
Aşağıdaki örnek, kuralı ihlal eden bir yöntemi gösterir.

[!code-csharp[FxCop.Design.HideBaseMethod#1](../code-quality/codesnippet/CSharp/ca1061-do-not-hide-base-class-methods_1.cs)]