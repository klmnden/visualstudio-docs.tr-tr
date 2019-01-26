---
title: R ile verileri görselleştirmeyi
description: R çizim windows kullanarak Visual Studio programlarında verilerden çizim yapma.
ms.date: 06/29/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: bc568c6e2e28d27516ac5a92d7ccd01d3704bb7c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55009940"
---
# <a name="create-visual-data-plots-with-r"></a>Görsel verileri çizimleri R ile oluşturma

Çizim, veri Uzmanı'nın iş akışı önemli bir parçasıdır. R araçları için Visual Studio (RTVS), tüm çizim etkinlik bu anahtar etkinlik verimliliğinizi artırmaya yönelik bir veya daha fazla çizim windows etrafında ortalar.

![Hero görüntüsü çizme](media/plotting-hero-image.png)

|   |   |
|---|---|
| ![video kamera simgesini film](../install/media/video-icon.png "bir video izleyin") | [(Youtube.com) videoyu](https://www.youtube.com/watch?v=ZTbKmz5RSgY) R (2 dk. 02s) ile çizim üzerinde. |

## <a name="the-plot-window"></a>Çizim penceresi

Çizimler, burada her bir çizim oluşturulur tarafından bir dizi bir çizim penceresi tutan bir `plot` komutu. Örneğin, kullanarak `plot(1:100)` biri zaten mevcut değilse yeni bir çizim penceresi oluşturur:

![1 ile 100 arası doğrusal çizimi](media/plotting-1-to-100.png)

Teknik terimlerle açıklamak gerekirse, R `plot` komutları işlemek çıktılarını bir R grafik cihazına; bir çizim penceresi her çizim pencere cihaz birkaç verilen neden olduğu bir R grafik cihazı içeriğini işler.

Çizim windows Visual Studio projelerinde bağımsızdır ve açık kalır, yük ve projeleri kapatın.

Bir çizim oluşturma kullanır "etkin" bir çizim penceresinde önceki herhangi bir kaydetme çizim, çizim geçmişi (bkz [çizim geçmişi](#plot-history)). Örneğin, `plot(100:1)` ve ilk çizim aşağıya bir satır ile değiştirilir.

Diğer tüm Visual Studio windows gibi. Özel düzenler çizim pencereyi destekler (bkz [Visual Studio'da pencere düzenlerini özelleştirme](../ide/customizing-window-layouts-in-visual-studio.md). Çizim windows Visual Studio çerçeve içinde farklı konumlara yerleştirilmiş, çerçeveye yeniden boyutlandırılmış veya tamamen bağımsız bir yeniden boyutlandırma için çerçevenin dışında çekilir.

Her zaman bir çizim penceresi yeniden boyutlandırma çizim en iyi kalite görüntü sağlamak üzere yeniden işler. Genellikle, bir çizim, çizim bir dosyaya veya sonraki bölümde açıklanan komutları kullanarak Pano dışarı aktarmadan önce yeniden boyutlandırmak istediğiniz.

## <a name="plot-window-commands"></a>Çizim penceresi komutları

Çizim pencerenin araç çoğunu aracılığıyla da uygulanabilir komutları tutan **R Araçları** > **çizimleri** menüsü.

| Düğme | Komut | Açıklama |
| --- | --- | --- |
| ![Yeni bir çizim penceresi düğmesi](media/plotting-toolbar-01-new-plot-window.png) | Yeni bir çizim penceresi | Ayrı çizim penceresi ile kendi geçmişini oluşturur. Bkz: [birden çok çizim windows](#multiple-plot-windows). |
| ![Çizim penceresi düğmeyi etkinleştirin](media/plotting-toolbar-02-activate-plot-window.png) | Çizim penceresini etkinleştir | Etkin pencereyi, bu nedenle, sonraki geçerli çizim pencerenin ayarlar `plot` komutları pencereye işlenir. Bkz: [birden çok çizim windows](#multiple-plot-windows). Bkz: [birden çok çizim windows](#multiple-plot-windows). |
| ![Çizim Geçmişi penceresini düğmesi](media/plotting-toolbar-03-plot-history.png) | Geçmiş penceresinde Çiz | Küçük resim olarak gösterilen geçmişinde bulunan tüm çizimleri ile bir pencere açılır. Bkz: [çizim geçmişi](#plot-history). |
| ![Geçmişi düğmeleri çizilecek](media/plotting-toolbar-04-plot-history-arrows.png) | Önceki/sonraki çizim |  Önceki veya sonraki çizim geçmişi gider. Ctrl + Alt + F11 (önceki) ve Ctrl + Alt + F12 (İleri) ile geçmiş da gidebilirsiniz. Bkz: [çizim geçmişi](#plot-history). |
| ![Görüntüyü düğme olarak Kaydet](media/plotting-toolbar-05-save-as-image.png)| Görüntü olarak Kaydet | Bir dosya adı için ister ve geçerli çizim (penceresi içeriği, pencere boyutu) bir görüntü dosyasına kaydeder. Kullanılabilir biçimler `.png`, `.jpg`, `.bmp`, ve `.tif`. |
| ![PDF düğme olarak Kaydet](media/plotting-toolbar-06-save-as-pdf.png)| PDF olarak Kaydet | Geçerli pencere boyutunu kullanarak bir PDF dosyası için geçerli çizim kaydeder. PDF ölçeklendirilirse çizim yeniden işlenir. |
| ![Bit eşlem düğmesi olarak Kopyala](media/plotting-toolbar-07-copy-as-bitmap.png)| Bit eşlem olarak Kopyala | Çizim, geçerli pencere boyutunu kullanarak bir tarama bit eşlem olarak panoya kopyalar. |
| ![Meta dosyası düğme olarak Kopyala](media/plotting-toolbar-08-copy-as-metafile.png)| Meta dosyası olarak Kopyala | Çizim panoya kopyalar bir [Windows Meta dosyası](https://en.wikipedia.org/wiki/Windows_Metafile) (Wikipedia). |
| ![Çizim düğmeyi kaldırma](media/plotting-toolbar-09-remove-plot.png)| Odebrat Diagram | Geçerli çizim Geçmişi'nden kaldırır. |
| ![Tümünü çizimleri Temizle düğmesi](media/plotting-toolbar-10-clear-all-plots.png) | Tüm çizimleri Temizle | Tüm çizimleri (onay istemleri) geçmişini kaldırır. |

## <a name="multiple-plot-windows"></a>Birden çok çizim windows

Veri bilimcileri genellikle birçok farklı veri kümelerinden birçok çizimleri çalışmak için RTVS olabildiğince çok bağımsız çizim windows oluşturmanıza olanak sağlar. Visual Studio çerçevesinde veya çerçevenin dışında tamamen gibi ancak daha sonra bu windows düzenleyebilirsiniz. (Bkz [Visual Studio'da pencere düzenlerini özelleştirme](../ide/customizing-window-layouts-in-visual-studio.md) yerleştirme ve windows yeniden boyutlandırma ile ilgili genel bilgi için.)

Yeni bir çizim penceresi araç çubuğu düğmesini kullanarak oluşturduğunuz veya **R Araçları** > **çizimleri** > **yeni bir çizim pencere**. Yeni bir çizim penceresi olur *etkin* yeni çizimleri nerede işlendiğini olan bir pencere. Etkin pencereyi değiştirmek için ona geçiş yapın ve seçin **çizim penceresini etkinleştir** araç çubuğu düğmesini veya **R Araçları** > **çizer**  >  **Çizim penceresini etkinleştir**.

Olan çok, bağımsız nesneler çizimleri, yani kopyalayın veya çizim windows ya da sürükle ve bırak kullanılarak veya fare kullanarak arasında taşıyın **kopyalama**, **Kes**, ve **Yapıştır** sağ bağlam komutları ve **Düzenle** menüleri.

Kopyalama için sürükle ve bırak varsayılan davranıştır; taşımak için sürükle ve tutarken bırak **Shift** anahtarı.

## <a name="plot-history"></a>Çizim geçmişi

Çizim komutlarını tüm, oturum içindeki çizim korunmasını sağlamak, her bir pencere için bir çizim geçmişi korunur. Git geçmişi, çizim penceresi araç çubuğunda, ok düğmelerini kullanın veya **Ctrl**+**Alt**+**F11** ve **Ctrl** + **Alt**+**F12**. Ayrıca tek çizimleri kaldırın veya tüm çizimleri araç çubuğu düğmeleri kullanarak yeniden penceresinden temizleyin veya **R Araçları** > **çizer** menü komutları.

Çizimler koleksiyonunun tamamını görmek için araç çubuğu düğmesini kullanarak çizim Geçmişi penceresini açın veya **R Araçları** > **çizer** > **çizim Geçmişi penceresini**.
Geçmiş farklı çizim windows (veya cihaz) gruplandırılmış Bu pencerede görüntülenen çizimleri için küçük bir listesini sağlar. Araç çubuğundaki Yakınlaştırma düğmelerini kullanarak, küçük resimlerin boyutunu değiştirir.

![Geçmiş penceresinde Çiz](media/plotting-plot-history-window.png)

Bir çizim, ilişkili bir pencerede açmak için bu grafik çift tıklayın, seçin ve ardından **Göster çizim** araç çubuğu düğmesini veya sütuna sağ tıklayıp **Göster çizim**. Bireysel belirleyebilirsiniz çizim ve kopyalama, kesme veya sağ tıklama bağlamdan silme veya **Düzenle** menüleri.

Tüm windows üzerinde çizim geçmişinizi ömrünü etkileşimli R oturumunuz ömrünü bağlıdır. R oturumunuz sıfırlama veya çıkın ve Visual Studio'yu yeniden başlatın, çizim geçmişinizi sıfırlanır.

## <a name="programmatically-manipulate-plot-windows"></a>Çizim windows programsal

Diagram R kodunu Windows'dan özel çizim windows tanımlamak için cihaz numaralarını kullanarak program aracılığıyla yönetebilirsiniz.

- `dev.list()`: Tüm grafik aygıtların geçerli R oturumunda listelenmektedir.
- `dev.new()`: Yeni bir grafik cihazı (yeni bir çizim pencere) oluşturun.
- `dev.set(<device number>)`: Etkin grafik cihazına ayarlayın.
- `dev.off()`: Etkin cihaz silin.
