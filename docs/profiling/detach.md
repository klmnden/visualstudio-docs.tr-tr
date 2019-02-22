---
title: Ayırma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: d9d1b52c-7f28-467d-b1e0-512afc4e46c9
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c65f17d9c37cf885460be8a2c9c3560d12f64dd5
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56630346"
---
# <a name="detach"></a>Ayır
VSPerfCmd.exe **ayırma** seçeneği keser profil oluşturucu belirtilen işlemleri veya tüm işlemlerden hiçbiri belirtilmezse. Profil oluşturma için örnekleme yöntemini kullanarak başlatılmış olması gerekir.

 Profil oluşturma başlatıldı ile **başlatma** veya **iliştirme** seçenekleri bağlantısı ile **ayırma**. Profil Oluşturucu sonraki kullanarak reattched olabilir **iliştirme** komutları.

 **Ayırma** profil oluşturma veri dosyasını kapatmak değil. Kullanım **kapatma** son profil oluşturma ve veri dosyasını kapatırsınız.

> [!NOTE]
>  Varsa **Başlat** seçeneği ile belirtilen **Crosssession** seçeneğini çağrıları **VSPerfCmd /Attach** veya **VSPerfCmd/detach** gerekir Ayrıca belirtin **Crosssession**.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Detach[:PIDs|ProcessNames]
```

#### <a name="parameters"></a>Parametreler
 `PIDs|ProcessNames` `PID` -Bir veya daha fazla işlem sayısal sistem tanımlayıcısını.

 `ProcessNames` -işlem adı. Adlandırılmış işlemi birden çok örneğini çalıştırıyorsanız, sonuçlar tahmin edilemez.

 Birden çok işlem virgülle ayırın.

 Hiçbir işlem belirtilmezse, profil oluşturucu tüm profili oluşturulan işlemden ayrılır.

## <a name="valid-options"></a>Geçerli seçenekler şunlardır:
 Aşağıdaki **VSPerfCmd** seçenekleri ile birleştirilebilir **iliştirme** tek bir komut satırı seçeneği.

 **Crosssession** oturumlarında oturum dışındaki uygulamaların profilini oluşturma etkinleştirir. Gerekli if **Başlat** seçeneği ile belirtilen **Crosssession** seçeneği.

## <a name="example"></a>Örnek
 Bu örnekte, **ayırma** komutu, profil oluşturma askıya alır ve **kapatma** komutu, Profil Oluşturucu veri dosyasına kapatır.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe
;REM Excercise the application
VSPerfCmd.exe /Detach
VSPerfCmd.exe /Shutdown
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)