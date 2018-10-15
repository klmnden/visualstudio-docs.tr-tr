---
title: 'DA0011: Pahalı CompareTo | Microsoft Docs'
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.DA0011
- vs.performance.rules.DAExpensiveCompareTo
- vs.performance.11
- vs.performance.rules.DA0011
ms.assetid: 239a381d-0d97-4367-8668-746c93f5af2c
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0726ef4eb93d3e962e5fa39fe9cc7acbdbfbe8ca
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49210450"
---
# <a name="da0011-expensive-compareto"></a>DA0011: Pahalı CompareTo
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Visual Studio 2017 ile ilgili en son belgeler için bkz. [DA0011: pahalı CompareTo](https://docs.microsoft.com/visualstudio/profiling/da0011-expensive-compareto) docs.microsoft.com'da.  
  
|||  
|-|-|  
|Kural Kimliği|DA0011|  
|Kategori|.NET framework kullanımı|  
|Profil oluşturma yöntemleri|Örnekleme<br /><br /> .NET bellek|  
|İleti|CompareTo fonksiyonları ucuz ve diğer bellek ayrılamadı. gerekir. Mümkünse CompareTo fonksiyonunun karmaşıklığını azaltın.|  
|Kural türü|Uyarı|  
  
## <a name="cause"></a>Sebep  
 CompareTo Yöntemi türü, pahalıdır veya bellek ayırır.  
  
## <a name="rule-description"></a>Kural Tanımı  
 CompareTo Yöntemi verimli olmalıdır ve bellek ayrılamadı.  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 CompareTo Yöntemi karmaşıklığını azaltın.

