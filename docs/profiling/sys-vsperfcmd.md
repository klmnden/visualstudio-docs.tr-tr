---
title: Sys (VSPerfCmd) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 294a6f9e-b49f-4c83-b322-5ac5411b66fb
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5f0a63cfca8e06d999c585793fabdce627d4896d
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62968047"
---
# <a name="sys-vsperfcmd"></a>Sys (VSPerfCmd)
*VSPerfCmd.exe* **Sys** seçeneği ayarlar sistem çağrısı olaylarını (işletim sistemi profili oluşturulmuş uygulamadan işlev çağrıları) için örneklenir ve isteğe bağlı olarak numarasını değiştirir profil oluşturma olayı Sistem çağrıları bir örnekleme aralığı varsayılan 10.

 **Sys** de içeren bir komut satırında yalnızca kullanılabilir **başlatma** veya **iliştirme** seçeneği.

 Varsayılan olarak, profil oluşturucu örnekleme olay işlemci saat döngülerini için ayarlanır ve örnekleme aralığı 10,000,000 için ayarlanır. **Zamanlayıcı**, **PF**, **Sys**, ve **sayacı** seçenekleri örnekleme olay ve örnekleme aralığı ayarlamanızı sağlar. **GC** seçeneği her ayırma ve atık toplama etkinlikte .NET bellek verileri toplar. Bir komut satırında bu seçenekleri yalnızca biri belirtilebilir.

 Örnekleme olay ve örnekleme aralığı yalnızca ilk komut içeren satırı ayarlanabilir bir **başlatma** veya **iliştirme** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe {/Launch:AppName|Attach:PID} /Sys[:Events] [Options]
```

#### <a name="parameters"></a>Parametreler
 `Events` Sistem sayısını belirten bir tamsayı değeri, bir örnekleme aralığındaki olayları arayın. Varsa `Events` belirtilmezse, aralığı 10'a ayarlayın.

## <a name="required-options"></a>Gerekli seçenekleri
 **Sys** aşağıdaki seçeneklerden birini gerektirir.

 **Başlat:** `AppName` Profil Oluşturucu ve tarafından belirtilen uygulamayı başlatır `AppName`.

 **Ekleme:** `PID` Tarafından belirtilen işlem için profil oluşturucuya iliştirir `PID`.

## <a name="invalid-options"></a>Geçersiz Seçenekler
 Aşağıdaki seçenekler aynı komut satırında belirtilemez **Sys**.

 **PF**[**:**`Events`] örnekleme olay sayfa hataları için ayarlar ve isteğe bağlı olarak örnekleme aralığı ayarlar `Events`. Varsayılan PF aralığı 10'dur.

 **Zamanlayıcı**[**:**`Cycles`] ayarlar işlemci saat için örnekleme olay geçiş yapar ve isteğe bağlı olarak örnekleme aralığı ayarlar `Cycles`. Varsayılan Zamanlayıcı 10,000,000 aralığıdır.

 **Sayaç:** `Name`[`,Reload`[`,FriendlyName`]] sayaç tarafından belirtilen CPU performansı için örnekleme olay ayarlar `Name` ve örnekleme aralığı ayarlar `Reload`.

 **GC**[**:**{**ayırma**&#124;**ömrü**}] toplar .NET bellek verileri. Varsayılan olarak (**ayırma**), her bir bellek ayırma etkinlikte toplanan veriler. Zaman **ömrü** parametresi belirtildiğinde, veriler ayrıca her çöp toplama olayını toplanır.

## <a name="example"></a>Örnek
 Bu örnek, profil oluşturucu örnekleme olay sistem çağrıları ayarlama ve örnekleme aralığı için örnek başına 20 çağrıları nasıl ayarlanacağını gösterir.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /Sys:20
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)