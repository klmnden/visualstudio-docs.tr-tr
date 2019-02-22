---
title: Kapatma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: a1e37500-4ad1-4670-9737-3d9a20536386
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: deeb74e8e8763feb62b0cc21fcfbfbf3c6b220ca
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596704"
---
# <a name="shutdown"></a>Kapat
**Kapatma** seçeneği bekler herhangi şu anda son veya ayırmak için işlem profili ve ardından profil oluşturucuyu devre dışı bırakır ve profil oluşturma veri dosyasını kapatır. **Kapatma** seçeneği, bir profil oluşturma, son komut olması gerekir.

 Bir zaman aşımı parametresi belirtilmezse **kapatma** süresiz olarak seçeneğini bekler. Seçeneği bir zaman aşımı parametresi belirtilirse, belirtilen sayıda saniye geçtikten sonra profil oluşturucuyu kapatarak veya veri dosyasını kapatmadan döndürür.

 **Kapatma** seçeneği, komut satırında belirtilen tek seçenek olması gerekir.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Shutdown[:Timeout]
```

#### <a name="parameters"></a>Parametreler
 `Timeout`
 -   (İsteğe bağlı) Belirtilmişse seçeneği belirtilen sayıda saniye geçtikten sonra profil oluşturucuyu kapatarak veya profil oluşturma veri dosyasını kapatmadan döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)