---
title: Biçimlendirme, XML, Metin Düzenleyici, Seçenekler İletişim Kutusu
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
ms.assetid: bb539b3a-027c-4b2f-906e-403e0e22ba8d
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 05ddfcb0613dac08fb6e4323062f87475bd8f0d1
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53938598"
---
# <a name="formatting-xml-text-editor-options-dialog-box"></a>Biçimlendirme, XML, metin düzenleyici, Seçenekler iletişim kutusu

Bu iletişim kutusu, XML Düzenleyicisi için biçimlendirme ayarları belirtmenize olanak sağlar. Erişebildiğiniz **seçenekleri** iletişim kutusundan **Araçları** menüsü.

> [!NOTE]
> Seçtiğinizde, bu ayarlar kullanılabilir **metin düzenleyici** klasöründe **XML** klasörünü ve ardından **biçimlendirme** seçeneğini **seçenekleri** iletişim kutusu.

## <a name="attributes"></a>Öznitelikler
 **El ile öznitelik biçimlendirmeyi koru**

 Öznitelikleri getirilecek değil. Bu varsayılandır.

> [!NOTE]
> Öznitelikler üzerinde birden fazla satır varsa, düzenleyici üst öğenin girintisini eşleştirilecek özniteliklerin her satırı girintiler.

 **Öznitelikleri her biri kendi satırında Hizala**

 Dikey olarak ilk öznitelik girintisini eşleştirmek için ikinci ve sonraki öznitelikleri hizalar. Aşağıdaki XML nasıl öznitelikleri hizalanmış bir örnek metindir.

```xml
<item id = "123-A"
      name = "hammer"
      price = "9.95">
</item>
```

## <a name="auto-reformat"></a>Otomatik yeniden Biçimlendir
 **Panodan yapıştırma**

 XML metni panodan yapıştırılan yeniden biçimlendirir.

 **Bitiş etiketi tamamlandığında**

 Öğe bitiş etiketi tamamlandığında yeniden biçimlendirir.

## <a name="mixed-content"></a>Karışık içerik
 **Varsayılan olarak karışık içeriği korumak**

 Düzenleyici karışık içerik yeniden biçimlendirir olup olmadığını belirler. Varsayılan olarak, düzenleyici içeriği ne zaman bulunur dışında karışık içeriği yeniden biçimlendirmek çalışır. bir `xml:space="preserve"` kapsam.

 Bir öğe metni ve biçimlendirmeyi bir karışımını içeriyorsa, içeriği içerik karışık kabul edilir. Karışık içerikli bir öğenin bir örnek verilmiştir.

```xml
<dir>c:\data\AlphaProject\
  <file readOnly="false">test1.txt</file>
  <file readOnly="false">test2.txt</file>
</dir>
```

## <a name="see-also"></a>Ayrıca bkz.

- [XML belge özellikleri, özellik penceresi](../xml-tools/xml-document-properties-properties-window.md)
- [XML Düzenleyicisi bileşenleri](../xml-tools/xml-editor-components.md)