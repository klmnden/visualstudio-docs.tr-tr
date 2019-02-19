---
title: QueryCounters | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: conceptual
ms.assetid: 8059d4b2-af61-4a47-a6c2-8da5c0741c74
caps.latest.revision: 14
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cdd2707a6af2b9d03e73c696884dc12413437b04
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54760131"
---
# <a name="querycounters"></a>QueryCounters
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

**QueryCounters** seçeneği bilgisayarda kullanılabilir CPU (Donanım) performans sayaçları listeler.  
  
 **QueryCounters** yalnızca seçeneğin komut satırında olması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```  
VSPerfCmd.exe /QueryCounters  
```  
  
#### <a name="parameters"></a>Parametreler  
 Hiçbiri  
  
## <a name="remarks"></a>Açıklamalar  
 Araçlar yöntemini kullanırken, profil oluşturucu her veri koleksiyonu olayı, bir veya daha fazla CPU performans sayacı değerlerini toplayabilirsiniz. Örnekleme profili oluşturma yöntemi kullanırken, bir sayaç olay ve örnekleme aralığı kullanılacak olay oluşum sayısını belirtebilirsiniz.  
  
 Farklı bir işlemci, farklı bir CPU performans sayaçları kullanıma sunar. Profil Oluşturucu, neredeyse tüm işlemciler üzerinde kullanılabilir genel sayaçları kümesini tanımlar. **QueryCounters** seçeneği hem genel sayaçların adlarını ve işlemciye özgü sayaçların adlarını listeler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [ASP.NET Web uygulamalarında profil oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil Oluşturma Hizmetleri](../profiling/command-line-profiling-of-services.md)
