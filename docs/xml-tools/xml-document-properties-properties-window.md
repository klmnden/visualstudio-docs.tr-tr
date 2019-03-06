---
title: XML Belge Özellikleri, Özellik Penceresi
ms.date: 03/05/2019
ms.topic: reference
ms.assetid: 9dbb34d9-02ea-4201-b445-c98a0eb0d6db
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 679ac529708a49d18025672ce8f880c4f7710471
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526275"
---
# <a name="xml-document-properties-properties-window"></a>XML belge özellikleri, özellik penceresi

**Özellikleri** penceresi XML Düzenleyicisi'nde etkin belgeyi hakkında temel bilgiler sağlar. Kullanılabilir özellikler şu anda etkin olan bir XML belgesi türüne bağlı olarak değişir.

> [!NOTE]
> Çözümdeki tüm XML belge özellikleri kaydedilir. Sonuç olarak, çözüm bir sonraki açışınızda bu değerleri girmek gerekmez.

**Kodlama**

Dosya için kodlama karakter. Bu özellik değişiklikleri kodlama özniteliği XML bildirimi ve tam tersi de değiştiriliyor. Yeni kodlama dosyasını kaydettiğinizde dosyanın kodlamak için kullanılır.

**Giriş**

XSLT stil sayfası ile ilişkili giriş belgesi. Tarafından kullanılan **Başlat XSLT** komutlar, örneğin, **XML** > **XSLT hata ayıklama olmadan Başlat**. Gözat'ı kullanarak bir belge seçilebilir (**...** ) düğmesi.

Bu özellik, yalnızca bir XSLT dosya düzenleyicide açıkken görülebilir.

**Output**

XML belge dönüştürme çalıştırdığınızda oluşturulan dosya.

Bir dosya belirtilmezse, varsayılan dosya adı temel alınarak oluşturulur `method` özniteliği `xsl:output` öğesinin dosya uzantısı belirler. Varsayılan dosya, geçerli kullanıcının geçici dizininde bulunur.

**Şemaları**

Doğrulama yapmak için kullanılan şemalar. Düğme açar **XSD şemaları** iletişim kutusunda, kullanılacak şemaları seçmek için kullanılabilir.

Şema yolunu da girebilirsiniz. Birden çok şema belirtilmezse, her şema çift tırnak içine alınmalıdır.

**Stil sayfası**

Belgeyi dönüştürmek için kullanılan XSLT dosyası olduğunda **XSLT hata ayıklamayı Başlat** ve **XSLT hata ayıklama olmadan Başlat** komutları kullanılır. Bu alan boş bırakılırsa, sağlanan değer Düzenleyicisi kullanan `xml-stylesheet` işleme yönergesi belgenin veya sizden için bir dosya adı.

Farklı bir stil sayfası olması gerektiğini belirtmek için bir XSLT dosyası düzenlenirken, bu özellik kullanılabilir olduğunda kullanılabilir **XSLT hata ayıklamayı Başlat** veya **XSLT hata ayıklama olmadan Başlat** seçili komutu. Örneğin, bir üst stil sayfasında bulunan bir stil sayfası düzenlerken bunu yapmak isteyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)