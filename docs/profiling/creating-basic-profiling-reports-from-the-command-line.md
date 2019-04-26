---
title: Basic raporları komut satırından profil oluşturma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 6d73e21e-c04e-48ea-91cc-e517a5f2cd3f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6ac35f506aadfcceebcbcf0dd4f6ec5b6dc33107
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62552869"
---
# <a name="create-basic-profiling-reports-from-the-command-line"></a>Komut satırından temel profil oluşturma raporları oluşturma
Bu makalede, virgülle ayrılmış değer oluşturan temel VSPerfReport komutlarını (. *CSV*) raporlarına bir. *vsp* veya. *vsps* profil oluşturma veri dosyası. Tüm rapor seçeneklerinin bir açıklaması için bkz: [VSPerfReport](../profiling/vsperfreport.md).

## <a name="report-commands"></a>Rapor komutları
 Belirtilen bir profil oluşturma veri dosyası için bir rapor oluşturmak için aşağıdaki komutlardan birini kullanın.

 **VSPerfReport** `VSPFile` **userrulesdirectory** için kullanılabilir tüm raporlar üretir. *Vsp* veya. *vsps* dosya.

 **VSPerfReport** `VSPFile` **/Summary:**`ReportType`[,`ReportType`...] Belirtilen rapor türlerini oluşturur.

 **VSPerfReport** `VSPFile` **/calltrace** her veri toplama olayını listeleyen bir rapor oluşturur. Yalnızca Araçlar.

## <a name="summary-report-type-parameters"></a>Rapor tür parametreleri özeti
 Aşağıdaki tabloda, belirtilen rapor türü seçeneği tarafından oluşturulan raporları açıklar. Raporun sütunları veri toplamak için kullanılan profil oluşturma yöntemine bağlıdır.

|Parametre özeti|Rapor açıklaması|Rapor başvurusu|
|-----------------------|------------------------|----------------------|
|**CallerCallee**|İşlevler arası üst/alt ilişkilerini temsil eder.|-   [Örnekleme verileri](../profiling/caller-callee-view-sampling-data.md)<br />-   [Ölçümlü izleme verileri](../profiling/caller-callee-view-instrumentation-data.md)<br />-   [.NET bellek örnekleme verileri](../profiling/caller-callee-view-dotnet-memory-sampling-data.md)<br />-   [.NET bellek izleme verileri](../profiling/caller-callee-view-net-memory-instrumentation-data.md)<br />-   [Çakışma verileri](../profiling/caller-callee-view-contention-data.md)|
|**İşlevi**|Profilleme verisini fonksiyon olarak listeler.|-   [Örnekleme verileri](../profiling/functions-view-sampling-data.md)<br />-   [Ölçümlü izleme verileri](../profiling/functions-view-instrumentation-data.md)<br />-   [.NET bellek örnekleme verileri](../profiling/functions-view-dotnet-memory-sampling-data.md)<br />-   [.NET bellek izleme verileri](../profiling/functions-view-dotnet-memory-instrumentation-data.md)<br />-   [Çakışma verileri](../profiling/functions-view-contention-data.md)|
|**CallTree**|Profil oluşturma çalıştırmasını işlevlerin profil oluşturma verilerini ve yürütme yollarını temsil eder.|-   [Ölçümlü izleme verileri](../profiling/call-tree-view-instrumentation-data.md)<br />-   [Örnekleme verileri](../profiling/call-tree-view-sampling-data.md)<br />-   [.NET bellek örnekleme verileri](../profiling/call-tree-view-dotnet-memory-sampling-data.md)<br />-   [.NET bellek izleme verileri](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)<br />-   [Çakışma verileri](../profiling/call-tree-view-contention-data.md)|
|**Counter**|Profil oluşturma işaretleri yanı sıra profil oluşturma çalışması sırasında toplanan Windows performans sayacı değerlerini listeler.|-   [İşaretler görünümü](../profiling/marks-view.md)|
|**IP**|Yönerge tarafından profil oluşturma verilerini listeler.|-   [Örnekleme verileri](../profiling/instruction-pointers-ips-view-sampling-data.md)<br />-   [.NET bellek örnekleme verileri](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)<br />-   [Çakışma verileri](../profiling/instruction-pointers-ips-view-contention-data.md)|
|**Ömür**|Ayrılmış nesnelerin ömrünü listeler.|-   [Nesne ömrü görünümü](../profiling/object-lifetime-view.md)|
|**Satır**|Kaynak kod satırı tarafından profil oluşturma verilerini listeler.|-   [Örnekleme verileri](../profiling/lines-view-sampling-data.md)<br />-   [.NET bellek örnekleme verileri](../profiling/lines-view-dotnet-memory-sampling-data.md)<br />-   [Çakışma verileri](../profiling/lines-view-contention-data.md)|
|**Üst bilgi**|Profil oluşturma veri dosyasının başlık bilgileri.|Belirli dosya için.|
|**Mark**|Profil oluşturma işaretleri profil oluşturma çalıştırmasını toplanmadı.|-   [İşaretler görünümü](../profiling/marks-view.md)|
|**Module**|Modüller için profil oluşturma verilerini listeler.|-   [Örnekleme verileri](../profiling/modules-view-sampling-data.md)<br />-   [Ölçümlü izleme verileri](../profiling/modules-view-instrumentation-data.md)<br />-   [.NET bellek örnekleme verileri](../profiling/modules-view-dotnet-memory-sampling-data.md)<br />-   [.NET bellek izleme verileri](../profiling/modules-view-dotnet-memory-instrumentation-data.md)<br />-   [Çakışma verileri](../profiling/modules-view-contention-data.md)|
|**İşlem**|İşlemler için profil oluşturma verilerini listeler.|-   [İşlem görünümü](../profiling/process-view.md)<br />-   [Çakışma verileri](../profiling/process-view-contention-data.md)|
|**iş parçacığı**|İş parçacıkları için profil oluşturma verilerini listeler.|-   [İşlem görünümü](../profiling/process-view.md)|
|**Tür**|Ayırma profil oluşturma verileri türe göre listelenmektedir.|-   [Ayırma görünümü](../profiling/dotnet-memory-allocations-view.md)|
|**Çekişme**|Kaynak çakışmaları.|-   [Kaynak çakışmaları](../profiling/resource-contentions-view-contention-data.md)|
|**RuleWarnings**|Performans kural sorunlarını listeler.|-Checkıd, açıklama ve kural sorununun kaynak kod konumunu listeler.|
|**ETW**|Olay izleme için Windows (ETW) olayları, profil oluşturma çalışmasında toplanan.|-   [ETW raporu](../profiling/event-tracing-for-windows-etw-report.md)|