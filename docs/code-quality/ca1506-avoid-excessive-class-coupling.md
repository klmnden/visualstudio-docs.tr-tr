---
title: 'CA1506: Aşırı sınıf bağlantısından kaçının'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- AvoidExcessiveClassCoupling
- CA1506
helpviewer_keywords:
- AvoidExcessiveClassCoupling
- CA1506
ms.assetid: 9f0943c0-e802-4e3f-8798-2ab8653ddc80
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b655609548d3de293abe2adc0ec3fb5c6fcf297b
ms.sourcegitcommit: 36f5ffd6ae3215fe31837f4366158bf0d871f7a9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59232489"
---
# <a name="ca1506-avoid-excessive-class-coupling"></a>CA1506: Aşırı sınıf bağlantısından kaçının

|||
|-|-|
|TypeName|AvoidExcessiveClassCoupling|
|CheckId|CA1506|
|Kategori|Microsoft.Maintainability|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir türün veya yöntemin birçok diğer türleri ile birleştirilmiştir.

## <a name="rule-description"></a>Kural açıklaması

Bu kural türü veya yöntemini içeren benzersiz türde başvuru sayısı belirlenerek eşlenmesiyle sınıfı ölçer.

Türler ve bir sınıf bağlantısı yüksek ölçüde içeren yöntemlerin bakımını yapmak zor olabilir. Türler ve düşük eşlenmesiyle ve yüksek uyum göstermesi yöntemler için iyi bir uygulamadır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?

Bu ihlali gidermek için tür veya yöntem bağlı türler sayısını azaltmak için yeniden tasarlayabilir deneyin.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında

Bu uyarı, tür veya yöntem rağmen bağımlılıklar diğer türleri üzerinde çok fazla sürdürülebilir edildiği durumlarda hariç tutun.

## <a name="see-also"></a>Ayrıca bkz.

- [Bakım Uyarıları](../code-quality/maintainability-warnings.md)
- [Yönetilen Kodun Ölçüm Karmaşıklığı ve Bakımı](../code-quality/code-metrics-values.md)