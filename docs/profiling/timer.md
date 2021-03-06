---
title: Zamanlayıcı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 1971868e-89fa-4452-8ee7-76e4daf31b66
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 351b5a8da781d8e60d6a603c1d037f8bf71cd317
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62999320"
---
# <a name="timer"></a>Zamanlayıcı
*VSPerfCmd.exe* **Zamanlayıcı** seçeneği ayarlar profil oluşturma olayı için işlemci saat döngülerini örneklenir ve isteğe bağlı olarak 10,000,000 varsayılan bir örnekleme aralığı döngüleri sayısını değiştirir. 10.000.000 saat döngüsü, bir adet 1GH (bir gigahertz) işlemci üzerinde saniyede yaklaşık 100 örnek olduğu. Belirtilebilir döngülerini en küçük sayısı 50. 000 ' dir.

 **Zamanlayıcı** yalnızca örnekleme profili oluşturma yöntemi kullanın ve bu da içeren bir komut satırında kullanılabilir olduğunda kullanılabilir **başlatma** veya **iliştirme** seçeneği.

 Varsayılan olarak, profil oluşturucu örnekleme olay işlemci saat döngülerini için ayarlanır ve örnekleme aralığı 10,000,000 için ayarlanır. **Zamanlayıcı**, **PF**, **Sys**, ve **sayacı** seçenekleri örnekleme olay ve örnekleme aralığı ayarlamanızı sağlar. **GC** seçeneği her ayırma ve atık toplama etkinlikte .NET bellek verileri toplar. Bir komut satırında bu seçenekleri yalnızca biri belirtilebilir.

 Örnekleme olay ve örnekleme aralığı yalnızca ilk komut içeren satırı ayarlanabilir bir **başlatma** veya **iliştirme** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe {/Launch:AppName|/Attach:PID} /Timer[:Cycles] [Options]
```

#### <a name="parameters"></a>Parametreler
 `Cycles` Bir örnekleme aralığındaki işlemci saat döngüsü sayısını belirten bir tamsayı değeri. Varsa `Cycles` belirtilmezse, aralık 10,000,000 için ayarlanır. Virgül olmayan bir değer belirtin.

## <a name="required-options"></a>Gerekli seçenekleri
 **Zamanlayıcı** yalnızca aşağıdaki seçeneklerden birini içeren bir komut satırında belirtilebilir.

 **Başlat:** `AppName` Profil Oluşturucu ve tarafından belirtilen uygulamayı başlatır `AppName`.

 **Ekleme:** `PID` İşlem kimliği tarafından belirtilen işlem için profil oluşturucuyu ekler (`PID`).

## <a name="invalid-options"></a>Geçersiz Seçenekler
 Aşağıdaki seçenekler aynı komut satırında belirtilemez **Zamanlayıcı**.

 **PF**[**:**`Events`] örnekleme olay sayfa hataları için ayarlar ve isteğe bağlı olarak örnekleme aralığı ayarlar `Events`. Varsayılan PF aralığı 10'dur.

 **Sys**[**:**`Events`] ayarlar işletim sistemi için örnekleme olay çağırır ve isteğe bağlı olarak örnekleme aralığı ayarlar `Events`. Varsayılan Sys aralığı 10'dur.

 **Sayaç**[**:**`Name,Reload,FriendlyName`] sayaç tarafından belirtilen CPU performansı için örnekleme olay ayarlar `Name` ve örnekleme aralığı ayarlar `Reload`.

 **GC**[**:**{**ayırma**&#124;**ömrü**}] toplar .NET bellek verileri. Varsayılan olarak (**ayırma**), her bir bellek ayırma etkinlikte toplanan veriler. Zaman **ömrü** parametresi belirtildiğinde, veriler ayrıca her çöp toplama olayını toplanır.

## <a name="example"></a>Örnek
 Bu örnek, profil oluşturucu örnekleme aralığı için 1.000.000 işlemci döngülerinin ayarlama işlemini gösterir.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /Timer:1000000
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)