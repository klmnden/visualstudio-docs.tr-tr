---
title: R etkileşimli REPL
description: Düzenleyici pencerelerini ile tümleşik R çözümdeki Studio etkileşimli REPL ortamı kullanma
ms.date: 06/28/2017
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 7109e74e858aa308b8f49e6e1e335478f801070b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62815000"
---
# <a name="work-with-the-r-interactive-window"></a>R etkileşimli pencere ile çalışma

R araçları için Visual Studio (RTVS) sağlayan bir R etkileşimli penceresi olarak da bilinen bir **REPL** (okuma-değerlendirme-Print-Loop) penceresi, R kodunu girin ve sonuçları hemen görün. Tüm modülleri, sözdizimini ve değişkenleri yanı IntelliSense, kullanılabilir etkileşimli pencerede.

Etkileşimli pencere normal R Düzenleyicisi windows ile de tümleştirilen. Kod ve ENTER tuşuna seçebileceğiniz **Ctrl**+**Enter**, veya sağ tıklayıp **etkileşimli içinde Yürüt**, ve kodu satır satır çalıştırılır etkileşimli pencereyi doğrudan yazılan alacağı. İmleç bir düzenleyici penceresinde tek bir satırda olduğunda **Ctrl**+**Enter** bu satırı etkileşimli pencereye gönderir ve ardından imleci sonraki satıra taşır. Bu şekilde yalnızca basabilirsiniz **Ctrl**+**Enter** için kodu adımlayın.

Bu özelliği kullanmak için izleyin [R ile çalışmaya başlama](getting-started-with-r.md) izlenecek yol bu makaledeki bölümler yanı sıra. [Kod parçacıkları](code-snippets-for-r.md) R Düzenleyici pencerelerinde yaptıkları gibi etkileşimli pencerede de çalışır.

## <a name="overview-of-the-interactive-window"></a>Etkileşimli pencereye genel bakış

Geçerli R kod yazıp ENTER tuşuna basarak **Enter** satırın sonunda kod satırdaki çalışır:

```repl
> 3 + 3
[1] 6
```

Tuşuna basarak **Enter** tek satırlı bir girdi bu satır ayrıca her yerde çalışır.

Önceki tüm giriş ve çıkış REPL salt okunur ve değiştirilemez. Ancak, seçin ve istediğiniz zaman penceresinden metin yanı sıra yapıştırılan kopyalayın. Yapıştırılan kod satırlarını girildiği gibi çalışır.

Diğer bir deyişle, deyimi ve tuşuna yazmaya başladığınızda **Enter**, RTVS deyim zaman ettirilmelidir bilir ve çok satırlı modu ile girer + solda ve uygun girintisini sor. RTVS, parantez, köşeli ayraçlar ve küme ayraçları ayrıca tamamlar:

![Etkileşimli pencerede çok satırlı beyanı girişi](media/repl-multiline-entry.png)

Bu çok satırlı modda **Enter** anahtarı, aksi takdirde, yeni bir satır ekler bloğun sonunda getirildiğinde, yalnızca kod bloğu çalışır. Ancak, basabilirsiniz **Ctrl**+**Enter** bu kodu çalıştırmak için herhangi bir konumda hemen engelleme.

### <a name="toolbar-commands"></a>Araç çubuğu komutlarını

Etkileşimli pencere ile kendi araç çubuğu şöyledir:

![Araç çubuğu ile etkileşimli penceresi](media/repl-window.png)

Araç çubuğu komutlarını gibidir, çoğunu klavye eşdeğerleri ve üzerinde de kullanılabilir **R Araçları** > **oturumu** ve **R Araçları**  >  **Çalışma dizini** menüleri (ya da belirtildiği gibi):

| Düğme | Komut | Tuş bileşimi | Açıklama |
| --- | --- | --- | --- |
| ![Sıfırla düğmesi](media/repl-toolbar-01-reset.png) | Sıfırlama | **CTRL**+**Shift**+**F10** | Tüm değişkenler ve geçmişi temizleniyor etkileşimli penceresi oturumu sıfırlar. |
| ![Temizle düğmesi](media/repl-toolbar-02-clear.png) | Temizle | **CTRL**+**m** | Etkileşimli pencerede gösterilen çıktıya temizler; oturum değişkenleri veya geçmiş etkilemez. |
| ![Geçmişi düğmeleri](media/repl-toolbar-03-history.png) | Önceki History komutu<br/>Sonraki History komutu | **Yukarı**, **aşağı**<br/>**Alt**+**yukarı**, **Alt**+**aşağı** | Çok satırlı kod blokları için belirli davranışlarla geçmişi kayar. Bkz: [geçmişi](#history). |
| ![Yük çalışma düğmesi](media/repl-toolbar-04-load-workspace.png) | Çalışma alanı yükleme | yok | Bir önceki çalışma kaydedilen yükler (bkz [çalışma alanları ve oturumları](#workspaces-and-sessions). |
| ![Düğme olarak çalışma alanını kaydetme](media/repl-toolbar-05-save-workspace-as.png)| Çalışma alanı olarak Kaydet | yok | Bir çalışma alanı olarak oturum geçerli durumunu kaydeder (bkz [çalışma alanları ve oturumları](#workspaces-and-sessions). |
| ![Kaynak R betiği düğmesi](media/repl-toolbar-06-source-r-script.png) | Source Skript R | **CTRL**+**Shift**+**S** | Çağrıları `source` etkin R betiği ile Visual Studio düzenleyicisinde, kodun çalıştığı.  Bu düğme, yalnızca bir R dosyası Visual Studio Düzenleyicisi'nde açık olduğunda görünür. |
| ![Source skript R echo düğmesi](media/repl-toolbar-07-source-r-script-with-echo.png) | Source Skript R Echo | **CTRL**+**Shift**+**girin** | Kaynak R betiği ile aynı ancak betiğin içeriklerini etkileşimli pencerede görüntüler. |
| ![R düğmesi kesme](media/repl-toolbar-08-interrupt-r.png)| Kesme R | **ESC** | Etkileşimli pencerede, hiçbir çalışan kodu gibi durdurur `while` döngü ekran görüntüsünde, bu bölümün başında gösterir. |
| ![Hata ayıklayıcı düğmesi ekleme](media/repl-toolbar-09b-attach-debugger.png)| Hata ayıklayıcının | yok | Ayrıca kullanılarak **hata ayıklama** > **R etkileşimli ekleme** komutu. |
| ![Kaynak dosya konumu düğmesi için çalışma dizinini Ayarla](media/repl-toolbar-10-set-working-directory-source.png)| Çalışma dizini için kaynak dosya konumu ayarlayın | **CTRL**+**Shift**+**E** | En son kaynaklı dosyası çalışma dizinine yüklenen etkileşimli pencereye kümeleri (kullanarak `source`). Bkz: [çalışma dizini](#working-directory). |
| ![Proje konumu düğmesi için çalışma dizinini ayarlayın](media/repl-toolbar-11-set-working-directory-to-project.png) | Çalışma dizini proje konumuna ayarlayın | **CTRL**+**Shift**+**P** | Visual Studio'da yüklü proje kök çalışma dizinini ayarlar. Bkz: [çalışma dizini](#working-directory). |
| (Metin alanı) | Çalışma seçin dizini | yok | Çalışma dizini için doğrudan giriş alanı. Bkz: [çalışma dizini](#working-directory). |

## <a name="workspaces-and-sessions"></a>Çalışma alanları ve oturumlar

Etkileşimli pencerede kod çalıştıran bir bağlamı geçerli oturumunuzdaki oluşturur. Genel değişkenler, işlev tanımları, kitaplık yükler ve benzeri bağlam oluşur. Bu bağlam topluca adlı bir *çalışma*, kaydedin ve herhangi bir zamanda çalışma alanları yüklemek.

Seçme **çalışma Kaydet** düğme veya kullanarak **R Araçları** > **oturumu** > **çalışma Kaydet**komut sizden bir konum ve dosya adı için (varsayılan uzantısı *. RData*).

Belirli bir dosya adı kullanarak bir çalışma alanı kaydetmek için (varsayılan değer *. RData*), tıklayarak **Kaydet çalışma** REPL düğmesi:

Daha önce kaydedilen bir çalışma alanını yeniden yüklemek için seçin **yük çalışma** düğmesine veya kullanın **R Araçları** > **oturumu** > **yük Çalışma alanı** ve çalışma dosyasına gidin.

**Sıfırlama** düğmesini veya **R Araçları** > **oturumu** > **sıfırlama** oturum bağlamı temizler. Uzak oturumu kullanıyorsanız, sıfırlandığında uzak makinede depolanan tüm dosyaları temizlemek için kullanıcı profili de silinir. (Bkz [çalışma alanları](r-workspaces-in-visual-studio.md#directories-on-local-and-remote-computers).)

## <a name="working-directory"></a>Çalışma dizini

Geliştiriciler genellikle etkileşimli bir oturum açıkken kendi çalışma dizininde değiştirmek isteyebilirsiniz. Çeşitli komutlara, araç çubuğunda kullanılabilir **R Araçları** > **çalışma dizini** menü ve proje bağlam menüsü çalışma dizini için bir kaynak dosyasının konumunu kolayca ayarlamanıza izin verir , konumu veya projenizi veya herhangi bir rastgele konumu. Bunun yapılması, dosyalar için söz konusu olduğunda tam yol adlarını veya uzun göreli yol adlarını yazarak önlemenize yardımcı olur.

## <a name="history"></a>Geçmiş

Etkileşimli pencerede, girdiğiniz her satırda bir Düzenleyicisi'nden gönderilen satırları içerir, geçmişi REPL korunur. Komut satırında büyük olasılıkla alışkın için olduğu gibi ardından yukarı ve aşağı ok tuşlarını geçmişinde gidebilirsiniz.

Tek fark, geçerli satırda yazmaya başlayın ve basarsanız, geçerli satırı de korunur geçmişinizi bile aracılığıyla henüz bu satırı henüz çalışmasıdır.

Etkileşimli pencerede geçmişi akıllıca satırları yayılan deyimleri diğer kod bloğunun ile de çalışır. Yukarı ve aşağı ok tuşlarını geçmişinde geçiş yapma, çok satırlı kod blokları tam bir birim olarak alınır ve geçerli girdi gösterilir. Bu noktada, üst veya alt ulaşılana kadar bu kod bloğu boyunca satır ok tuşlarını gidin. Kod bloğu başında yukarı ok önceki öğede geçmişini alır; alt satırında, aşağı oku sonraki öğeyi alır.

Bu davranışı geçmişini yukarı ok ile son öğenin artırarak algoritmanın yeniden çalıştırılması, genellikle bu durum barındırır ve **Enter** sağlarken doğal olarak bir çok satırlı kod bloğu için yukarı ok tuşlarına basarak düzenleme için birleşimi, tuş vuruşu kaydetme uygulamasına gidin.

Çok satırlı kod blokları şeklinde gezinme önlemek için araç çubuğu düğmelerini kullanın veya **Alt**+**yukarı** ve **Alt**-**Aşağı**, ve bu tür blokların tek bir satır olarak kabul edilir.

Geçmişi özelliği kullanmak için en kolay yolu, bunları kendiniz etkileşimli pencerede deneyin sağlamaktır. Aşağıdaki kod, birkaç uygun tek ve birden çok satırı deyimleri sağlar. Kopyala-yapıştır her deyimiyle tek tek, ancak uygun geçmişini oluşturmak için kullanın. (Ayrıca kodu ayrı kod dosyasına yapıştırın ve ardından etkileşimli pencere ile satırları göndermek **Ctrl**+**Enter**.)

```R
3 + 3

4 + 4

5 + 5

add <- function (x, y) {
  return (x + y)
}

sub <- function (x, y) {
  return (x - y)
}
```