---
title: 'CA1501: Aşırı devralmadan kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1501
- AvoidExcessiveInheritance
helpviewer_keywords:
- AvoidExcessiveInheritance
- CA1501
ms.assetid: 9e934746-1a4d-492a-91e4-085201abafa4
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: 88464effce80b6957dc8945ad17f5a39b4f449c8
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234512"
---
# <a name="ca1501-avoid-excessive-inheritance"></a>CA1501: Aşırı devralmadan kaçının

|||
|-|-|
|TypeName|AvoidExcessiveInheritance|
|CheckId|CA1501|
|Kategori|Microsoft. Bakımolmaması|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Devralma hiyerarşisinde düzeyleri dörtten fazla olan türdür.

## <a name="rule-description"></a>Kural açıklaması

İç içe yuvalanmış hiyerarşileri izlemek, anlamak ve muhafaza etmek zor olabilir. Bu kural, Analizi aynı modüldeki Hiyerarşilerle sınırlandırır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu kuralın ihlal edildiğini gidermek için, türü devralma hiyerarşisinde daha az derin olan temel bir türden türeten veya bazı ara taban türlerinden birini ortadan kaldırın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Bu kuraldan bir uyarıyı gizlemek güvenlidir. Ancak, kod bakımı daha zor olabilir. Temel türlerin görünürlüğüne bağlı olarak, bu kuralın ihlallerinin çözümlenmesi, son değişiklikler oluşturabilir. Örneğin, ortak temel türleri kaldırmak bir son değişiklik.

## <a name="example"></a>Örnek

Aşağıdaki örnek, kuralı ihlal eden bir türü gösterir:

[!code-csharp[FxCop.Maintainability.ExcessiveInheritance#1](../code-quality/codesnippet/CSharp/ca1501-avoid-excessive-inheritance_1.cs)]
[!code-vb[FxCop.Maintainability.ExcessiveInheritance#1](../code-quality/codesnippet/VisualBasic/ca1501-avoid-excessive-inheritance_1.vb)]