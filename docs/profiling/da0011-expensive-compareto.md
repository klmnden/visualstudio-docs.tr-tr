---
title: 'DA0011: Pahalı CompareTo | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.DA0011
- vs.performance.rules.DAExpensiveCompareTo
- vs.performance.11
- vs.performance.rules.DA0011
ms.assetid: 239a381d-0d97-4367-8668-746c93f5af2c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ee5839e91e2205a98a38ed27823a26a4a127e1ac
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56621623"
---
# <a name="da0011-expensive-compareto"></a>DA0011: Pahalı CompareTo

|||
|-|-|
|Kural Kimliği|DA0011|
|Kategori|.NET framework kullanımı|
|Profil oluşturma yöntemleri|Örnekleme<br /><br /> .NET bellek|
|İleti|CompareTo fonksiyonları ucuz ve diğer bellek ayrılamadı. gerekir. Mümkünse CompareTo fonksiyonunun karmaşıklığını azaltın.|
|Kural türü|Uyarı|

## <a name="cause"></a>Sebep
 CompareTo Yöntemi türü, pahalıdır veya bellek ayırır.

## <a name="rule-description"></a>Kural açıklaması
 CompareTo Yöntemi verimli olmalıdır ve bellek ayrılamadı.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 CompareTo Yöntemi karmaşıklığını azaltın.