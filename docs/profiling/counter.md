---
title: Sayaç | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: aa4b4cdb-e6ea-433a-9579-56f3785e1385
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e21e364d05641089fb7400fbbfa9873510037d62
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56596235"
---
# <a name="counter"></a>Sayaç
**Sayacı** seçeneği işlemci (Donanım) performans sayaçlarından veri toplar.

- Örnekleme profili oluşturma yöntemi, kullanırken **sayacı** yonga üzerinde performans sayacı ve örnekleme aralığı kullanılacak sayacı olay sayısını belirtir. Örnekleme kullanırken, yalnızca bir sayaç belirtebilirsiniz.

- Yöntemi profil oluşturma Araçları'nı kullanırken, geçerli ve önceki toplama olayları arasındaki aralık içinde oluşan sayacı olay sayısı profil oluşturucusu raporu ayrı alanlar olarak listelenir. Birden çok **sayacı** seçenekleri araçları kullanırken belirtilebilir.

  Her işlemci türü kendi donanım performans sayaç kümesi vardır. Profil Oluşturucu, neredeyse tüm işlemciler için ortak olan genel performans sayaçları kümesini tanımlar. Genel ve işlemciye özgü sayaçları bilgisayarınızda listelemek için VSPerfCmd kullanın **QueryCounters** komutu.

## <a name="syntax"></a>Sözdizimi

```cmd
VSPerfCmd.exe {/Launch:AppName | /Attach PID} /Counter:Name[,Reload[,FriendlyName]][Options]
```

```cmd
VSPerfCmd.exe /Start:Method /Counter:Name[,Reload[,FriendlyName]][/Counter:Name[,Reload[,FriendlyName]]][Options]
```

#### <a name="parameters"></a>Parametreler
 `Name` Sayaç adı. VSPerfCmd.exe kullanın **/querycounters** bilgisayardaki kullanılabilir sayaçların adlarını listelemek için seçeneği.

 `Reload` Örnekleme aralığı içinde sayacı olay sayısı. Cihaz atama yöntemi ile kullanmayın.

 `FriendlyName` (İsteğe bağlı) Yerine kullanılacak dize `Name` profil oluşturucu raporları ve görünümleri sütun başlıklarına.

## <a name="required-options"></a>Gerekli seçenekleri
 Sayaç seçeneği, yalnızca aşağıdaki seçeneklerden biriyle kullanılabilir:

 **Başlat:** `Trace` Şüpheli işlem yöntemini kullanan profil oluşturucuyu başlatır.

 **Başlat:** `AppName` Belirtilen uygulama ve profil oluşturucuyu başlatır. Profil Oluşturucu örnekleme yöntemini kullanmak için başlatılması gerekir.

 **Ekleme:** `PID` Profil oluşturucuyu başlatır ve işlem kimliği tarafından belirtilen işlem ekler Profil Oluşturucu örnekleme yöntemini kullanmak için başlatılması gerekir.

## <a name="example"></a>Örnek
 Örnekleme yöntemi örneği her 1000 yineleme uygulama NonHaltedCycles genel profil oluşturucu sayacın örnek gösterilmektedir.

 İzleme metodu örnek L2InstructionFetches sayacı olaylarını toplamak için profil oluşturucuyu başlatmak nasıl gösterir. İşlemci L2InstructionFetches sayaç adı özeldir.

```cmd
; Sample Method Example
VSPerfCmd.exe /Start:Sample /Output:TestApp.exe.vsp
VSPerfCmd.exe /Launch:TestApp.exe /Counter:NonHaltedCycles,1000,"Non-Halted Cycles"

;INSTRUMENTATION METHOD EXAMPLE
VSPerfCmd.exe /Start:Trace /Output:TestApp.exe.vsp /Counter:L2InstructionFetches,,"L2 Cache Instruction Fetches"
```

## <a name="see-also"></a>Ayrıca bkz.
- [VSPerfCmd](../profiling/vsperfcmd.md)
- [Bağımsız uygulamalar profili](../profiling/command-line-profiling-of-stand-alone-applications.md)
- [Profil ASP.NET web uygulamaları](../profiling/command-line-profiling-of-aspnet-web-applications.md)
- [Profil hizmetler](../profiling/command-line-profiling-of-services.md)