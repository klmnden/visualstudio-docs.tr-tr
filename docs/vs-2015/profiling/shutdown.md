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
ms.openlocfilehash: b9b8848399ea88b5f4ce7ebf30f970e2091e6406
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54784605"
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
 -   (İsteğe bağlı) Belirtilmişse seçeneği belirtilen sayıda saniye geçtikten sonra profil oluşturucuyu kapatmak veya profil oluşturma veri dosyasını kapatmadan döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
