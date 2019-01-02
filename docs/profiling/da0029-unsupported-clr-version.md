---
title: 'DA0029: Desteklenmeyen CLR sürümü | Microsoft Docs'
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.29
- vs.performance.rules.DA0029
helpviewer_keywords:
- vs.performance.29
- vs.performance.DA0029
- vs.performance.rules.DA0029
ms.assetid: 76247259-c6f3-44c4-b3f9-d8dac16b5e0d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c52d9ee8ba8488ef8dd3f343aab172689d907532
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53948965"
---
# <a name="da0029-unsupported-clr-version"></a>DA0029: Desteklenmeyen CLR sürümü

|||  
|-|-|  
|Kural Kimliği|DA0029|  
|Kategori|Profil oluşturma araçları kullanım|  
|Profil oluşturma yöntemi|Komut satırından profil oluşturma|  
|İleti|Koleksiyon sırasında desteklenmeyen CLR sürümü algılandı. Yönetilen semboller düzgün çözülemiyor olabilir.|  
|Kural türü|Bilgiler.|  

## <a name="cause"></a>Sebep  
 Kullanan bir uygulama profili çalıştığınız [!INCLUDE[net_v11_long](../profiling/includes/net_v11_long_md.md)] profil oluşturma araçları tarafından desteklenmiyor.  

## <a name="rule-description"></a>Kural açıklaması  
 Profil oluşturma araçlarından uygulama içinde çalışan yönetilen kod için simgeleri çözme mümkün olmayacaktır. Bu uyarı oluşur. Profil oluşturma araçlarından çalışmakta olan uygulamalar için yönetilen kodu sembol çözümlenemiyor [!INCLUDE[net_v11_long](../profiling/includes/net_v11_long_md.md)].  

## <a name="how-to-fix-violations"></a>İhlaller nasıl düzeltilir?  
 Yok.