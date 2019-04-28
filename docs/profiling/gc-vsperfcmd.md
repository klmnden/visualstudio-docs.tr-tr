---
title: GC (VSPerfCmd) | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 7c81e88b-a748-4cf5-a7a1-3429608e1b54
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 50b2e269ec292aaf37b8d0c707fa27ff8268a1f0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969714"
---
# <a name="gc-vsperfcmd"></a>GC (VSPerfCmd)
**GC** seçenek, .NET Framework bellek ayırma ve nesne yaşam verilerinin koleksiyonunu etkinleştirir. **GC** seçeneği, yalnızca örnekleme profili oluşturma yöntemi ve yalnızca ile kullanılabilir **başlatma** seçeneği.

 Kullanırken **GC** seçeneğini VSPerfClrEnv **/sampleon** komut gerekli değildir.

 Parametre belirtilmezse veya **ayırma** parametresi belirtildiğinde, yalnızca .NET Framework bellek ayırma verileri toplanır. Varsa **ömrü** parametresi belirtildiğinde, hem .NET Framework bellek ayırma hem de .NET Framework nesne yaşam verisi toplanır.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Launch:AppName /GC[:{Allocation|Lifetime}] [Options]
```

#### <a name="parameters"></a>Parametreler
 **Ayırma** varsayılan. .NET Framework bellek ayırma verileri toplar.

 **Yaşam süresi** hem .NET Framework bellek ayırma verisini hem de .NET Framework nesne yaşam süresi verisi toplar.

## <a name="required-options"></a>Gerekli seçenekleri
 **GC** seçeneği yalnızca kullanılabilir ile **başlatma** seçeneği.

 **Başlat:** `AppName` Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.

## <a name="example"></a>Örnek
 Aşağıdaki örnek, bir uygulama başlatır ve .NET Framework bellek ayırma verileri toplar.

```cmd
VSPerfCmd.exe /Launch:TestApp.exe /gc
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)