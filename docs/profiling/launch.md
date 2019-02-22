---
title: Başlatma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: f81bde5c-3394-4b79-a315-c2f6491689b3
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c1d4c2c81583015aca39f00cc20a6286297476cc
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56625172"
---
# <a name="launch"></a>Başlat
**Başlatma** seçeneği profil oluşturucu örnekleme metodu kullanılarak başlatılır ve ayrıca belirtilen uygulamayı başlatır.

 Kullanılacak **başlatma** seçeneğini belirtmelisiniz **örnek** yönteminde **Başlat** seçeneği.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe /Launch:AppName [Options]
```

#### <a name="parameters"></a>Parametreler
 `AppName` Başlatmak için uygulamanın adı. Geçerli dizindeki tam ve kısmi yollar desteklenir.

## <a name="valid-options"></a>Geçerli seçenekler şunlardır:
 Aşağıdaki VSPerfCmd seçenekleri ile birleştirilebilir **başlatma** tek bir komut satırı seçeneği.

 **Başlat:** `Method` Komut satırı Profil Oluşturucu oturumu başlatır ve belirtilen profil oluşturma yöntemini ayarlar.

 **GlobalOn** ve **GlobalOff** sürdürür (**GlobalOn**) veya duraklatır (**GlobalOff**) profil oluşturma, ancak profil oluşturma oturumu sona ermez.

 **ProcessOn:** `PID` ve **ProcessOff**:`PID` Sürdürür (**ProcessOn**) veya duraklatır (**ProcessOff**) belirtilen işlem için profil oluşturma.

 **TargetCLR** profil oluşturma oturumu içinde birden fazla sürümü yüklendiğinde, .NET Framework ortak dil çalışma zamanı (CLR) profil sürümü belirtir. Varsayılan olarak, ilk yüklenen sürümü profil oluşturulan.

## <a name="exclusive-options"></a>Dışlayan seçenekleri
 Aşağıdaki seçenekler ile yalnızca kullanılabilir **başlatma** seçeneği.

 **Konsol** yeni bir pencerede belirtilen komut satırı uygulaması başlatır.

 **Bağımsız değişkenleri:** `ArgList` Uygulamaya devredilecek bağımsız değişkenler listesini belirtir.

 **Lıneoff** satır düzeyi profil oluşturma verilerinin toplanmasını devre dışı bırakır.

## <a name="sampling-options"></a>Örnekleme seçenekleri
 Örnekleme aralığı şunlardan biri belirtilebilir üzerinde **başlatma** komut satırı. Varsayılan örnekleme aralığı 10.000.000 işlemci saat döngülerini ' dir.

 **Zamanlayıcı**[**:**`Cycles`]**PF**[**:**`Events`]**Sys**[**:**`Events`] **Sayaç**[**:**`Name`,`Reload`,`FriendlyName`]**GC**[:**ayırma** &#124;  **yaşam süresi**] sayısı ve örnekleme aralığı türünü belirtir.

-   **Zamanlayıcı** -örnekleri her `Cycles` durdurulmamış işlemci saat döngüsü. Varsa `Cycles` belirtilmezse, 10.000.000 döngüleri kullanılır.

-   **PF** -örnekleri her `Events` sayfa hataları. Varsa `Events` belirtilmezse, 10 sayfa hataları.

-   **Sys** -örnekleri her `Events` işletim sistem çağrıları. Varsa `Events` belirtilmezse, 10 sistem çağrıları kullanılır.

-   **Sayaç** -örnekleri her `Reload` CPU performans sayaç tarafından belirtilen sayıda `Name`. İsteğe bağlı olarak, `FriendlyName` profil oluşturucusu raporu sütun başlığına olarak kullanılacak bir dize belirtebilirsiniz.

-   **GC** -toplar .NET bellek verileri. Varsayılan olarak (**ayırma**), her bir bellek ayırma etkinlikte toplanan veriler. Zaman **ömrü** parametresi belirtildiğinde, veriler ayrıca her çöp toplama olayını toplanır.

## <a name="example"></a>Örnek
 Bu örnek kullanımını gösterir **başlatma** bir uygulamayı başlatmak için.

```cmd
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)