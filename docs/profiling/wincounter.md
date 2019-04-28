---
title: WinCounter | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ff319ffc-f249-4c3f-9eb2-06e392e3ae80
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8e93cc526ad61916e2a8663caa9652842ce136c5
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62960200"
---
# <a name="wincounter"></a>WinCounter
**WinCounter** seçeneği, farklı çalıştır profilinin sırasında belirlenen aralıklarla toplamak için bir Windows ya da uygulama performans sayacı belirtir. Windows ve uygulama performans sayaçları, profil oluşturma veri dosyasını işaretleri olarak listelenir. Ayrı seçeneklerinde toplamak için birden çok performans sayaçları belirtebilirsiniz.

 Sayaçlar varsayılan olarak, toplanan her 500 milisaniye. Kullanım **AutoMark** seçeneği farklı bir koleksiyon aralığı belirtin.

 Yalnızca bir **AutoMark** seçeneği kullanılır. Birden çok **AutoMark** seçenekler belirtilir, sonuncu kullanılır.

 **WinCounter** seçeneği yalnızca kullanılabilir ile **Başlat** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Start:Method /Wincounter:Path [/WinCounter:Path] [AutoMark:Milliseconds] [Options]
```

#### <a name="parameters"></a>Parametreler
 `Path` Windows performans sayacı PDH sayacı yol biçiminde.

## <a name="required-options"></a>Gerekli seçenekleri
 **WinCounter** seçeneği yalnızca kullanılabilir ile **Başlat** seçeneği.

 **Başlat:** `Method` **Başlat** seçeneği belirtilen profil oluşturma metodu için profil oluşturucuyu başlatır.

## <a name="exclusive-options"></a>Dışlayan seçenekleri
 **AutoMark** seçeneği yalnızca kullanılabilir ile **WinCounter** seçeneği.

 **AutoMark:** `Milliseconds` Windows performans sayacı verilerini toplama arasındaki milisaniye sayısını belirtir.

## <a name="example"></a>Örnek
 Aşağıdaki örnekte, 1000 milisaniye cinsinden zaman aralığı sırasında Tahsil edilecek Windows performans sayaçları iki belirtilir.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp /WinCounter:"\Processor(0)\% Processor Time" /WinCounter:"\System\Context Switches/sec" /AutoMark:1000
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)