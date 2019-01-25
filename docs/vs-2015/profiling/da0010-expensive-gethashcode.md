---
title: 'DA0010: Pahalı GetHashCode | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.rules.DAExpensiveGetHashCode
- vs.performance.DA0010
- vs.performance.rules.DA0010
- vs.performance.10
ms.assetid: 3987e21a-5b4f-45e4-8a33-6b3f0a472c08
caps.latest.revision: 16
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4576806131572c3bb7875748fead51327d3d718f
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54804838"
---
# <a name="da0010-expensive-gethashcode"></a>DA0010: Pahalı GetHashCode
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio 2017 ile ilgili en son belgeler için bkz. [DA0010: Pahalı GetHashCode](https://docs.microsoft.com/visualstudio/profiling/da0010-expensive-gethashcode) docs.microsoft.com'da.  

  

|||  
|-|-|  
|Kural Kimliği|DA0010|  
|Kategori|.NET framework kullanımı|  
|Profil oluşturma yöntemleri|Örnekleme<br /><br /> .NET bellek|  
|İleti|GetHashCode fonksiyonları ucuz ve diğer bellek ayrılamadı. gerekir. Mümkünse karma kod işlevi karmaşıklığını azaltın.|  
|İleti türü|Uyarı|  
  
## <a name="cause"></a>Sebep  
 Profil oluşturma verilerinin önemli bir kısmı GetHashCode metot türü çağrılarıdır veya yöntemi bellek ayırır.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Karma, hızlı bir şekilde büyük bir koleksiyonda belirli bir öğeyi bulmak için bir tekniktir. Karma tabloları karma tablo çok büyük olabilir ve çok yüksek hızda erişim desteklemek zorunda olduğundan, son derece verimli olması gerekir. Bu gereksinim, bir olduğu çıkarımında GetHashCode yöntemler .NET Framework'te bellek ayrılamadı ' dir. Bellek ayırma, çöp toplayıcı üzerindeki yükü artırır ve çöp toplama ayırma isteğinin sonucu olarak çalıştırmak için gerekli hale gelirse olası gecikmeler yöntemi kullanıma sunar.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Yöntem karmaşıklığını azaltın.
