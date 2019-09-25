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
ms.openlocfilehash: 1721fd52c00c5b312c88f19d48b668b12d28f050
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71234490"
---
# <a name="ca1506-avoid-excessive-class-coupling"></a>CA1506: Aşırı sınıf bağlantısından kaçının

|||
|-|-|
|TypeName|AvoidExcessiveClassCoupling|
|CheckId|CA1506|
|Kategori|Microsoft. Bakımolmaması|
|Son değişiklik|Yeni|

## <a name="cause"></a>Sebep

Bir tür ya da yöntem diğer birçok türle birlikte bağlanmış.

## <a name="rule-description"></a>Kural açıklaması

Bu kural türü veya yöntemini içeren benzersiz türde başvuru sayısı belirlenerek eşlenmesiyle sınıfı ölçer.

Yüksek ölçüde sınıf bağlantısı olan türler ve Yöntemler devam etmek zor olabilir. Düşük ve yüksek bir cohede gösteren türler ve yöntemlere sahip olmak iyi bir uygulamadır.

## <a name="how-to-fix-violations"></a>İhlalleri çözme

Bu ihlalin giderilmesi için, türü veya yöntemi, bağlandığı türlerin sayısını azaltmak için yeniden tasarlayadeneyin.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor

Tür veya yöntem diğer türlerde çok sayıda bağımlılıklara karşın bakım yapılabilir olarak kabul edildiğinde bu uyarıyı hariç tutun.

## <a name="see-also"></a>Ayrıca bkz.

- [Bakım Uyarıları](../code-quality/maintainability-warnings.md)
- [Yönetilen Kodun Ölçüm Karmaşıklığı ve Bakımı](../code-quality/code-metrics-values.md)