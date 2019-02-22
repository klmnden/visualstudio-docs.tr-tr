---
title: Otomatik işaret zamanının | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: c4de965e-0364-4f78-9936-1f509e85df74
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2d2bbd33308ddf14f14746db7f5c2c4ada6826b6
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56634116"
---
# <a name="automark"></a>AutoMark
**AutoMark** seçeneği, Windows yazılım performansı sayaç olaylarını koleksiyonunu arasındaki milisaniye sayısını belirtir. Windows performans sayaçları belirtilir **WinCounter** seçeneği.

 Yalnızca bir **AutoMark** seçeneği, komut satırında belirtilebilir. Unutmayın **WinCounter** örnekleme aralığı tarafından belirtilen **AutoMark** ana örnekleme aralığı bağımsızdır.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Start:Method /WinCounter:Path /AutoMark:Milliseconds
```

#### <a name="parameters"></a>Parametreler
 `Milliseconds` Windows performansı sayaç olaylarını koleksiyonları arasında geçen milisaniye sayısını belirtir.

## <a name="required-options"></a>Gerekli seçenekleri
 **WinCounter:** `Path` Toplanacak Windows performans sayacı belirtir. Araçlar yöntemini kullanırken, birden çok Windows sayaçları belirtilebilir. Örnekleme yöntemini kullanırken, yalnızca bir yazılım sayacı belirtilebilir. **WinCounter** içeren bir komut satırı seçeneği belirtilen **Başlat** seçeneği.

## <a name="example"></a>Örnek
 Bu örnekte, iki Windows performans sayaçları için 1000 milisaniye cinsinden örnekleme aralığı ayarlanır.

```cmd
VSPerfCmd.exe /Start:Trace /Output:TestApp.exe.vsp /WinCounter:"\Process(*)\% Processor Time" /WinCounter:"\ASP.NET\Pages/sec" /AutoMark:1000
VSPerfCmd.exe /Launch:TestApp.exe
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)