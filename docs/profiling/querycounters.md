---
title: QueryCounters | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 8059d4b2-af61-4a47-a6c2-8da5c0741c74
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 501818d000b2db69b0744649d8e4a472cb87a55b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62982596"
---
# <a name="querycounters"></a>QueryCounters
**QueryCounters** seçeneği bilgisayarda kullanılabilir CPU (Donanım) performans sayaçları listeler.

 **QueryCounters** yalnızca seçeneğin komut satırında olması gerekir.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /QueryCounters
```

#### <a name="parameters"></a>Parametreler
 Yok.

## <a name="remarks"></a>Açıklamalar
 Araçlar yöntemini kullanırken, profil oluşturucu her veri koleksiyonu olayı, bir veya daha fazla CPU performans sayacı değerlerini toplayabilirsiniz. Örnekleme profili oluşturma yöntemi kullanırken, bir sayaç olay ve örnekleme aralığı kullanılacak olay oluşum sayısını belirtebilirsiniz.

 Farklı bir işlemci, farklı bir CPU performans sayaçları kullanıma sunar. Profil Oluşturucu, neredeyse tüm işlemciler üzerinde kullanılabilir genel sayaçları kümesini tanımlar. **QueryCounters** seçeneği hem genel sayaçların adlarını ve işlemciye özgü sayaçların adlarını listeler.

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)