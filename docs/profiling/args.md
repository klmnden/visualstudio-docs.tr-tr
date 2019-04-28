---
title: Args | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 20c35949-1f29-4282-ac75-4e6c237d71bc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 036b13a7fea5d64e23e2b7d5ccbd8a7b17f91176
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62777056"
---
# <a name="args"></a>Bağımsız Değişkenler
VSPerfCmd.exe **Args** seçeneği belirtir hedef uygulamaya geçirilen bağımsız değişkenlerin bir listesi **başlatma** alt.

 **Args** yalnızca ne zaman kullanılabilir **başlatma** da komut satırı üzerinde belirtilmiş. **Args** isteğe bağlı olduğunda **başlatma** belirtilir.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Launch:AppName /Args:Arguments [Options]
```

#### <a name="parameters"></a>Parametreler
 `Arguments` Hedef uygulamayı bağımsız değişken listesi **başlatma** komutu.

## <a name="required-options"></a>Gerekli seçenekleri
 **Başlat:** `AppName` Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte **Args** TestApp.exe için bağımsız değişkenleri geçirmek için seçeneği.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /Args:"123, 'Hello World'"
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamaların profilini oluşturma](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [ASP.NET web uygulamalarının profilini oluşturma](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil oluşturma hizmetleri](../profiling/command-line-profiling-of-services.md)