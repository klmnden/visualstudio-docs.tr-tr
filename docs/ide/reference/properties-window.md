---
title: Özellikler Penceresi
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- properties [Visual Studio], Properties Window
- handler functions, Properties window
- handlers, Properties window
- Windows messages
- properties [Visual Studio], setting at design time
- properties [Visual Studio], editing
- Property Browser
- Windows messages, adding message handlers
- Properties window, overrides
- virtual functions, Properties window
- Properties window
ms.assetid: e6e0fa4f-75c4-4a52-af15-281cd61876ca
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e26bd9d874ba5526a858e32907bff6676b68c81e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969039"
---
# <a name="properties-window"></a>Özellik penceresi

Tasarım zamanı özelliklerini ve düzenleyicilerde ve tasarımcılarda bulunan seçilen nesnelerin olaylarını görüntülemek ve değiştirmek için bu pencereyi kullanın. Ayrıca **özellikleri** düzenlemek ve dosya, proje ve çözüm özelliklerini görüntülemek için penceresi. Bulabilirsiniz **özellikleri** penceresinde **görünümü** menüsü. Ayrıca tuşlarına basarak açabilirsiniz **F4** veya yazarak **özellikleri** arama kutusuna.

**Özellikleri** farklı tür alanları, belirli bir özelliğin gereksinimlerine bağlı olarak düzenleme penceresinde görüntülenir. Bu düzenleme alanları düzenleme kutuları, açılan listeler ve özel Düzenleyici iletişim kutularına bağlantılar içerir. Gri renkle gösterilen özellikler salt okunurdur.

## <a name="uielement-list"></a>UIElement Listesi

Nesne name\
Seçili nesneyi ya da nesneleri listeler. Sadece aktif Düzenleyici veya tasarımcı nesnelerden görülebilir. Birden çok nesne seçtiğinize, yalnızca seçilen tüm nesneler için ortak olan özellikler görünür.

Categorized\
Kategoriye göre tüm özellikleri ve seçili nesne için özellik değerlerini listeler. Görünür özelliklerin sayısını azaltmak için bir kategoriyi daraltabilirsiniz. Genişlet veya daralt bir kategori artı görürsünüz (+) veya eksidir (–) sol tarafındaki kategori adı. Kategoriler alfabetik olarak listelenir.

Alphabetical\
Tüm tasarım zamanı özelliklerini ve seçilen nesnelerin olaylarını alfabetik olarak sıralar. Soluklaşmamış bir özelliği düzenlemek için sağındaki hücreyi tıklatın ve değişiklikleri girin.

Özellik Sayfaları\
Görüntüler **özellik sayfaları** iletişim kutusu veya **Proje Tasarımcısı** seçili öğe için. Özellik sayfaları görüntüler bir alt kümesini aynısını veya bulunan özelliklerin bir alt kümesi **özellikleri** penceresi. Projenizin etkin yapılandırması ile ilgili özellikleri görüntülemek ve düzenlemek için bu düğmeyi kullanın.

Properties\
Bir nesne için özellikleri görüntüler. Çok sayıda nesne kullanılarak görüntülenebilen olayları de **özellikleri** penceresi.

Özellik Source\ göre sırala
Stiller ve bağlamalar gibi devralma, bir kaynağa göre özellikleri gruplandırır uygulanır. Yalnızca tasarımcıdaki XAML dosyaları düzenlerken kullanılabilir.

Events\
Bir nesne için olayları görüntüler.

> [!NOTE]
> Bu **özellikleri** penceresi araç çubuğu denetimi yalnızca yok bir form veya Denetim Tasarımcısı olduğunda bağlamında etkin bir [!INCLUDE[csprcs](../../data-tools/includes/csprcs_md.md)] proje. XAML dosyalarını düzenlerken, olaylar Özellikler penceresinin ayrı bir sekmede görünür.

Messages\
Tüm Windows iletilerini listeler. Ekleme veya silme seçilen sınıf için sağlanan iletilerin belirtilen işleyici işlevlerini sağlar.

> [!NOTE]
> Bu **özellikleri** penceresi araç çubuğu denetimi yalnızca kullanılabilir olduğunda **sınıf görünümü** bağlamında etkin pencere bir [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] proje.

Overrides\
Seçilen sınıf için tüm sanal işlevleri listeler ve ekleme veya silmeyi geçersiz kılma işlevleri sağlar.

> [!NOTE]
> Bu **özellikleri** penceresi araç çubuğu denetimi yalnızca kullanılabilir olduğunda **sınıf görünümü** bağlamında etkin pencere bir [!INCLUDE[vcprvc](../../code-quality/includes/vcprvc_md.md)] proje.

Açıklama pane\
Özellik türünü ve özelliğin kısa bir açıklamasını gösterir. Ve kısayol menüsünden Açıklama komutunu kullanarak özelliğin açıklamasını kapatabilirsiniz.

> [!NOTE]
> Bu **özellikleri** penceresi araç çubuğu denetimi kullanılamıyor tasarımcıdaki XAML dosyaları düzenlerken.

Küçük resim view\
Seçili olan öğenin görsel bir temsilini tasarımcıdaki XAML dosyaları düzenlerken gösterir.

Search\
Özellikler ve tasarımcıdaki XAML dosyaları düzenlerken olaylar için bir arama işlevi sağlar. Arama kutusuna, kısmi sözcük aramalarına yanıt verir ve siz yazarken arama sonuçlarını güncelleştirir.

## <a name="see-also"></a>Ayrıca bkz.

- [Proje Özellikleri Başvurusu](../../ide/reference/project-properties-reference.md)
- [Pencere düzenlerini özelleştirme](../../ide/customizing-window-layouts-in-visual-studio.md)