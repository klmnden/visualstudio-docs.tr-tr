---
title: Kapatma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: a1e37500-4ad1-4670-9737-3d9a20536386
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: fbbbd27cfe7d720349592050419f5c73d1843c70
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60115412"
---
# <a name="shutdown"></a>Kapat
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**Kapatma** seçeneği bekler herhangi şu anda son veya ayırmak için işlem profili ve ardından profil oluşturucuyu devre dışı bırakır ve profil oluşturma veri dosyasını kapatır. **Kapatma** seçeneği, bir profil oluşturma, son komut olması gerekir.  
  
 Bir zaman aşımı parametresi belirtilmezse **kapatma** seçeneği süresiz olarak bekleyecek. Seçeneği bir zaman aşımı parametresi belirtilirse, belirtilen sayıda saniye geçtikten sonra profil oluşturucuyu kapatmak veya veri dosyasını kapatmadan döndürür.  
  
 **Kapatma** seçeneği, komut satırında belirtilen tek seçenek olması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /Shutdown[:Timeout]  
```  
  
#### <a name="parameters"></a>Parametreler  
`Timeout`  
- (İsteğe bağlı) Belirtilmişse seçeneği belirtilen sayıda saniye geçtikten sonra profil oluşturucuyu kapatmak veya profil oluşturma veri dosyasını kapatmadan döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
