---
title: Konsol | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: e825ba66-1383-46ad-8712-396bc9c14036
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 74a5cecbdf3bba942c888a5cde3d49236047f4ee
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62553194"
---
# <a name="console"></a>Konsol
VSPerfCmd.exe **konsol** seçenek, yeni bir komut istemi penceresinde belirtilen uygulamayı başlatır. **Konsol** VSPerfCmd ile yalnızca kullanılabilir **başlatma** seçeneği. Uygulamayı bir komut satırı uygulaması değilse **konsol** hiçbir etkisi olmaz.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Launch:AppName /Console
```

#### <a name="parameters"></a>Parametreler
 None

## <a name="required-options"></a>Gerekli seçenekleri
 **Konsol** yalnızca de içeren bir komut satırında belirtilebilir **başlatma** seçeneği.

 **Başlat:** `AppName` Profil Oluşturucu ve tarafından belirtilen uygulamayı başlatır `AppName`.

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)