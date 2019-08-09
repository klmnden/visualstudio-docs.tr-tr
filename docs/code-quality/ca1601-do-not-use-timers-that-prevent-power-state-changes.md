---
title: 'CA1601: Güç durumu değişikliklerini önleyen zamanlayıcılar kullanmayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CA1601
- DoNotUseTimersThatPreventPowerStateChanges
helpviewer_keywords:
- CA1601
- DoNotUseTimersThatPreventPowerStateChanges
ms.assetid: b8028c92-0696-4c54-9773-0028f29bda9a
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6b3c3fe41332d488d180ddafbedfe29da1a3855e
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921785"
---
# <a name="ca1601-do-not-use-timers-that-prevent-power-state-changes"></a>CA1601: Güç durumu değişikliklerini önleyen zamanlayıcılar kullanmayın

|||
|-|-|
|TypeName|DoNotUseTimersThatPreventPowerStateChanges|
|CheckId|CA1601|
|Kategori|Microsoft. Mobility|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bir zamanlayıcının bir saniye başına birden fazla kez gerçekleşmesi için ayarlanmış bir aralığı vardır.

## <a name="rule-description"></a>Kural açıklaması
Saniyede bir kez daha fazla yoklama yapın veya saniye başına bir kez daha sık gerçekleşen zamanlayıcılar kullanın. Yüksek frekanslı dönemsel faaliyet CPU'yu meşgul tutar ve sabit diski gösteren güç tasarruflu zamanlayıcılarla müdahale edilir.

## <a name="how-to-fix-violations"></a>İhlalleri çözme
Zamanlayıcı aralıklarını saniye başına bir kez gerçekleşmeyecek şekilde ayarlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kural, yalnızca süreölçeri bir saniyede birden fazla kez tetiklebilme gerekliyse ve hareketlilik konuları güvenle yoksayılırsa bastırılır.