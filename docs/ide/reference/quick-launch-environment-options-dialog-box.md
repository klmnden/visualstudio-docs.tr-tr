---
title: Hızlı Başlatma, Ortam, Seçenekler İletişim Kutusu
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Environment.QuickLaunch
- vs.quicklaunch
helpviewer_keywords:
- searching IDE
- IDE, searching
ms.assetid: 4200f297-d065-4723-9a30-d91ff2e26c9d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
monikerRange: vs-2017
ms.openlocfilehash: a67e909dc43f17e12dd63b7a8a3b2e8a4afacc5e
ms.sourcegitcommit: d4bea2867a4f0c3b044fd334a54407c0fe87f9e8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2019
ms.locfileid: "58789880"
---
# <a name="quick-launch-environment-options-dialog-box"></a>Hızlı Başlatma, Ortam, Seçenekler İletişim Kutusu

Kullanabileceğiniz **hızlı başlatma** hızlıca arayıp seçenekleri, şablonlar, menüler gibi IDE varlıklar için Eylemler yürütmek için. Kullanamazsınız **hızlı başlatma** koduna ve simgelere için aranacak. **Hızlı başlatma** arama kutusu menü çubuğunun sağ üst köşede bulunur ve tuşlarına basarak erişilebilir **Ctrl**+**Q**. Arama dizesinin kutuya yazın. İçeren dizeleri aramak için @, Kullan ”@@”. 

**Hızlı başlatma** Visual Studio'yu yüklediğinizde varsayılan olarak etkindir. Menü çubuğunda göster gizle veya istediğiniz **hızlı başlatma** seçerek **Araçları** > **seçenekleri**. Genişletin **ortamları** düğümünü seçip **hızlı başlatma**. Seçin veya temizleyin **Hızlı Başlat'ı etkinleştirme** onay kutusu. Etkinleştirin veya bu sayfadaki arama kategorileri devre dışı bırakın.

## <a name="category-list"></a>Kategori Listesi

Hızlı Başlatma arama sonuçları dört kategorilerde görüntülenir: **En son kullanılan**, **menüleri**, **seçenekleri**, ve **açık belgeler**, birlikte kategorideki öğelerin sayısı. Kategoriye göre arama sonuçları arasında çapraz tercih **Ctrl**+**Q** sonraki kategorisinden tüm sonuçları göstermek için anahtarları. Son kategori göründükten sonra **Ctrl**+**Q** her kategori birkaç sonuçlarını gösterir. Tuşuna **Ctrl**+**Shift**+**Q** kategorilerinizin ters sırada gidin. Bir kategori altında tüm arama sonuçlarını görüntülemek için kategori adı seçin.

Aramanızı belirli kategorileri sınırlandırmak için aşağıdaki kısayolları kullanabilirsiniz.

|Kategori|Kısayol|Kısayol açıklaması|
|--------------|--------------| - |
|En son kullanılan|@mru<br /><br /> Örneğin, `@mru font`|En fazla beş öğe, görüntüler **en son kullanılan**.|
|Menüler|@menu<br /><br /> Örneğin, `@menu project`|Arama menü öğeleri için sınırlar.|
|Seçenekler|@opt<br /><br /> Örneğin, `@opt font`|Arama ayarları için sınırları **seçenekleri** iletişim kutusu.|
|Belgeler|@doc<br /><br /> Örneğin, `@doc program.cs`|Arama ölçütlerine dosya adlarını ve yollarını açık belgelerin arama sınırlanır ancak dosyaları içindeki metin arama yapmaz.|

> [!NOTE]
> Kısayol tuşlarını değiştirebileceğiniz **genel** > **klavye** sayfasını **seçenekleri** iletişim kutusu.

## <a name="show-previous-results"></a>Önceki sonuçları göster

Varsayılan olarak, girdiğiniz arama terimi arama oturumları arasında tutarlı olmaz. Arama dizesi, bir dönem için arama yaparsanız temizlenir dışında imleci taşıma **hızlı başlatma** alan ve ardından Git yedekleyin. Arama sonuçlarını tutmak için şuraya gidin: **seçenekleri** iletişim kutusunda **hızlı başlatma**ve ardından **hızlı başlatma etkinleştirildiğinde önceki aramaya ait Show arama sonuçları.** Onay kutusunu seçin. Bir arama yapın, hızlı başlat alanında bırakın ve geri gelen Hızlı Başlat son kullanılan arama terimi korumak ve ayrıca, arama sonuçlarını gösterir.

## <a name="see-also"></a>Ayrıca bkz.

- [Ortam Seçenekleri İletişim Kutusu](../../ide/reference/environment-options-dialog-box.md)
