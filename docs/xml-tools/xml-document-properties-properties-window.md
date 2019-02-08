---
title: XML Belge Özellikleri, Özellik Penceresi
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 9dbb34d9-02ea-4201-b445-c98a0eb0d6db
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 69cd8a8f1acd650c65c995f303adc4d3ee2c1bc5
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55938253"
---
# <a name="xml-document-properties-properties-window"></a>XML belge özellikleri, özellik penceresi

**Özellikleri** penceresi XML Düzenleyicisi'nde etkin belgeyi hakkında temel bilgiler sağlar. Kullanılabilir özellikler şu anda etkin olan bir XML belgesi türüne bağlı olarak değişir.

> [!NOTE]
> Çözümdeki tüm XML belge özellikleri kaydedilir. Sonuç olarak, çözüm bir sonraki açışınızda bu değerleri girmek gerekmez.

 **Kodlama**

 Dosya için kodlama karakter. Bu özellik değişiklikleri kodlama özniteliği XML bildirimi ve tam tersi de değiştiriliyor. Yeni kodlama dosyasını kaydettiğinizde dosyanın kodlamak için kullanılır.

 **Giriş**

 XSLT stil sayfası ile ilişkili giriş belgesi. Tarafından kullanılan **ShowXSLT çıkış** komutu. Gözat'ı kullanarak bir belge seçilebilir (**...** ) düğmesi.

 Bu özellik, yalnızca bir XSLT dosyası düzenleyici penceresinde şu anda etkin olduğunda görülebilir.

 **Output**

 XML belge dönüştürme çalıştırdığınızda oluşturulan dosya.

 Bir dosya belirtilmezse, varsayılan dosya adı temel alınarak oluşturulur `method` özniteliği `xsl:output` öğesinin dosya uzantısı belirler. Varsayılan dosya, geçerli kullanıcının geçici dizininde bulunur.

 **Şemaları**

 Doğrulama yapmak için kullanılan şemalar. Düğme açar **XSD şemaları** iletişim kutusunda, kullanılacak şemaları seçmek için kullanılabilir.

 Şema yolunu da girebilirsiniz. Birden çok şema belirtilmezse, her şema çift tırnak içine alınmalıdır.

 **Stil sayfası**

 Belgeyi dönüştürmek için kullanılan XSLT dosyası olduğunda **XSLT çıktıyı Göster** komutu kullanılır. Bu alan boşsa, **XSLT çıktıyı Göster** komutu kullanıldığında, sağlanan değer Düzenleyicisi kullanan `xml-stylesheet` işleme yönergesi belge veya sizden için dosya adı.

 Farklı bir stil sayfası olması gerektiğini belirtmek için bir XSLT dosyası düzenlenirken, bu özellik kullanılabilir olduğunda kullanılabilir **XSLT çıktıyı Göster** veya **XSLT hata ayıklama** komut seçili. Örneğin, bir üst stil sayfasında bulunan bir stil sayfası düzenlerken bunu yapmak isteyebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)
- [XML Düzenleyicisi bileşenleri](../xml-tools/xml-editor-components.md)