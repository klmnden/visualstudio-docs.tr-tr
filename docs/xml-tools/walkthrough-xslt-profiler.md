---
title: 'İzlenecek yol: XSLT Profil Oluşturucusu'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 87387c9a-2e89-4801-ad51-83740cd6ea25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1866500fc4b04622aeb469f663b3b3893ca89c80
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55954549"
---
# <a name="walkthrough-xslt-profiler"></a>İzlenecek yol: XSLT Profil Oluşturucusu

XSLT Profiler ölçülmesine yardımcı olmak, değerlendirme ve performans ile ilgili sorunları XSLT kodda hedef ayrıntılı XSLT performans raporları oluşturur. XSLT Profiler XSL ve XSLT stil sayfası iyileştirmeler için faydalı ipuçları içerir. XSLT uygulamaları için isteğe bağlı en yüksek performans, bu aracı gerekli olabilir.

## <a name="prerequisites"></a>Önkoşullar

Aşağıdaki örneklerde yer alan yordamlar, Visual Studio ve .NET Framework 4.0 veya sonraki bir sürümü gerektirir.

### <a name="create-the-performance-report"></a>Performans raporu oluşturun

1.  XSLT belge Visual Studio'da açın.

2.  Tıklayarak **profil XSLT** XML menüsünde sağlanır seçeneği.

3.  Girdi XML belgesini sağlar. Bir XML belgesi zaten açık değilse, dosya için istenir.

4.  Analiz başlar ve bir ilerleme çubuğu Düzenleyicisi içinde ilerlemesini görüntüler.

5.  XSLT çıkış çıkış Bölmesi'nde görünür.

6.  Performans oturumu sona erdikten sonra bu performans raporu denetleyin. Bir performans raporda kaydedilen verileri görüntüleyin ve XSLT Performans analiz sağlar.

### <a name="get-all-the-available-views"></a>Tüm kullanılabilir görünümlere Al

1.  Tıklayarak **Geçerli Görünüm** tüm kullanılabilir görünümlere almak için aşağı açılan listesi.

2.  Seçin **özeti görünümünü** seçeneğini **Geçerli Görünüm** aşağı açılan listesi. Varsayılan olarak, bir performans raporu görüntülenen **özeti görünümünü**. Bu görünüm, XSLT belge ile performans sorunlarını belirlemek için bir başlangıç noktasıdır. **Özeti görünümünü** aşağıdaki veri noktaları listelenmektedir:

    -   En çok çağrılan İşlevler

    -   En bireysel işlerle İşlevler

    -   Yürütmek için en uzun zaman ayırdığınız işlevleri

3.  Varsayılan olarak, her veri noktası için üç sütun vardır: işlev, mutlak değeri içinde çağrı sayısı ve toplam işlev çağrısı adlandırılmış işlevinin bir yüzde değeri adı. Her bir veri noktası **özeti görünümünü**, daha ayrıntılı görünüm için işlev veri noktalarına sağ tıklayarak gidebilirsiniz.

4.  Seçin **işlev görünümü** seçeneğini **Geçerli Görünüm** aşağı açılan listesi. **İşlev görünümü** profil oluşturma sırasında çağrılan işlevlerin listeler. Bir sütun adına tıklayarak verileri yeniden sıralayabilirsiniz. Varsayılan olarak görüntülenen sütunlar şunlardır:

    -   **İşlev adı**

    -   **Geçen kapsamlı süre**

    -   **Geçen dışlamalı süre**

    -   **Kapsamlı uygulama süresi**

    -   **Dışlamalı uygulama süresi**

    -   **Çağrı sayısı**

5.  Tüm saat sütunları hem mutlak değerler hem de yüzde görüntülenir. Terim **özel** diğer işlevleri tarafından harcanan zamanı fiyatlara geçen yürütülürken, bu işlevin yürütülmesi sırasında çağrılan işlev için toplam süreyi ifade eder.

6.  Terim **Inclusive** adlı ve diğer işlevleri olarak adlandırılan işlevlerin çağrılma bunlardan herhangi bir işlev, yürütme süresi dahil olmak üzere tüm işlevlerin yürütülürken harcanan toplam süreyi gösterir.

### <a name="select-callercallee-view"></a>Arayan/Aranan görünümü seçin

1.  Seçin **çağıran/çağrılan** görünümünde **Geçerli Görünüm** aşağı açılan listesi.

2.  **Çağıran/çağrılan** görünümü, aşağıdaki üç ayrı bölümü vardır:

    -   **Çağıran işlevler**: Belirli bir işlevi çağrılan tüm işlevleri görünümün üst kısmında listelenir.

    -   **Geçerli işlev**: Belirli işlev çağrıldı görünümün orta bölümünde listelenir.

    -   **Tarafından çağrılan işlevler** : Belirli işlev tarafından çağrılan tüm işlevleri görünümün alt kısmında listelenir.

3.  Adlı bir işlev ise `SyncToNavigator` çağrılan tüm işlevleri görünümü ikinci kısmında görünür `SyncToNavigator` işlevi Görünüm ve tarafından çağrılan tüm işlevler üst kısmında görünür `SyncToNavigator` görünümün alt kısmında görüntülenir.

4.  İşlev görünümü Orta kısmındaki görünümün diğer iki bölümü listelenen işlevlerden herhangi birinin çift tıklayarak değiştirebilirsiniz. Görünüm, daha sonra otomatik olarak değişiklikleri yansıtacak şekilde güncelleştirilir.

5.  Ayrıca, verileri sütun adlarını tıklatarak sıralayabilirsiniz.

### <a name="select-call-tree-view"></a>Çağrı ağacı görünümü seçin

1.  Seçin **çağrı ağacı görünümü** içinde **Geçerli Görünüm** aşağı açılan listesi. Bu program yürütme ağaç görünümünü görünümüdür.

2.  **Çağrı ağacı görünümü** işlem adı olarak ağacının kökü gösterir. Ağaç düğümleri işlevlerdir. Bu görünüm belirli çağrı izlemeleri ayrıntıya ve hangi izlemeleri en yüksek performans etkisi analiz sağlar. Görünüm benzer **çağrı yığın görünümü** hata ayıklama sırasında kullanılabilir. Ek sütunları **işlev görünümü**, **çağrı ağacı görünümü**, görüntülenecek ek bir sütun yok **modül adı**.

3.  Seçin **işaretleri** içinde **Geçerli Görünüm** aşağı açılan listesi.

4.  SLT Profiler ile ilişkili bir açıklamayla veri koleksiyonu akışında görünmesini işaretleri vardır. İşaretleri sayaçları sahip kodda yerlerdir. XSLT Profiler XSLT performans sayaçları toplamak için size zaman sayaçları biri bu işaretler, yürütülen her zaman toplanan. Veriler içeren bir tablo görüntülenir **işaret kimliği**, **işareti adı** (**başlangıç programı**, **son Program**) ve  **Zaman damgası**. İşaretleri değil toplanır ve kronolojik sırada görünmesini **işaret görünümü** performans raporu.

### <a name="select-modules-in-the-current-view"></a>Geçerli görünümde modülleri seçin

1.  Seçin **modülleri** içinde **Geçerli Görünüm** aşağı açılan listesi.

2.  Modüller görünümü, tüm işlevler için Modül düzeyinde toplanmış düz listesidir. Genişlet veya daralt görüntülemek veya modül performans verileri görünümü kapatmak için modül adı. Bir sütun adına tıklayarak verileri yeniden sıralayabilirsiniz. Varsayılan olarak mevcuttur hem mutlak değerler hem de yüzde sayılar için **geçen kapsamlı süre**, **geçen dışlamalı süre**, **kapsamlı uygulama süresi**, **Dışlamalı uygulama süresi**, ve **çağrılarını**.

3.  Seçin **işlem** içinde **Geçerli Görünüm** aşağı açılan listesi.

4.  İşlem görünümü içeren bir tablo görüntüler **işlem kimliği**, **işlem adı**, **başlaması zamanı**ve **bitiş zamanı**. Veri sütunu adları tıklayarak sıralanabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: XSLT hiyerarşisi kullanma](../xml-tools/walkthrough-using-xslt-hierarchy.md)