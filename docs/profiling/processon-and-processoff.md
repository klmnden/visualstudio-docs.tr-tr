---
title: ProcessOn ve ProcessOff | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d3dc6a7e-bc0f-48a6-a4ec-f386348bb296
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ab218f8dabb2b4360c1be17d809399a752f7cc2c
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62972424"
---
# <a name="processon-and-processoff"></a>ProcessOn ve ProcessOff
VSPerfCmd.exe **ProcessOff** ve **ProcessOn** alt komutları duraklatma ve komut satırı profil oluşturma oturumu içinde belirtilen işlem için profil oluşturmayı sürdürün. **ProcessOff** profil oluşturma işlemi durdurur ve **ProcessOn** işlemi profil oluşturmaya başlar.

 Çoğu durumda, belirttiğiniz **ProcessOn** veya **ProcessOff** yalnızca bir VSPerfCmd.exe seçenek olarak komut satırı, ancak aynı zamanda ile birleştirilebilir **GlobalOn**, **GlobalOff**, **ThreadOn**, ve **ThreadOff** alt komutları.

 **ProcessOn** ve **ProcessOff** alt komutları etkileşimde **GlobalOn** ve **GlobalOff** veri denetimi komutları komut satırı profil oluşturma oturumunu, tüm işlemler için koleksiyonda ve **ThreadOn** ve **ThreadOff** belirtilen iş parçacığı için veri toplamayı kontrol alt komutları.

 **ProcessOff** ve **ProcessOn** alt komutları da profil oluşturucu API işlevleri tarafından yönetilen işlemi Başlat/Durdur sayısını etkiler.

- **ProcessOff** hemen işlem Başlat/Durdur sayısı 0 olarak ayarlar ve bu nedenle profil oluşturma duraklatır.

- **ProcessOn** hemen işlem Başlat/Durdur sayısı 1 olarak ayarlar ve bu nedenle sürdürür profil oluşturma.

  Daha fazla bilgi için [Profil Araçları API'leri](../profiling/profiling-tools-apis.md).

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /{ProcessOff|ProcessOn}:PID [Options]

```

#### <a name="parameters"></a>Parametreler
 `PID` Başlatma veya durdurma işlemini tamsayı tanımlayıcısı. İşlem kimliklerini listelenen **işlem** Windows Görev Yöneticisi'nin sekmesinde.

## <a name="required-subcommands"></a>Gerekli bir alt komutları
 Yok.

## <a name="valid-subcommands"></a>Geçerli alt komutları
 **ProcessOn** ve **ProcessOff** de aşağıdaki komutları içeren komut satırlarında belirtilebilir.

 **Başlat:** `Method` Komut satırı profil oluşturma oturumu başlatır ve belirtilen profil oluşturma yöntemini ayarlar.

 **Başlat:** `AppName` Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.

 **Ekleme:** `PID` Belirtilen işlem profil oluşturma başlar.

 **GlobalOff**&#124;**GlobalOn** durdurur veya tüm işlemler için profil oluşturma bir komut satırı profil oluşturma oturumu başlatır.

 {**ThreadOff**&#124;**ThreadOn**}**:**`TID` Durdurur veya belirtilen iş parçacığı (yalnızca izleme metodunu) için profil oluşturmaya başlar.

## <a name="example"></a>Örnek
 Bu örnekte, **ProcessOff** alt uygulama başlatma için profil oluşturma verilerini toplamak için kullanılır.

```cmd
; Initialize the profiler.
VSPerfCmd.exe /Start:Trace /Output:Instrument.vsp
; Start the instrumented application.
; Stop profiling the process after startup.
VSPerfCmd.exe /ProcessOff:12345
; Shut down the target application.
; Close the profiler.
VSPerfCmd /Shutdown

```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)