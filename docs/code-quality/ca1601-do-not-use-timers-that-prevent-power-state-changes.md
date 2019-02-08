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
ms.openlocfilehash: fc6db6dff5ee4c4e4d387399dbf79277046d6c02
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55931864"
---
# <a name="ca1601-do-not-use-timers-that-prevent-power-state-changes"></a>CA1601: Güç durumu değişikliklerini önleyen zamanlayıcılar kullanmayın

|||
|-|-|
|TypeName|DoNotUseTimersThatPreventPowerStateChanges|
|CheckId|CA1601|
|Kategori|Microsoft.Mobility|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Zamanlayıcı, saniye başına birden fazla kez gerçekleşecek şekilde ayarlanan bir aralığı vardır.

## <a name="rule-description"></a>Kural açıklaması
 İkinci ya da birden daha sık gerçekleşmesine kullanım zamanlayıcılar başına bir kez daha sık yoklama değil saniye başına zaman. Yüksek frekanslı dönemsel faaliyet CPU'yu meşgul tutar ve sabit diski gösteren güç tasarruflu zamanlayıcılarla müdahale edilir.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Zamanlayıcı aralıkları saniyede saatten daha az bir kez gerçekleşecek şekilde ayarlayın.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kural yalnızca saniye başına birden fazla kez Zamanlayıcı tetikleme gereklidir ve mobility konuları güvenle görmezden gelinebilir atlanması.