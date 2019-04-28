---
title: Hareketlilik Uyarıları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.codeanalysis.MobilityRules
helpviewer_keywords:
- managed code analysis warnings, mobility warnings
- mobility warnings
- warnings, mobility
ms.assetid: 9808054c-593b-4fc3-92cc-1fc45f41569c
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 170caf52999fb687c040c2e9212d1a1ed2e154a0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62820680"
---
# <a name="mobility-warnings"></a>Hareketlilik Uyarıları
Hareketlilik uyarıları verimli güç kullanımını destekler.

## <a name="in-this-section"></a>Bu Bölümde

|Kural|Açıklama|
|----------|-----------------|
|[CA1600: Boş işlem önceliğini kullanmayın](../code-quality/ca1600-do-not-use-idle-process-priority.md)|İşlem önceliğini Boşta olarak ayarlamayın. Aksi durumda boş olacak ve bu nedenle beklemeyi engeller, System.Diagnostics.ProcessPriorityClass.Idle bulunan işlemleri CPU dolduracaktır.|
|[CA1601: Güç durumu değişikliklerini önleyen zamanlayıcılar kullanmayın](../code-quality/ca1601-do-not-use-timers-that-prevent-power-state-changes.md)|Yüksek frekanslı dönemsel faaliyet CPU'yu meşgul tutar ve sabit diski gösteren güç tasarruflu zamanlayıcılarla müdahale edilir.|