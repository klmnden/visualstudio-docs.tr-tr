---
title: XSLT performans
ms.date: 03/05/2019
ms.topic: conceptual
ms.assetid: 87387c9a-2e89-4801-ad51-83740cd6ea25
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 8ecc5482c8519ceadfe1e6d5db7880c98b3d2ceb
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57525485"
---
# <a name="the-xslt-profiler"></a>XSLT Profiler

XSLT Profiler ölçülmesine yardımcı olmak, değerlendirme ve performans ile ilgili sorunları XSLT kodda hedef ayrıntılı XSLT performans raporları oluşturur. XSLT Profiler XSL ve XSLT stil sayfası iyileştirmeler için faydalı ipuçları içerir. XSLT uygulamaları için isteğe bağlı en yüksek performans, bu aracı gerekli olabilir.

XSLT Profiler Visual Studio'nun bir parçasıdır ve kullanılabilir **XML** menüsü.

![XSLT Profil Oluşturucusu](../xml-tools/media/profile-xslt-menu.png)

> [!NOTE]
> XSLT Profiler yalnızca Visual Studio Enterprise sürümünde kullanılabilir.

## <a name="create-a-performance-report"></a>Performans raporu oluşturun

1. XSLT belge Visual Studio'da açın.

2. Menü çubuğunda, **XML** > **profil XSLT**.

3. Girdi XML belgesini sağlar. Bir XML belgesi zaten açık değilse, dosya için istenir.

   Analiz başlar ve bir ilerleme çubuğu Düzenleyicisi içinde ilerlemesini görüntüler. XSLT çıkış da görülebilir.

4. Performans oturumu sona erdikten sonra XSLT performansını analiz etmek için performans raporuna bakın.

## <a name="get-all-available-views"></a>Tüm kullanılabilir görünümlere Al

1. Tıklayarak **Geçerli Görünüm** tüm kullanılabilir görünümlere almak için aşağı açılan listesi.

2. Seçin **özeti görünümünü** seçeneğini **Geçerli Görünüm** aşağı açılan listesi. Varsayılan olarak, bir performans raporu görüntülenen **özeti görünümünü**. Bu görünüm, XSLT belge ile performans sorunlarını belirlemek için bir başlangıç noktasıdır. **Özeti görünümünü** aşağıdaki veri noktaları listelenmektedir:

   - En çok çağrılan İşlevler

   - En bireysel işlerle İşlevler

   - Yürütmek için en uzun zaman ayırdığınız işlevleri

   Varsayılan olarak, her veri noktası için üç sütun vardır: işlev, mutlak değeri içinde çağrı sayısı ve toplam işlev çağrısı adlandırılmış işlevinin bir yüzde değeri adı. Her bir veri noktası **özeti görünümünü**, daha ayrıntılı görünüm için işlev veri noktalarına sağ tıklayarak gidebilirsiniz.

3. Seçin **işlev görünümü** seçeneğini **Geçerli Görünüm** aşağı açılan listesi. **İşlev görünümü** profil oluşturma sırasında çağrılan işlevlerin listeler. Bir sütun adına tıklayarak verileri yeniden sıralayabilirsiniz. Varsayılan olarak görüntülenen sütunlar şunlardır:

    - **İşlev adı**

    - **Geçen kapsamlı süre**

    - **Geçen dışlamalı süre**

    - **Kapsamlı uygulama süresi**

    - **Dışlamalı uygulama süresi**

    - **Çağrı sayısı**

   Tüm saat sütunları hem mutlak değerler hem de yüzde görüntülenir. Terim **özel** diğer işlevleri tarafından harcanan zamanı fiyatlara geçen yürütülürken, bu işlevin yürütülmesi sırasında çağrılan işlev için toplam süreyi ifade eder.

   Terim **Inclusive** adlı ve diğer işlevleri olarak adlandırılan işlevlerin çağrılma bunlardan herhangi bir işlev, yürütme süresi dahil olmak üzere tüm işlevlerin yürütülürken harcanan toplam süreyi gösterir.

## <a name="select-callercallee-view"></a>Arayan/Aranan görünümü seçin

Seçin **çağıran/çağrılan** görünümünde **Geçerli Görünüm** aşağı açılan listesi. **Çağıran/çağrılan** görünümü, aşağıdaki üç ayrı bölümü vardır:

- **Çağıran işlevler**: Belirli bir işlevi çağrılan tüm işlevleri görünümün üst kısmında listelenir.

- **Geçerli işlev**: Belirli işlev çağrıldı görünümün orta bölümünde listelenir.

- **Tarafından çağrılan işlevler**: Belirli işlev tarafından çağrılan tüm işlevleri görünümün alt kısmında listelenir.

Adlı bir işlev ise `SyncToNavigator` çağrılan tüm işlevleri görünümü ikinci kısmında görünür `SyncToNavigator` işlevi Görünüm ve tarafından çağrılan tüm işlevler üst kısmında görünür `SyncToNavigator` görünümün alt kısmında görüntülenir.

- İşlev görünümü Orta kısmındaki görünümün diğer iki bölümü listelenen işlevlerden herhangi birinin çift tıklayarak değiştirebilirsiniz. Görünüm, daha sonra otomatik olarak değişiklikleri yansıtacak şekilde güncelleştirilir.

- Ayrıca, verileri sütun adlarını tıklatarak sıralayabilirsiniz.

## <a name="select-call-tree-view"></a>Çağrı ağacı görünümü seçin

- Seçin **çağrı ağacı görünümü** içinde **Geçerli Görünüm** aşağı açılan listesi. Bu program yürütme ağaç görünümünü görünümüdür.

   **Çağrı ağacı görünümü** işlem adı olarak ağacının kökü gösterir. Ağaç düğümleri işlevlerdir. Bu görünüm belirli çağrı izlemeleri ayrıntıya ve hangi izlemeleri en yüksek performans etkisi analiz sağlar. Görünüm benzer **çağrı yığın görünümü** hata ayıklama sırasında kullanılabilir. Ek sütunları **işlev görünümü**, **çağrı ağacı görünümü**, görüntülenecek ek bir sütun yok **modül adı**.

- Seçin **işaretleri** içinde **Geçerli Görünüm** aşağı açılan listesi.

   XSLT Profiler ile ilişkili bir açıklamayla veri koleksiyonu akışında görünmesini işaretleri vardır. İşaretleri sayaçları sahip kodda yerlerdir. XSLT Profiler XSLT performans sayaçları toplamak için size zaman sayaçları biri bu işaretler, yürütülen her zaman toplanan. Veriler içeren bir tablo görüntülenir **işaret kimliği**, **işareti adı** (**başlangıç programı**, **son Program**) ve  **Zaman damgası**. İşaretleri değil toplanır ve kronolojik sırada görünmesini **işaret görünümü** performans raporu.

## <a name="select-modules-in-the-current-view"></a>Geçerli görünümde modülleri seçin

- Seçin **modülleri** içinde **Geçerli Görünüm** aşağı açılan listesi.

   Modüller görünümü, tüm işlevler için Modül düzeyinde toplanmış düz listesidir. Genişlet veya daralt görüntülemek veya modül performans verileri görünümü kapatmak için modül adı. Bir sütun adına tıklayarak verileri yeniden sıralayabilirsiniz. Varsayılan olarak mevcuttur hem mutlak değerler hem de yüzde sayılar için **geçen kapsamlı süre**, **geçen dışlamalı süre**, **kapsamlı uygulama süresi**, **Dışlamalı uygulama süresi**, ve **çağrılarını**.

- Seçin **işlem** içinde **Geçerli Görünüm** aşağı açılan listesi.

   İşlem görünümü içeren bir tablo görüntüler **işlem kimliği**, **işlem adı**, **başlaması zamanı**ve **bitiş zamanı**. Veri sütunu adları tıklayarak sıralanabilir.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: XSLT hiyerarşisi kullanma](../xml-tools/walkthrough-using-xslt-hierarchy.md)