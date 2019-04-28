---
title: .NET bellek verisi görünümleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- .NET memory profiling method views
- profiling tools,.NET memory profiling views
ms.assetid: 79184d8e-769b-4ace-be2b-521147772081
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b1a866ba73669caba0c8d96647a134123f4ae753
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62970050"
---
# <a name="net-memory-data-views"></a>.NET bellek verisi görünümleri
Bu bölüm .NET bellek profil oluşturma verileri içeren görünümleri ve raporları Profil Oluşturucu veri dosyalarının yönelik başvuru bilgileri içerir.

## <a name="in-this-section"></a>Bu bölümde
- [Özet Görünümü](../profiling/summary-view-dotnet-memory-data.md)

 En çok bellek ayrılan türleri ve işlevleri listeler.

- [Ayırmalar Görünümü](../profiling/dotnet-memory-allocations-view.md)

 Profil oluşturma çalıştırmasını ve türü tahsiste sonuçlanan çağrı ağaçları (yürütme yolları) tahsis türlerini listeler.

- [Nesne Ömrü Görünümü](../profiling/object-lifetime-view.md)

 Profil oluşturma çalıştırmasını ve örnekleri, bayt cinsinden boyutu ve türü çöp toplama nesil sayısını ayrılan türlerini listeler.

- [Çağrı Ağacı Görünümü - Örnekleme](../profiling/call-tree-view-dotnet-memory-sampling-data.md)

 Bellek ayırma verisini işlevleri çalıştırmak profil oluşturma ve yürütme yollarını temsil eden bir hiyerarşik ağaç görüntüler.

- [Modüller Görünümü- Örnekleme](../profiling/modules-view-dotnet-memory-sampling-data.md)

 .NET bellek ayırma verisini modülü tarafından düzenler ve İşlevler, kaynak kod satırlarına ve ayrılan bellek yürütme yönergeleri listeler.

- [Arayan/Aranan görünümü - .NET bellek örnekleme verileri](../profiling/caller-callee-view-dotnet-memory-sampling-data.md)

 Seçili işleve, seçili işlev çağıran işlevler ve seçili işlev tarafından çağrılan işlevler için bellek ayırma verisini listeler.

- [İşlevler Görünümü- Örnekleme](../profiling/functions-view-dotnet-memory-sampling-data.md)

 Profil oluşturma çalıştırmasını işlevler için bellek ayırma verisini listeler.

- [Satırlar Görünümü- Örnekleme](../profiling/lines-view-dotnet-memory-sampling-data.md)

 Kaynak kod satırlarına işlevlerin profil oluşturma çalışması için bellek ayırma verisini listeler.

- [Yönerge İşaretçileri (IP) Görünümü- Örnekleme](../profiling/instruction-pointers-ips-view-dotnet-memory-sampling-data.md)

 Profil oluşturma çalıştırmasını işlevlerin yönergeleri için bellek ayırma verisini listeler.

- [Çağrı Ağacı Görünümü - İzleme](../profiling/call-tree-view-dotnet-memory-instrumentation-data.md)

 Yürütme yollarını, bellek ayırma verileri ve profil oluşturma çalışması olarak işaretlenmiş işlevler için ayrıntılı zamanlama verileri temsil eden bir hiyerarşik ağaç görüntüler.

- [Modüller Görünümü - İzleme](../profiling/modules-view-dotnet-memory-instrumentation-data.md)

 Modülü tarafından profil oluşturma verileri düzenler ve İşlevler, bellek ayırma verilerinin ve modülü için ayrıntılı zamanlama bilgisi listeler.

- [Arayan/Aranan görünümü - .NET bellek izleme verileri](../profiling/caller-callee-view-net-memory-instrumentation-data.md)

 Bellek ayırma verileri ve seçili izleme eklenmiş bir işleve, seçili işlev çağıran işlevler ve seçili işlev tarafından çağrılan işlevler için ayrıntılı zamanlama bilgilerini listeler.

- [İşlevler Görünümü - İzleme](../profiling/functions-view-dotnet-memory-instrumentation-data.md)

 İzleme eklenmiş profil oluşturma çalıştırmasını işlevler için bellek ayırma verisini listeler.

## <a name="reference"></a>Başvuru
- [İşlev Ayrıntıları Görünümü](../profiling/function-details-view.md)

 Seçili işleve çağrılır ve seçili işlev tarafından çağrılmış işlevler arasındaki ilişkinin bir grafik görüntüler.

- [İşlem Görünümü](../profiling/process-view.md)

 Listeleri işlem ve iş parçacığı başlangıç ve bitiş zamanlarını.

- [İşaretler Görünümü](../profiling/marks-view.md)

 ETW ve örnekleme bir profil oluşturma veri dosyası içine eklenen olaylarını listeler.

## <a name="related-sections"></a>İlgili bölümler
- [Örnekleme Yöntemi Veri Görünümleri](../profiling/profiler-sampling-method-data-views.md)

 Görünümleri ve raporları örnekleme metodu kullanılarak üretilen Profil Oluşturucu veri dosyaları için başvuru bilgileri.

- [İzleme Metodu Veri Görünümleri](../profiling/instrumentation-method-data-views.md)

 Görünümleri ve raporları araç haline getirme yöntemi kullanılarak üretilen Profil Oluşturucu veri dosyalarının için başvuru bilgileri.