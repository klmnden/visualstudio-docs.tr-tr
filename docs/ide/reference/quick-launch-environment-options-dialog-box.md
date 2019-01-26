---
title: Hızlı Başlatma, Ortam, Seçenekler İletişim Kutusu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
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
ms.openlocfilehash: 029b42cf4a1df9fdb2082e8202c0557827b0ba7a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55020977"
---
# <a name="quick-launch-environment-options-dialog-box"></a>Hızlı Başlatma, Ortam, Seçenekler İletişim Kutusu

Kullanabileceğiniz **hızlı başlatma** hızlıca arayıp seçenekleri, şablonlar, menüler gibi IDE varlıklar için Eylemler yürütmek için. Kullanamazsınız **hızlı başlatma** koduna ve simgelere için aranacak. **Hızlı başlatma** arama kutusu menü çubuğunun sağ üst köşede bulunur ve Ctrl + Q tuşlarını seçerek erişilebilir. Yalnızca arama dizenizle kutuya girin. İçeren dizeleri aramak için @, Kullan ”@@”. 

**Hızlı başlatma** Visual Studio'yu yüklediğinizde varsayılan olarak etkindir. Menü çubuğunda göster gizle veya istediğiniz **hızlı başlatma** seçerek **Araçları**, **seçenekleri**. Genişletin **ortamları** düğümünü seçip **hızlı başlatma**. Seçin veya temizleyin **Hızlı Başlat'ı etkinleştirme** onay kutusu. Etkinleştirin veya bu sayfadaki arama kategorileri devre dışı bırakın.

## <a name="category-list"></a>Kategori Listesi

Hızlı Başlatma arama sonuçları dört kategorilerde görüntülenir: **En son kullanılan**, **menüleri**, **seçenekleri**, ve **açık belgeler**, birlikte kategorideki öğelerin sayısı. Kategoriye göre arama sonuçlarıyla geçirmek için İleri kategorisinden tüm sonuçları göstermek için Ctrl + Q anahtarları seçin. Sonra son kategori, Ctrl + Q her kategori birkaç sonuçlarını gösteren görünür. Ctrl + Shift + Q kategorilerinizin ters sırada gitmek için kullanabilirsiniz. Bir kategori altında tüm arama sonuçlarını görüntülemek için kategori adı seçin.

Aramanızı belirli kategorileri sınırlandırmak için aşağıdaki kısayolları kullanabilirsiniz.

|Kategori|Kısayol|Kısayol açıklaması|
|--------------|--------------| - |
|En son kullanılan|@mru<br /><br /> Örneğin, `@mru font`|En fazla beş öğe, görüntüler **en son kullanılan**.|
|Menüler|@menu<br /><br /> Örneğin, `@menu font`|Arama menü öğeleri için sınırlar.|
|Seçenekler|@opt<br /><br /> Örneğin, `@opt font`|Arama ayarları için sınırları **seçenekleri** iletişim kutusu.|
|Belgeler|@doc<br /><br /> Örneğin, `@doc font`|Arama ölçütlerine dosya adlarını ve yollarını açık belgelerin arama sınırlanır ancak dosyaları içindeki metin arama yapmaz.|

> [!NOTE]
> Kısayol tuşlarını değiştirebileceğiniz **genel**, **klavye** sayfasını **seçenekleri** iletişim kutusu.

## <a name="show-previous-results"></a>Önceki sonuçları göster

Varsayılan olarak, girdiğiniz arama terimi arama oturumları arasında tutarlı olmaz. Arama dizesi, bir dönem için arama yaparsanız temizlenir dışında imleci taşıma **hızlı başlatma** alan ve ardından Git yedekleyin. Arama sonuçlarını tutmak için şuraya gidin: **seçenekleri** iletişim kutusunda **hızlı başlatma**ve ardından **hızlı başlatma etkinleştirildiğinde önceki aramaya ait Show arama sonuçları.** Onay kutusunu seçin. Bir arama yapın, hızlı başlat alanında bırakın ve geri gelen Hızlı Başlat son kullanılan arama terimi korumak ve ayrıca, arama sonuçlarını gösterir.

En son ipuçları ve püf noktaları kullanma **hızlı başlatma**, bkz: [Visual Studio blogu](http://go.microsoft.com/fwlink/?LinkId=236054).

## <a name="see-also"></a>Ayrıca Bkz.

- [Ortam Seçenekleri İletişim Kutusu](../../ide/reference/environment-options-dialog-box.md)