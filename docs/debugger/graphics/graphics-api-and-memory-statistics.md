---
title: Grafik API'si ve bellek istatistikleri | Microsoft Docs
ms.date: 03/02/2017
ms.topic: conceptual
f1_keywords:
- vs.graphics.apistatistics
- vs.graphics.memorystatistics
ms.assetid: 27d2f303-e3ed-4219-9009-345a0d849506
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7810889d4af411477573c71aa694d797a90763f3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62896025"
---
# <a name="graphics-api-and-memory-statistics"></a>Grafik API'si ve bellek istatistikleri
<!-- VERSIONLESS -->
Visual Studio 2017 ve daha büyük destek grafik API istatistikleri ve bellek istatistikleri araçları.  Bu iki Araçlar GPU bellek tüketimi çeşitli kaynakların yanı sıra Direct3D API kullanımı hakkında bilgi çeşitli bitlerini görüntülemenize olanak sağlar.

## <a name="graphics-api-statistics"></a>Grafik API istatistikleri
Visual Studio grafik tanılama grafik API'si istatistiklerin tüm yapılan Direct3D çağrıları ve her çağrı sayısı görüntülemenize olanak tanır.  Penceresini görüntülemek için seçin **Görüntüle > API istatistikleri** menü öğesi.

![API istatistikleri](media/gfx_diag_api_statistics.png)

Bu araç DirectX çağrılarına, sizin fark ettiğinizden değil yapıyorsanız bulma veya çok sık yaptığınız çağrılar kullanışlı olabilir.

Penceresinde kopyalama tüm verileri ayrıntılı analiz için Excel gibi bir şeyi yapıştırılabilir CSV, olarak sağ tıklayabilirsiniz.

## <a name="memory-statistics"></a>Bellek istatistikleri
Bu araç, ne kadar bellek, grafik sürücüsü, kaynaklar için ayrılırken bir çerçeve içinde oluşturduğunuz görüntülenir.  Bu pencereyi görüntülemek için seçin **Görüntüle > bellek istatistikleri** menü öğesi.

![Bellek istatistikleri](media/gfx_diag_memory_statistics.png)

**GPU ayırma** sütun görüntülenen olay tarafından kullanılan bellek miktarını görüntüler **olay** sütun.  İzle simgesini de seçebilirsiniz ![izleme simgesi](media/gfx_watch.png) görüntülemek için [kaynak geçmişi](graphics-event-list.md#resource-history) seçili olay için.

API istatistikleri aracıyla olduğu gibi, penceresinde kopyalama tüm verileri ayrıntılı analiz için Excel gibi bir şeyi yapıştırılabilir CSV, olarak sağ tıklayabilirsiniz.

## <a name="see-also"></a>Ayrıca Bkz.
- [Grafik Tanılama (DirectX Grafiklerinde Hata Ayıklama)](visual-studio-graphics-diagnostics.md)
- [Kaynak geçmişi](graphics-event-list.md#resource-history)
<!-- /VERSIONLESS -->