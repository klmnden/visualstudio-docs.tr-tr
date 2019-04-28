---
title: Biçimlendirme seçenekler, metin düzenleyici, XML,
ms.date: 10/29/2018
ms.topic: reference
f1_keywords:
- VS.ToolsOptionsPages.Text_Editor.XML.Formatting
ms.assetid: 203e60b2-7b80-4ff4-9fa1-aa9f4374377b
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: e20b2f7ebe351aa050ea66468fb33aba8e4a31bc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62969273"
---
# <a name="options-text-editor-xml-formatting"></a>Biçimlendirme seçenekler, metin düzenleyici, XML,

Kullanım **biçimlendirme** öğeler ve öznitelikler XML belgelerinizde nasıl biçimlendirileceğini belirtmek için bir seçenekler sayfası. XML biçimlendirme seçenekleri erişmek için kendi seçtikleri **Araçları** > **seçenekleri** > **metin düzenleyici** > **XML**ve ardından **biçimlendirme**.

## <a name="attributes"></a>Öznitelikler

**El ile öznitelik biçimlendirmeyi koru**

Öznitelikleri biçimlendirmez. Bu varsayılan ayardır.

> [!NOTE]
> Öznitelikler üzerinde birden fazla satır varsa, düzenleyici üst öğenin girintisini eşleştirilecek özniteliklerin her satırı girintiler.

**Öznitelikleri her ayrı satıra Hizala**

Dikey olarak ilk öznitelik girintisini eşleştirmek için ikinci ve sonraki öznitelikleri Hizala. Aşağıdaki XML metni nasıl öznitelikleri hizalanmış bir örnektir:

```xml
<item id = "123-A"
      name = "hammer"
      price = "9.95">
</item>
```

## <a name="auto-reformat"></a>Otomatik yeniden Biçimlendir

**Pano'dan üzerinde Yapıştır**

Panodan yapıştırılan XML metin biçimlendirmesi.

**Bitiş etiketi tamamlandığında**

Öğe bitiş etiketi tamamlandığında yeniden biçimlendirin.

## <a name="mixed-content"></a>Karışık içerik

**Varsayılan olarak karışık içeriği biçimlendirin.**

Zaman içinde içerik bulunana dışında karışık içerik, yeniden biçimlendirme girişiminde bir `xml:space="preserve"` kapsam. Bu varsayılan ayardır.

Bir öğe metni ve biçimlendirmeyi bir karışımını içeriyorsa, içeriği içerik karışık kabul edilir. Karışık içerikli bir öğenin bir örneği verilmiştir.

```xml
<dir>c:\data\AlphaProject\
  <file readOnly="false">test1.txt</file>
  <file readOnly="false">test2.txt</file>
</dir>
```

## <a name="see-also"></a>Ayrıca bkz.

- [XML seçenekleri - diğer](options-text-editor-xml-miscellaneous.md)
- [Visual Studio'daki XML araçları](../../xml-tools/xml-tools-in-visual-studio.md)