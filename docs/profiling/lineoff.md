---
title: Lıneoff | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 76082063-20ef-47ae-ad64-81b43b654865
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b4de8aa278adab0127f3a39d9adcf105f906e152
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62995338"
---
# <a name="lineoff"></a>LineOff
Örnekleme profili oluşturma yöntemi kullanırken, varsayılan olarak, profil oluşturucu kaynak kodu satır numarasını ve satır numarası uzaklık veri toplar. VSPerfCmd **Lıneoff** seçeneği devre dışı bırakır satır numarası veri koleksiyonunu VSPerfCmd uygulamayı başlatmak için kullanıldığında. Profil oluşturma verilerinin işleve toplandığı zaman düzey **Lıneoff** belirtilir.

 Kullanabileceğiniz **Lıneoff** yalnızca **başlatma** seçeneği, ve yalnızca zaman profil oluşturucu örnekleme için kullanarak başlatıldı **Başlat**:**örnek** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Launch:AppName /LineOff [Options]
```

#### <a name="parameters"></a>Parametreler
 Yok.

## <a name="required-options"></a>Gerekli seçenekleri
 **Lıneoff** seçeneği yalnızca içeren bir komut satırında kullanılabilir **başlatma** seçeneği.

 **Başlat:** `AppName` Belirtilen uygulamayı başlatır ve örnekleme yöntemiyle profili oluşturma başlar.

## <a name="example"></a>Örnek
 Bu örnek, uygulama ve profil oluşturucuyu başlatır ve satır düzeyi örnekleme devre dışı bırakır.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /LineOff
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)