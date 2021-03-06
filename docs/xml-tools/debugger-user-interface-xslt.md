---
title: XSLT hata ayıklayıcı pencereleri
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 846fdabd-e5c3-4688-9b0d-a93fbeea1b96
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b25c47e6db79fe4b860b6e7c209f0fc8403d0fcd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62838499"
---
# <a name="debugger-user-interface-xslt"></a>Hata ayıklayıcı kullanıcı arabirimi (XSLT)

Bu makalede, hata ayıklayıcı pencereleri ve iletişim kutuları açıklanır. Yalnızca özel XSLT hata ayıklama davranışa sahip kullanıcı arabirimi parçaları ele alınmaktadır.

Daha fazla bilgi için [kullanıcı arabirim başvurusunda hata ayıklama](../debugger/debugging-user-interface-reference.md).

## <a name="locals-window"></a>Yerel öğeler penceresi

Stil sayfasında tanımlanan tüm değişkenler hakkında bilgi için Yereller penceresine görüntüler. Yerel öğeler penceresinde üç sütun bilgileri içerir:

**Ad**

Bu sütun, geçerli kapsamdaki tüm yerel değişkenlerin adlarını içerir. Alt klasörlerinde görmek için detaya gidebilirsiniz bir ağaç denetimi düğümü vardır.

**Değer**

Bu sütunda yer alan her bir değişken değeri görüntülenir. Öznitelik, işlem yönergesi, yorum, metin ve CData düğümler, düğümün metin değerini görüntüler. Ad alanı URI Namespace düğümleri görüntüleyin.

**Tür**

Bu sütunda listelenen her bir değişken veri türünü tanımlayan **adı** sütun.

Yerel öğeler penceresinde de XSLT dönüşümü bağlamında izleyen önceden tanımlanmış bağlam değişkenlerini görüntüler. XSLT hata ayıklayıcısı tarafından kullanılan önceden tanımlanmış bağlam değişkenleri aşağıdaki tabloda açıklanmaktadır.

|Ad|Açıklama|
|-|-----------------|
|`last()`|İçerik boyutu.|
|`position()`|Konumu veya dizin sayısı, bağlam düğümü göre içerik boyutu.|
|`self::node()`|Bağlam düğümünün değeri.|

## <a name="output-window"></a>Çıktı penceresi

Çıkış penceresi, herhangi bir hata iletileri veya hata ayıklama sırasında oluşan bir güvenlik özel durumları gösterir. Ayrıca, hata ayıklayıcı çıkış gösterir.

## <a name="task-list"></a>Görev Listesi

**Görev listesi** stil sayfası tüm derleme hataları listeler. Hata çift hata satırı için imleç alır.

**Görev listesi** komut dosyası blokları XSLT dosyasında oluşan hataları içerir.

> [!NOTE]
> XSLT hata ayıklayıcısı hiçbir zaman görünürler, uyarı olduğundan **görev listesi**.

## <a name="breakpoints-window"></a>Kesme Noktaları penceresi

Kesme noktaları penceresi tüm kesme noktalarını ayarlayın geçerli projedeki gösterir. Pencerenin görünümde olduğu sürece bir kesme noktası eklenirse, pencerenin yeni kesme noktası gösterecek şekilde otomatik olarak güncelleştirilir.

Kesme noktaları penceresini diğer Visual Studio hata ayıklayıcıları aynı şekilde çalışacaktır.

## <a name="watch-window"></a>Gözcü penceresi

İzleme penceresi değişkenleri değerlendirmek için kullanılır. Değişkenlerin değerlerini de değiştirebilirsiniz.

İzleme penceresinde görüntülenen geçerli bağlam (çağrı yığınında en üst öğe) için değişkenlerdir. Bağlam değiştirirseniz, İzleme penceresinde güncelleştirir ve bu bağlam için ayarlanan değişkenler görüntüler.

## <a name="call-stack-window"></a>Çağrı Yığını penceresi

**Çağrı yığını** penceresinin, çağrı yığını, parametre türleri ve parametre değerlerini işlevlerin adları görüntülemek için kullanılır. Çağrı yığını bilgileri yalnızca ayıklanan programın bir kesme durumunda olduğunda gösterilir.

Çağrı yığınını XSLT yürütme oluşturulmak çeşitli bağlamı temsil eder. Örneğin, şablondan bir çağrı ise "a" Şablon "b", şablon "a" ve "b" şablonu görünür **çağrı yığını** penceresi listenin üst kısmındaki geçerli bağlam ile. Kullanıcı şu anda yürütülmekte olan sorgu görebilirsiniz.

Şablonlar XSLT dosyasında bir adı yoksa, XSLT işlemcisi tarafından oluşturulan adları kullanılır.

Bir listenin üst kısmındaki dışında bir öğeye tıklandığında Burada XSLT yürütme dal standart yeşil vurgu kullanarak oldu ve yeşil ok Görüntüleyicisi gösterir.

## <a name="quickwatch-dialog-box"></a>QuickWatch iletişim kutusu

**QuickWatch** iletişim kutusu, XPath 1.0 ifade değerlendirmek için kullanılır. Bağlam düğümünün ( `self::node()` Yereller penceresinde düğüm) için XPath ifadesinin yürütme bağlamı sağlar. XPath ifadesini yürütmenin sonucu İzleme penceresinde görüntülenir.

Aşağıdaki listede XPath ifadesi değerlendirmesi kısıtlamaları açıklar:

- Yerleşik XPath işlevleri izin verilir.

- Yerleşik XSLT işlevleri gibi `document()` ve `key()` izin verilmez.

- Kullanıcı tanımlı işlevlerde izin verilmez.

Daha fazla bilgi için [nasıl yapılır: Bir XPath ifadesini değerlendirme](../xml-tools/how-to-evaluate-an-xpath-expression.md).

## <a name="disassembly-window"></a>Ayrıştırma penceresi

Ayrıştırılmış kod penceresini XSLT derleyici tarafından oluşturulan bütünleştirilmiş kodu gösterir. Bu pencerede diğer Visual Studio çözümünü windows ile aynı şekilde kullanılabilir.

Daha fazla bilgi için [nasıl yapılır: Ayrıştırılmış kod penceresini kullanma](../debugger/how-to-use-the-disassembly-window.md).

## <a name="see-also"></a>Ayrıca bkz.

- [XSLT Hatalarını Ayıklama](../xml-tools/debugging-xslt.md)
- [Hata ayıklayıcıya ilk bakış](../debugger/debugger-feature-tour.md)
- [Visual Studio'da otolar ve yerel öğeler pencerelerinde değişkenleri denetleyin](../debugger/autos-and-locals-windows.md)