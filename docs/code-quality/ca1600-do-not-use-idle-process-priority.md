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
ms.openlocfilehash: c37affc585653807912d00c1cfe365853fd6260b
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68921819"
---
# <a name="ca1600-do-not-use-idle-process-priority"></a>CA1600: Boş işlem önceliğini kullanmayın

|||
|-|-|
|TypeName|DoNotUseIdleProcessPriority|
|CheckId|CA1600|
|Kategori|Microsoft. Mobility|
|Yeni Değişiklik|Yeni|

## <a name="cause"></a>Sebep
Bu kural, işlem olarak `ProcessPriorityClass.Idle`ayarlandığında oluşur.

## <a name="rule-description"></a>Kural açıklaması
İşlem önceliğini Boşta olarak ayarlamayın. Bu işlem, aksi durumda boşta kaldığında CPU 'yu kaplayacaktırvebunedenlebeklemeyiengeller.`System.Diagnostics.ProcessPriorityClass.Idle`

## <a name="how-to-fix-violations"></a>İhlalleri çözme
İşlem olarak `ProcessPriorityClass.BelowNormal`ayarlayın.

## <a name="when-to-suppress-warnings"></a>Uyarıların ne zaman bastırılamıyor
Bu kural yalnızca boş işlem önceliği gerekli olduğunda ve hareketlilik konuları güvenli bir şekilde yoksayılarak bastırılır.