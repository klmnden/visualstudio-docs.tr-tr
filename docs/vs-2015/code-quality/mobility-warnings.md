---
title: Hareketlilik uyarıları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- vs.codeanalysis.MobilityRules
helpviewer_keywords:
- managed code analysis warnings, mobility warnings
- mobility warnings
- warnings, mobility
ms.assetid: 9808054c-593b-4fc3-92cc-1fc45f41569c
caps.latest.revision: 19
author: gewarren
ms.author: gewarren
manager: wpickett
ms.openlocfilehash: e67be4e501cb2d0dd9d584250fcea91af13fe657
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68201247"
---
# <a name="mobility-warnings"></a>Hareketlilik Uyarıları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Hareketlilik uyarıları verimli güç kullanımını destekler.  
  
## <a name="in-this-section"></a>Bu Bölümde  
  
|Kural|Açıklama|  
|----------|-----------------|  
|[CA1600: Boş işlem önceliğini kullanmayın](../code-quality/ca1600-do-not-use-idle-process-priority.md)|İşlem önceliğini Boşta olarak ayarlamayın. Aksi durumda boş olacak ve bu nedenle beklemeyi engeller, System.Diagnostics.ProcessPriorityClass.Idle bulunan işlemleri CPU dolduracaktır.|  
|[CA1601: Güç durumu değişikliklerini önleyen zamanlayıcılar kullanmayın](../code-quality/ca1601-do-not-use-timers-that-prevent-power-state-changes.md)|Yüksek frekanslı dönemsel faaliyet CPU'yu meşgul tutar ve sabit diski gösteren güç tasarruflu zamanlayıcılarla müdahale edilir.|
