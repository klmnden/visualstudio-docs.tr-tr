---
title: ThreadOn ve ThreadOff | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 5cd5a695-0a14-484a-8952-ed47e13d8e92
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2516ff5597151e65276b0fcb2bef5bb81c929cd3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62965238"
---
# <a name="threadon-and-threadoff"></a>ThreadOn ve ThreadOff
*VSPerfCmd.exe* **ThreadOff** ve **ThreadOn** alt komutları şüpheli işlem yöntemini kullanan komut satırı profil oluşturma oturumunda kullanılabilir yalnızca. **ThreadOff** ve **ThreadOn** duraklatma ve sürdürme belirtilen iş parçacığı profil oluşturma. **ThreadOff** iş parçacığı profil oluşturmayı durdurur ve **ThreadOn** iş parçacığı profil oluşturmaya başlar.

 Çoğu durumda, belirttiğiniz **ThreadOn** veya **ThreadOff** yalnızca seçeneği olarak bir *VSPerfCmd.exe* komut satırı, ancak bunlar ile de birleştirilebilir  **GlobalOn**, **GlobalOff**, **ProcessOn**, ve **ProcessOff** alt komutları.

 **ThreadOn** ve **ThreadOff** alt komutları etkileşimde **GlobalOn** ve **GlobalOff** veri denetimi komutları komut satırı profil oluşturma oturumunu, tüm işlemler için koleksiyonda ve **ProcessOn** ve **ProcessOff** belirtilen işlem için veri toplamayı kontrol alt komutları.

 **ThreadOff** ve **ThreadOn** alt komutları da profil oluşturucu API işlevleri tarafından yönlendirilen iş parçacığı Başlat/Durdur sayısını etkiler.

- **ThreadOff** hemen iş parçacığı Başlat/Durdur sayısı 0 olarak ayarlar ve bu nedenle profil oluşturma duraklatır.

- **ThreadOn** hemen iş parçacığı Başlat/Durdur sayısını 1 olarak ayarlar ve bu nedenle sürdürür profil oluşturma.

  Daha fazla bilgi için [Profil Araçları API'leri](../profiling/profiling-tools-apis.md).

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /{ThreadOff|ThreadOn}:TID [Options]

```

#### <a name="parameters"></a>Parametreler
 `TID` İş parçacığı başlatmak veya durdurmak için tamsayı tanımlayıcısı.

## <a name="valid-options"></a>Geçerli seçenekler şunlardır:
 **ThreadOn** ve **ThreadOff** de aşağıdaki komutları içeren komut satırlarında belirtilebilir.

 **Başlat:** `Method` Komut satırı profil oluşturma oturumu başlatır ve belirtilen profil oluşturma yöntemini ayarlar.

 **GlobalOff**&#124;**GlobalOn** durdurur veya tüm işlemler için profil oluşturma bir komut satırı profil oluşturma oturumu başlatır.

 {**ProcessOff**&#124;**ProcessOn**}**:**`TID` Durdurur veya belirtilen işlem için profil oluşturmaya başlar.

## <a name="example"></a>Örnek
 Bu örnekte, **ThreadOff** alt, böylece yalnızca uygulama başlangıç verileri toplanır, profil oluşturma veri toplamayı durdurmak için kullanılır.

```cmd
; Initialize the profiler.
VSPerfCmd.exe /Start:Trace /Output:Instrument.vsp
; Start the instrumented application.
; Stop profiling the thread after startup.
VSPerfCmd.exe /ThreadOff:12345
; Shut down the target application.
; Close the profiler.
VSPerfCmd /Shutdown

```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)