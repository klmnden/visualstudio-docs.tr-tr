---
title: EventSource olaylarını işaretleyici olarak Görselleştirme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 3a10022a-5c37-48b1-a833-dd35902176b6
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: bd6339b3f55b4a4c9a1e2c90ff3183a36f16c178
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63422088"
---
# <a name="visualize-eventsource-events-as-markers"></a>EventSource olaylarını işaretleyici olarak Görselleştirme
Eşzamanlılık görselleştiricisi EventSource olaylarını işaretleyici olarak görüntüleyebilir ve işaretçileri nasıl görüntüleneceğini denetleyebilirsiniz. EventSource işaretlerinin görüntülemek için kullanarak ETW sağlayıcısı GUID kaydetme [Gelişmiş ayarlar](../profiling/advanced-settings-dialog-box-concurrency-visualizer.md) iletişim kutusu. EventSource olaylarını olarak göstermek için varsayılan kuralları eşzamanlılık görselleştiricisi sahip [bayrak işaretleyicileri](../profiling/flag-markers.md), [yayılma işaretçileri](../profiling/span-markers.md), ve [ileti işaretçileri](../profiling/message-markers.md). EventSource olaylarını olaylara özel alanlar ekleyerek nasıl görüntüleneceğini özelleştirebilirsiniz. İşaretçiler hakkında daha fazla bilgi için bkz: [eşzamanlılık görselleştiricisi işaretleyicileri](../profiling/concurrency-visualizer-markers.md). EventSource olaylarını hakkında daha fazla bilgi için bkz: <xref:System.Diagnostics.Tracing>.

## <a name="default-visualization-of-eventsource-events"></a>EventSource olaylarını varsayılan Görselleştirme
 Varsayılan olarak, Concurrency Visualizer EventSource olaylarını göstermek için aşağıdaki kuralları kullanır.

### <a name="marker-type"></a>İşaret türü

1. Sahip olayları [Opcode](/windows/desktop/WES/eventmanifestschema-opcodetype-complextype) kazanma: Başlangıç ya da kazanın: Stop kabul edilir başına veya sonuna bir aralık sırasıyla.  İç içe geçmiş veya yayılma çakışan görüntülenemiyor. Bir iş parçacığı üzerinde başlayan ve başka birinde son olay çifti görüntülenemiyor.

2. Sürece, Opcode kazanma: Başlangıç ne kazanma: Stop bir olay işaretçisi bayrak olarak kabul edilir, [düzeyi](/windows/desktop/WES/defining-severity-levels) (EVENT_RECORD alanı. EVENT_HEADER. EVENT_DESCRIPTOR) olan kazanma: ayrıntılı veya üzeri.

3. Diğer durumlarda, olay iletisi olarak kabul edilir.

### <a name="importance"></a>Önem derecesi
 Aşağıdaki tabloda, olay düzeyi işaret önemini nasıl eşlendiğini tanımlar.

|ETW Level|Eşzamanlılık görselleştiricisi önem derecesi|
|---------------|---------------------------------------|
|Kazanma: LogAlways|Normal|
|Kazanma: kritik|Kritik|
|Kazanma: hata|Kritik|
|Kazanma: uyarı|Yüksek|
|Kazanma: bilgilendirme|Normal|
|Kazanma: ayrıntılı|Düşük|
|Win büyüktür: ayrıntılı|Düşük|

### <a name="series-name"></a>Seri adı
 Olayın görev adı için seri adı kullanılır. Seri adı, hiçbir görev olayı için tanımlanmışsa boştur.

### <a name="category"></a>Kategori
 Düzeyi win ise: kritik veya kazanma: hata, sonra da kategoriyi uyarı (-1). Aksi takdirde, varsayılan değer (0) kategorisidir.

### <a name="text"></a>Metin
 Printf türü biçimlendirilmiş metin iletisi için olay tanımlanmışsa, işaret açıklamasını görüntülenir. Aksi takdirde, olayın adı ve her yükü alanın değerini açıklamasıdır.

## <a name="customize-visualization-of-eventsource-events"></a>EventSource olaylarını görselleştirmesini özelleştirme
 EventSource olaylarını olayı için uygun alanlar ekleyerek aşağıdaki bölümlerde açıklandığı gibi gösterilme biçimini özelleştirebilirsiniz.

### <a name="marker-type"></a>İşaret türü
 Kullanım `cvType` alan, olay temsil etmek için kullanılan işaret türünü denetlemek için bir bayt. CvType için kullanılabilen değerler şunlardır:

|cvType değeri|Sonuçta elde edilen işaret türü|
|------------------|---------------------------|
|0|İleti|
|1.|Aralık başlangıcı|
|2|Aralık sonu|
|3|Bayrağı|
|Diğer tüm değerler|İleti|

### <a name="importance"></a>Önem derecesi
 Kullanabileceğiniz `cvImportance` alan, bir EventSource olay önem derecesi ayarı denetlemek için bir bayt. Ancak, alt düzey kullanarak bir olay görüntülenen önemini denetim öneririz.

|cvImportance değeri|Eşzamanlılık görselleştiricisi önem derecesi|
|------------------------|---------------------------------------|
|0|Normal|
|1.|Kritik|
|2|Yüksek|
|3|Yüksek|
|4|Normal|
|5|Düşük|
|Diğer tüm değerler|Düşük|

### <a name="series-name"></a>Seri adı
 Kullanım `cvSeries` olay alanı, Concurrency Visualizer EventSource olaya sağlar. seri adı denetlemek için bir dize.

### <a name="category"></a>Kategori
 Kullanım `cvCategory` EventSource olaya eşzamanlılık görselleştiricisi veren kategori denetlemek için bir bayt alan.

### <a name="text"></a>Metin
 Kullanım `cvTextW` alan, Concurrency Visualizer EventSource olaya veren bir açıklama denetlemek için bir dize.

### <a name="spanid"></a>SpanID
 Olay çifti ile eşleşen için bir int cvSpanId alanını kullanın. Her bir çifti Başlat/Durdur olayların bir aralığı temsil eden değeri benzersiz olmalıdır. Genellikle eş zamanlı kod için bu eşitleme temellerine gibi gerektirir <xref:System.Threading.Interlocked.Exchange%2A> (CvSpanID için kullanılan değer) anahtarının doğru olduğundan emin olmak için.

> [!NOTE]
> Kısmen aynı iş parçacığında üst üste veya bir iş parçacığında başlatmaya izin vermek için yayılma içine yerleştirmek için SpanID kullanılmasına izin verin ve diğer uçta desteklenmiyor.

## <a name="see-also"></a>Ayrıca bkz.
- [Eşzamanlılık görselleştiricisi işaretleyicileri](../profiling/concurrency-visualizer-markers.md)