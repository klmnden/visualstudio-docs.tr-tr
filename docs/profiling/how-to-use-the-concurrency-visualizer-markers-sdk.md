---
title: "Nasıl yapılır: Eşzamanlılık görselleştiricisi işaretçileri SDK'sını kullanma | Microsoft Docs"
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 19a45032-f8a7-4137-890e-2ceeec938b8d
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fe76cc490523325c8334ad7ada3273f101e0bbc9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56626134"
---
# <a name="how-to-use-the-concurrency-visualizer-markers-sdk"></a>Nasıl yapılır: Eşzamanlılık görselleştiricisi işaretçileri SDK'yı kullanın
Bu konu, eşzamanlılık görselleştiricisi SDK'si yayılma oluşturup bayrakları, iletileri ve Uyarılar için nasıl kullanılacağını gösterir.

### <a name="to-use-c"></a>C++ kullanmak için

1.  Eşzamanlılık görselleştiricisi SDK desteği uygulamanıza ekleyin. Daha fazla bilgi için [eşzamanlılık görselleştiricisi SDK'si](../profiling/concurrency-visualizer-sdk.md).

2.  Ekleme bir `include` deyimi ve `using` SDK bildirimi.

    ```C++

    #include <cvmarkersobj.h>
    using namespace Concurrency::diagnostic;

    ```

3.  Varsayılan işaret dizide üç yayılma oluşturup yazma bayrağı, bir ileti ve bir uyarı, her aralık için kod ekleyin. Bayrakları, iletileri ve uyarılar yazma yöntemleri üyeleri [marker_series](../profiling/marker-series-class.md) sınıfı. Oluşturucusu [span](../profiling/span-class.md) sınıfı gerektirir bir `marker_series` nesne her aralık belirli işaret seri ilişkili olmasını sağlayın. A `span` silindiğinde sona erer.

    ```C++

    marker_series series;
    span *flagSpan = new span(series, 1, _T("flag span"));
    series.write_flag(_T("Here is the flag."));
    delete flagSpan;

    span *messageSpan = new span(series, 2, _T("message span"));
    series.write_flag(_T("Here is the message."));
    delete messageSpan;

    span *alertSpan = new span(series, 3, _T("alert span"));
    series.write_flag(_T("Here is the alert."));
    delete alertSpan;

    ```

4.  Menü çubuğunda, **Çözümle**, **eşzamanlılık görselleştiricisi**, **Geçerli projeyle Başlat** uygulamayı çalıştırın ve eşzamanlılık görselleştiricisi görüntülemek için. Aşağıdaki çizim üç yayılımları ve üç işaretçileri eşzamanlılık görselleştiricisi içinde gösterir.

     ![Eşzamanlılık görselleştiricisi işaretçileri ve uyarılarla 3](../profiling/media/cvmarkersnative.png "CvMarkersNative")

5.  Ek, özel işaretçisi serisi için oluşturucu çağırarak oluşturmak için kod ekleyin `marker_series` , işaret serisi için bir dize adını alır.

    ```C++

    marker_series flagSeries(_T("flag series"));
    span *flagSeriesSpan = new span(flagSeries, 1, _T("flag span"));
    flagSeries.write_flag(1, _T("flag"));
    // Sleep to even out the display in the Concurrency Visualizer.
    Sleep(50);
    delete flagSeriesSpan;

    marker_series messageSeries(_T("message series"));
    span *messageSeriesSpan = new span(messageSeries, 1, _T("message span"));
    messageSeries.write_message(1, _T("message"));
    // Sleep to even out the display in the Concurrency Visualizer.
    Sleep(50);
    delete messageSeriesSpan;

    ```

6.  Eşzamanlılık görselleştiricisi görüntülemek için geçerli bir proje başlatın. İki işaret serisi kendi kulvarları iş parçacıkları görünümünde görünür. Aşağıdaki çizimde, iki yeni yayılma gösterir.

     ![Eşzamanlılık görselleştiricisi 3 özel işaret serisi ile](../profiling/media/cvmarkerseriesnative.png "CvMarkerSeriesNative")

### <a name="to-use-visual-basic-or-c"></a>Visual Basic veya C# ' ı kullanmak için #

1.  Eşzamanlılık görselleştiricisi SDK desteği uygulamanıza ekleyin. Daha fazla bilgi için [eşzamanlılık görselleştiricisi SDK'si](../profiling/concurrency-visualizer-sdk.md).

2.  Ekleme bir `using` veya `Imports` SDK bildirimi.

    ```VB
    Imports Microsoft.ConcurrencyVisualizer.Instrumentation

    ```

    ```csharp
    using Microsoft.ConcurrencyVisualizer.Instrumentation;
    ```

3.  Varsayılan işaret serisinin üç yayılma oluşturup yazma bayrağı, bir ileti ve bir uyarı, her aralık için kod ekleyin. Oluşturduğunuz bir <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.Span> statik çağırarak `EnterSpan` yöntemi. Varsayılan serinin yazmak için statik yazma yöntemlerini kullanın. <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.Markers> sınıfı.

    ```VB

    Dim flagSpan As Span = Markers.EnterSpan("flag span")
    Markers.WriteFlag("Here is the flag.")
    flagSpan.Leave()

    Dim messageSpan As Span = Markers.EnterSpan("message span")
    ' Sleep for a millisecond to even out the display in the Concurrency Visualizer.
    System.Threading.Thread.Sleep(1)
    Markers.WriteMessage("Here is a message")
    messageSpan.Leave()

    Dim alertSpan As Span = Markers.EnterSpan("alert span")
    ' Sleep for a millisecond to even out the display in the Concurrency Visualizer.
    System.Threading.Thread.Sleep(1)
    Markers.WriteAlert("Here is an alert")
    alertSpan.Leave()

    ```

    ```csharp

    Span flagSpan = Markers.EnterSpan("flag span");
    Markers.WriteFlag("Here is the flag.");
    flagSpan.Leave();

    Span messageSpan = Markers.EnterSpan("message span");
    // Sleep for a millisecond to even out the display in the Concurrency Visualizer.
    System.Threading.Thread.Sleep(1);
    Markers.WriteMessage("Here is a message");
    messageSpan.Leave();

    Span alertSpan = Markers.EnterSpan("alert span");
    // Sleep for a millisecond to even out the display in the Concurrency Visualizer.
    System.Threading.Thread.Sleep(1);
    Markers.WriteAlert("Here is an alert");
    alertSpan.Leave();
    ```

4.  Menü çubuğunda, **Çözümle**, **eşzamanlılık görselleştiricisi**, **Geçerli projeyle Başlat** uygulamayı çalıştırın ve eşzamanlılık görselleştiricisi görüntülemek için. Aşağıdaki çizim üç yayılımları ve üç işaretçileri eşzamanlılık görselleştiricisi iş parçacıkları Görünümü'nde gösterir.

     ![Eşzamanlılık görselleştiricisi işaretçileri ve uyarılarla](../profiling/media/cvmarkersmanaged.png "CvMarkersManaged")

5.  Statik kullanarak müşteri işaret serisi oluşturmak için kod ekleyin <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.Markers.CreateMarkerSeries%2A> yöntemi. <xref:Microsoft.ConcurrencyVisualizer.Instrumentation.MarkerSeries> Sınıfı yayılma oluşturma ve bayrakları, iletileri ve uyarılar yazma yöntemleri içerir.

    ```VB

    Dim flagSeries As MarkerSeries = Markers.DefaultWriter.CreateMarkerSeries("flag series")
    Dim flagSeriesSpan As Span = flagSeries.EnterSpan("flag span")
    System.Threading.Thread.Sleep(1)
    flagSeries.WriteFlag(1, "flag")
    System.Threading.Thread.Sleep(1)
    flagSeriesSpan.Leave()

    Dim messageSeries As MarkerSeries = Markers.DefaultWriter.CreateMarkerSeries("message series")
    Dim messageSeriesSpan As Span = messageSeries.EnterSpan("message span")
    messageSeries.WriteMessage("message")
    System.Threading.Thread.Sleep(1)
    messageSeriesSpan.Leave()
    ```

    ```csharp

    MarkerSeries flagSeries = Markers.DefaultWriter.CreateMarkerSeries("flag series");
    Span flagSeriesSpan = flagSeries.EnterSpan("flag span");
    System.Threading.Thread.Sleep(1);
    flagSeries.WriteFlag(1, "flag");
    System.Threading.Thread.Sleep(1);
    flagSeriesSpan.Leave();

    MarkerSeries messageSeries = Markers.DefaultWriter.CreateMarkerSeries("message series");
    Span messageSeriesSpan = messageSeries.EnterSpan("message span");
    messageSeries.WriteMessage("message");
    System.Threading.Thread.Sleep(1);
    messageSeriesSpan.Leave();
    ```

6.  Eşzamanlılık görselleştiricisi görüntülemek için geçerli bir proje başlatın. Üç işaret serisi kendi kulvarları iş parçacıkları görünümünde görünür. Aşağıdaki çizim üç yeni yayılma gösterir.

     ![Eşzamanlılık görselleştiricisi 3 özel işaret serisi ile](../profiling/media/cvmarkerseriesmanaged.png "CvMarkerSeriesManaged")

## <a name="see-also"></a>Ayrıca bkz.
- [Eşzamanlılık Görselleştiricisi SDK](../profiling/concurrency-visualizer-sdk.md)
