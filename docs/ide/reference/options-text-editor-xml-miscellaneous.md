---
title: Seçenekler, metin düzenleyici, çeşitli XML
ms.date: 10/29/2018
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.XML.Miscellaneous
ms.assetid: b6538cbe-badd-4313-a1fb-39e906736bbe
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: d3421580251a6a871adba311fd609e881e088ebd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969221"
---
# <a name="options-text-editor-xml-miscellaneous"></a>Seçenekler, metin düzenleyici, çeşitli XML

Kullanım **çeşitli** otomatik tamamlama ve şema XML Düzenleyicisi ayarları değiştirmek için seçenekler sayfası. Diğer XML Seçenekleri erişmek için kendi seçtikleri **Araçları** > **seçenekleri** > **metin düzenleyici** > **XML**ve ardından **çeşitli**.

## <a name="auto-insert"></a>Otomatik Ekle

**Kapatma etiketleri**

Metin düzenleyici, XML öğeleri yazarken kapatma etiketleri ekler. Bir öğenin başlangıç etiketinde seçtiyseniz, düzenleyici eşleşen bir ad alanı öneki de dahil olmak üzere eşleşen bir kapatma etiketi ekler. Bu onay kutusu varsayılan olarak seçilidir.

**Öznitelik tırnak işaretleri**

XML öznitelikleri yazarken, düzenleyici ekler `="` ve `"` giriş işaretini yerleştirir ve karakter (**^**) tırnak işaretleri. Bu onay kutusu varsayılan olarak seçilidir.

**Namespace bildirimi**

Gerekli olurlarsa olsunlar Düzenleyicisi ad alanı bildirimi otomatik olarak ekler. Bu onay kutusu varsayılan olarak seçilidir.

**Diğer işaretlemeler (açıklamalar, CDATA)**

Açıklamalar, CDATA, DOCTYPE, işleme yönergeleri ve diğer biçimlendirme, otomatik tamamlanan içindir. Bu onay kutusu varsayılan olarak seçilidir.

## <a name="network"></a>Ağ

**Otomatik olarak indirilen DTD'ler ve şemalar indir**

Şemaları ve belge türü tanımları (DTD'ler), HTTP konumlardan otomatik olarak yüklenir. Bu özellik etkin autoproxy sunucu algılaması System.Net kullanır. Bu onay kutusu varsayılan olarak seçilidir.

## <a name="outlining"></a>Anahat Oluşturma

**Dosyalar açıldığında anahat moduna gir**

Bir dosya açıldığında anahat oluşturma özelliğini etkinleştirir. Bu onay kutusu varsayılan olarak seçilidir.

## <a name="caching"></a>Önbelleğe Alma

**Şemaları**

Şema önbelleği konumunu belirtir. **Gözat** düğmesi geçerli şema önbellek konumunda yeni bir pencerede açar. Varsayılan konum *%VsInstallDir%\xml\Schemas*.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Seçenekleri - biçimlendirme](options-text-editor-xml-formatting.md)
- [Visual Studio'daki XML araçları](../../xml-tools/xml-tools-in-visual-studio.md)