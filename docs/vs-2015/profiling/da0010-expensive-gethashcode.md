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
ms.openlocfilehash: 1055136562d59412a6187524dc6023c55ef2dc3c
ms.sourcegitcommit: 53aa5a413717a1b62ca56a5983b6a50f7f0663b3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/17/2019
ms.locfileid: "59659039"
---
# <a name="da0010-expensive-gethashcode"></a>DA0010: Pahalı GetHashCode
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio ile ilgili en son belgeler için bkz. [DA0010: Pahalı GetHashCode](https://docs.microsoft.com/visualstudio/profiling/da0010-expensive-gethashcode).  

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
 Karma, hızlı bir şekilde büyük bir koleksiyonda belirli bir öğeyi bulmak için bir tekniktir. Karma tabloları karma tablo çok büyük olabilir ve erişim yüksek oranlarda desteklemek zorunda olduğundan, son derece verimli olması gerekir. Bu gereksinim, bir olduğu çıkarımında GetHashCode yöntemler .NET Framework'te bellek ayrılamadı ' dir. Bellek ayırma, çöp toplayıcı üzerindeki yükü artırır ve çöp toplama ayırma isteğinin sonucu olarak çalıştırmak gerekli hale gelirse olası gecikmeler yöntemi kullanıma sunar.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Yöntem karmaşıklığını azaltın.
