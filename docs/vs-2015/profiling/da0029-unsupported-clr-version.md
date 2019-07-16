---
title: 'DA0029: Desteklenmeyen CLR sürümü | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
f1_keywords:
- vs.performance.29
- vs.performance.rules.DA0029
helpviewer_keywords:
- vs.performance.29
- vs.performance.DA0029
- vs.performance.rules.DA0029
ms.assetid: 76247259-c6f3-44c4-b3f9-d8dac16b5e0d
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 532427618f476e1e187d8a1c88749810f9d157c9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68152658"
---
# <a name="da0029-unsupported-clr-version"></a>DA0029: Desteklenmeyen CLR Sürümü
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Kural Kimliği | DA0029 |  
| Kategori | Profil oluşturma araçları kullanım |  
| Profil oluşturma yöntemi | Komut satırından profil oluşturma |  
| İleti | Koleksiyon sırasında desteklenmeyen CLR sürümü algılandı. Yönetilen semboller değil çözebilir doğru. |  
| Kural türü | Bilgi. |  
  
## <a name="cause"></a>Sebep  
 Kullanan bir uygulama profili çalıştığınız [!INCLUDE[net_v11_long](../includes/net-v11-long-md.md)] profil oluşturma araçları tarafından desteklenmiyor.  
  
## <a name="rule-description"></a>Kural Tanımı  
 Profil oluşturma araçlarından uygulama içinde çalışan yönetilen kod için simgeleri çözme mümkün olmayacaktır. Bu uyarı oluşur. Profil oluşturma araçlarından çalışmakta olan uygulamalar için yönetilen kodu sembol çözümlenemiyor [!INCLUDE[net_v11_long](../includes/net-v11-long-md.md)].  
  
## <a name="how-to-fix-violations"></a>İhlaller Nasıl Düzeltilir?  
 Yok.
