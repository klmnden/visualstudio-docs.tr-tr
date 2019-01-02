---
title: QueryCounters | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 8059d4b2-af61-4a47-a6c2-8da5c0741c74
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a9a4e3c9f80ed437eb4476833776c5c19689c69a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53866926"
---
# <a name="querycounters"></a>QueryCounters
**QueryCounters** seçeneği bilgisayarda kullanılabilir CPU (Donanım) performans sayaçları listeler.  
  
 **QueryCounters** yalnızca seçeneğin komut satırında olması gerekir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cmd  
VSPerfCmd.exe /QueryCounters  
```  
  
#### <a name="parameters"></a>Parametreler  
 Hiçbiri  
  
## <a name="remarks"></a>Açıklamalar  
 Araçlar yöntemini kullanırken, profil oluşturucu her veri koleksiyonu olayı, bir veya daha fazla CPU performans sayacı değerlerini toplayabilirsiniz. Örnekleme profili oluşturma yöntemi kullanırken, bir sayaç olay ve örnekleme aralığı kullanılacak olay oluşum sayısını belirtebilirsiniz.  
  
 Farklı bir işlemci, farklı bir CPU performans sayaçları kullanıma sunar. Profil Oluşturucu, neredeyse tüm işlemciler üzerinde kullanılabilir genel sayaçları kümesini tanımlar. **QueryCounters** seçeneği hem genel sayaçların adlarını ve işlemciye özgü sayaçların adlarını listeler.  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [VSPerfCmd](../profiling/vsperfcmd.md)   
 [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)   
 [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)   
 [Profil hizmetler](../profiling/command-line-profiling-of-services.md)