---
title: 'DA0010: Pahalı GetHashCode | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.rules.DAExpensiveGetHashCode
- vs.performance.DA0010
- vs.performance.rules.DA0010
- vs.performance.10
ms.assetid: 3987e21a-5b4f-45e4-8a33-6b3f0a472c08
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a2a1ddeb2b12d592c93bb0e5b88ba76c1b01c3c3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62936559"
---
# <a name="da0010-expensive-gethashcode"></a>DA0010: Pahalı GetHashCode

|||
|-|-|
|Kural Kimliği|DA0010|
|Kategori|.NET framework kullanımı|
|Profil oluşturma yöntemleri|Örnekleme<br /><br /> .NET bellek|
|İleti|GetHashCode fonksiyonları ucuz ve diğer bellek ayrılamadı. gerekir. Mümkünse karma kod işlevi karmaşıklığını azaltın.|
|İleti türü|Uyarı|

## <a name="cause"></a>Sebep
 Profil oluşturma verilerinin önemli bir kısmı GetHashCode metot türü çağrılarıdır veya yöntemi bellek ayırır.

## <a name="rule-description"></a>Kural açıklaması
 Karma, hızlı bir şekilde büyük bir koleksiyonda belirli bir öğeyi bulmak için bir tekniktir. Karma tabloları karma tabloları büyük ve çok yüksek hızda erişim desteklemek zorunda olduğundan, etkili olması gerekir. Bu gereksinim, bir olduğu çıkarımında GetHashCode yöntemler .NET Framework'te bellek ayrılamadı ' dir. Bellek ayırma, çöp toplayıcı üzerindeki yükü artırır ve çöp toplama ayırma isteğinin sonucu olarak çalıştırmak gerekli hale gelirse olası gecikmeler yöntemi kullanıma sunar.

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?
 Yöntem karmaşıklığını azaltın.