---
title: 'CA1600: Boş işlem önceliğini kullanmayın'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- DoNotUseIdleProcessPriority
- CA1600
helpviewer_keywords:
- CA1600
- DoNotUseIdleProcessPriority
ms.assetid: 9b0d073b-78b6-41be-8ef3-14692a735283
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a1774b3feb2da4939420bf75506892aac6dedd72
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55955797"
---
# <a name="ca1600-do-not-use-idle-process-priority"></a>CA1600: Boş işlem önceliğini kullanmayın

|||
|-|-|
|TypeName|DoNotUseIdleProcessPriority|
|CheckId|CA1600|
|Kategori|Microsoft.Mobility|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
 Bu kural işlemleri ayarlandığından oluşur `ProcessPriorityClass.Idle`.

## <a name="rule-description"></a>Kural açıklaması
 İşlem önceliğini Boşta olarak ayarlamayın. Sahip işlemler `System.Diagnostics.ProcessPriorityClass.Idle` Aksi durumda boş olacak ve bu nedenle beklemeyi engeller, CPU dolduracaktır.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Ayarlama işlemleri `ProcessPriorityClass.BelowNormal`.

## <a name="when-to-suppress-warnings"></a>Uyarılar bastırıldığında
 Bu kural yalnızca boş işlem önceliğini gereklidir ve mobility konuları güvenle görmezden gelinebilir atlanması.