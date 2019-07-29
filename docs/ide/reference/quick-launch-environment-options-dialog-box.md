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
ms.openlocfilehash: 1f5026a014b5adc96f0729d130c4398474d6d413
ms.sourcegitcommit: ce1ab8a25c66a83e60eab80ed8e1596fe66dd85c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/29/2019
ms.locfileid: "68605901"
---
# <a name="quick-launch-environment-options-dialog-box"></a>Hızlı Başlatma, Ortam, Seçenekler İletişim Kutusu

Seçenekler, şablonlar, menüler gibi IDE varlıkları için eylemleri hızlıca aramak ve yürütmek üzere **Hızlı Başlat** ' ı kullanabilirsiniz. Kodu ve sembolleri aramak için **Hızlı başlatma** kullanamazsınız. **Hızlı Başlat** arama kutusu, menü çubuğunun sağ üst köşesinde bulunur ve **CTRL**+**Q**tuşlarına basarak erişilebilir. Arama dizenizi kutuya yazın. İçeren dizeleri aramak için @, Kullan ”@@”.

**Hızlı başlatma** , Visual Studio 'yu yüklediğinizde varsayılan olarak etkindir. Menü çubuğunda, **Araçlar** > **Seçenekler**' i seçerek **hızlı başlatmayı** gösterebilir veya gizleyebilirsiniz. **Ortamlar** düğümünü genişletin ve **Hızlı Başlat**' ı seçin. **Hızlı başlatmayı etkinleştir** onay kutusunu seçin veya temizleyin. Ayrıca, bu sayfada arama kategorilerini etkinleştirebilir veya devre dışı bırakabilirsiniz.

## <a name="category-list"></a>Kategori listesi

Hızlı başlatma arama sonuçları dört kategoride görünür: **En son kullanılanlar**, **menüler**, **Seçenekler**ve **Açık belgeler**, Kategorideki öğelerin sayısı ile birlikte. Arama sonuçlarıyla kategoriye göre geçiş yapmak için, sonraki kategorinin tüm sonuçlarını göstermek üzere **CTRL**+**Q** tuşlarını seçin. Son kategori görüntülendikten sonra, **CTRL**+**Q** her kategoriden birkaç sonuç gösterir. Kategoriler arasında ters sırada gezinmek için **CTRL**+**SHIFT**+**Q** tuşuna basın. Bir kategori altındaki tüm arama sonuçlarını görüntülemek için kategori adını seçin.

Aramanızı belirli kategorilere sınırlamak için aşağıdaki kısayolları kullanabilirsiniz.

|Kategori|Kısayol|Kısayol açıklaması|
|--------------|--------------| - |
|En son kullanılan|@mru<br /><br /> Örneğin, `@mru font`|**En son kullandığınız**öğelerin en fazla beş sayısını görüntüler.|
|Menüler|@menu<br /><br /> Örneğin, `@menu project`|Aramayı menü öğeleriyle sınırlandırır.|
|Seçenekler|@opt<br /><br /> Örneğin, `@opt font`|**Seçenekler** iletişim kutusundaki arama ayarlarını sınırlandırır.|
|Belgeler|@doc<br /><br /> Örneğin, `@doc program.cs`|Arama kriterlerine yönelik açık belgelerin dosya adlarıyla ve yollarına yönelik aramayı kısıtlar, ancak dosyaların içinde metinde arama yapmaz.|

> [!NOTE]
> **Seçenekler** iletişim kutusundaki **genel** > **klavye** sayfasında kısayol tuşlarını değiştirebilirsiniz.

## <a name="show-previous-results"></a>Önceki sonuçları göster

Varsayılan olarak, girdiğiniz arama terimi arama oturumları arasında kalıcı olmaz. Arama dizesi bir terim arıyorsanız, imleci **Hızlı başlatma** alanının dışına taşıyın ve ardından geri dönün. Arama sonuçlarını sürdürmek için **Seçenekler** iletişim kutusuna gidin, **Hızlı Başlat**' ı seçin ve ardından **Hızlı başlatma etkinleştirildiğinde önceki aramadan arama sonuçlarını göster** ' i seçin. onay kutusu. Bir sonraki sefer bir arama yaptığınızda hızlı başlatma alanını bırakın ve geri dönüp, hızlı başlatma en son kullanılan arama terimini korur ve ayrıca arama sonuçlarını gösterir.
