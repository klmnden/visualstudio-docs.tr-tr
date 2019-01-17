---
title: Seçenekler, metin düzenleyici, HTML biçimlendirmeyi (Web Forms)
ms.date: 1/15/2019
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.HTML_(Web_Forms).Formatting
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 64a8ad0e4b0c4f8b7c955bd11a69ef8a9e9d81d7
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54350177"
---
# <a name="options-text-editor-html-web-forms-formatting"></a>Seçenekler, metin düzenleyici, HTML biçimlendirmeyi (Web Forms)

Kullanım **biçimlendirme** seçenekler sayfası, Kod Düzenleyicisi'nde kod biçimlendirme için HTML proje seçeneklerini ayarlamak için. Menü çubuğunda, bu sayfaya erişmek için seçin **Araçları** > **seçenekleri**ve ardından **metin düzenleyici** > **HTML (Web Forms)**   >  **Biçimlendirme**.

## <a name="capitalization"></a>Büyük/küçük harf

Bu seçenek seçildiğinde, kaynak görünümü ve XML Düzenleyicisi varsayılan büyük/küçük harf biçimi adlarını öğeleri ve özniteliklerinin öğeleri ilk oluşturulduğunda ve otomatik biçimlendirme sırasında uygulanır. **Otomatik biçimlendirme uygulamak** ayarlarını belirleme zamanı hangi otomatik biçimlendirme geçerli olur.

> [!WARNING]
> XML büyük/küçük harf duyarlıdır. XML çözümleyicileri varsayılan durumu ayarını etkiler.

### <a name="uielement-list"></a>UIElement listesi

**Sunucu etiketi, sunucu öznitelikleri**

Bu seçenekler, Web sunucusu denetimi için biçimlendirme büyük harfle nasıl belirtin.

|Seçenek|Sonuç|
|---------------------------------|------------------------------|
|**Girildiği gibi**|Tam olarak girerken öğesi durumdur.|
|**büyük harf**|Öğe adları için büyük harf biçimlendirilir.|
|**Küçük**|Öğe adlarının küçük harfe biçimlendirilir.|
|**Derleme tanımı**|Öğe durumu, öğenin karşılık gelen türü sınıfında nasıl tanımlandığını tarafından belirlenir.|


**İstemci etiketi, istemci öznitelikleri**

Bu seçenekler otomatik biçimlendirme HTML özniteliklerini ve özellikleri için büyük harf veya küçük adlarını değiştirir veya girildiği gibi tutar olup olmadığını belirtin.

|Seçenek|Sonuç|
|---------------------------------|------------------------------|
|**Girildiği gibi**|Tam olarak girerken, öznitelik durumdur.|
|**büyük harf**|Öznitelik adları büyük harfe biçimlendirilir.|
|**Küçük**|Öznitelik adları küçük harf olarak biçimlendirilir.|


## <a name="automatic-formatting-options"></a>Otomatik biçimlendirme seçenekleri

Bu seçenekler eklemek veya otomatik biçimlendirme sırasında fiziksel satır sonlarını kaldırmanız kaynak görünümü Düzenleyicisi neden. Düzenleyici öznitelikleri tırnak ekler olup olmadığını belirtebilirsiniz.

> [!NOTE]
> Bu ayarlar, boşluk XML biçimlendirmesi içinde değiştirmeyin.

### <a name="uielement-list"></a>UIElement listesi

- **Yazma sırasında öznitelik değer tırnakları Ekle**

   Bu seçenek belirlendiğinde, siz yazarken Düzenleyicisi'ni otomatik olarak öznitelikleri etrafında tırnak işareti koyar (örneğin: KİMLİK = "Select1"). Tırnak işaretleri, bir biçimlendirme el ile eklemek isterseniz bu seçeneği temizleyin.


   > [!NOTE]
   > Bu seçenek belirlendiğinde olsun veya olmasın, tüm mevcut tırnak işaretleri, biçimlendirmede korunur; tırnak işaretleri hiçbir zaman kaldırılır.

- **Biçimlendirme sırasında öznitelik değer tırnakları Ekle**

   Bu seçenek belirlendiğinde, öznitelik değerleri çift tırnak otomatik biçimlendirme ekler (örneğin: KİMLİK = "Select1").

   > [!NOTE]
   > Bu seçenek belirlendiğinde olsun veya olmasın, tüm mevcut tırnak işaretleri, biçimlendirmede korunur.

- **Kapatma etiketlerini otomatik olarak Ekle**

   Bu seçenek belirlendiğinde, Düzenleyici bir kapatma etiketi otomatik olarak oluşturur. (örneğin,  **\</b >**) açılış etiketinde kapattığınızda.

## <a name="tag-wrapping"></a>Etiket kaydırma

Bu seçenekler, belirli bir süre gitmeleri Düzenleyicisi etiketleri satırlarına keser olup olmadığını belirler.

### <a name="uielement-list"></a>UIElement listesi

- **Belirtilen uzunluk aşıldığında etiketleri Kaydır**

   Etiket, belirttiğiniz uzunluğu dışında kalırsa seçili olduğunda, düzenleyici etiketleri satıra ayırır. **uzunluğu** metin kutusu. Bu işlem, yeni bir etiket yazarken değil yalnızca etiketi biçimlendirme sırasında oluşur.

   > [!NOTE]
   > Belirttiğiniz değer, en az bir değer olarak kullanılır. Düzenleyici, tek tek nitelikler kesmez.

- **Uzunluğu**

   Bir satır kaydırma görüntülemek için karakter sayısını belirtir. Bu giriş kutusunu sürece devre dışıdır **kaydırma belirtilen uzunluk aşıldığında etiketleri** kutunun işaretli.

- **Etikete özgü seçenekler**

   Görüntüler **etikete özgü seçenekler** sağlayan iletişim kutusunda, tek etiket veya etiketleri grupları için biçimlendirme seçeneklerini ayarlayın.

## <a name="see-also"></a>Ayrıca bkz.

- [Genel, Ortam, Seçenekler İletişim Kutusu](../../ide/reference/general-environment-options-dialog-box.md)