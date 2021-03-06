---
title: Araç Kutusu, HTML Sekmesi
ms.date: 06/21/2017
ms.topic: reference
f1_keywords:
- vs.toolbox.html
helpviewer_keywords:
- Toolbox, HTML tab
- HTML Designer, setting options
- HTML tab in Toolbox
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 72492b984e7f47b87ea326fe8ebcce414ee978ec
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926055"
---
# <a name="toolbox-html-tab"></a>Araç kutusu, HTML sekmesi

Araç kutusunun **HTML** sekmesi, Web sayfaları ve Web formlarında yararlı olan bileşenleri sağlar. Bu sekmeyi görüntülemek için önce HTML tasarımcısında düzenlenecek bir belgeyi açın. **Görünüm** menüsünde, **araç kutusu**' na tıklayın ve ardından araç kutusunun **HTML** sekmesine tıklayın.

**HTML** sekmesinde bir aracın örneğini oluşturmak için araca çift tıklayarak geçerli ekleme noktasındaki belgenize ekleyin ya da aracı seçin ve düzen yüzeyi üzerinde istediğiniz konuma sürükleyin.

## <a name="ui-elements"></a>UI öğeleri

Aşağıdaki araçlar HTML sekmesinde varsayılan olarak kullanılabilir.

**Çağrısı**

![ASP.NET Mobile Designer HTMLpage Işaretçisi](../../ide/reference/media/vxpointer.gif)

Araç kutusu sekmesi açıldığında bu araç varsayılan olarak seçilidir. Silinemez. İşaretçi, nesneleri Tasarım görünümü yüzeyi üzerine sürüklemenize, yeniden boyutlandırmanıza ve sayfa ya da form üzerinde yeniden konumlandırmanıza olanak sağlar. Daha fazla bilgi için [araç kutusu](../../ide/reference/toolbox.md).

**Giriş (düğme)**

![HTML Web sayfası düğmesi](../../ide/reference/media/vxbutton.gif)

`input` Öğesi`type="button"`ekler. Görüntülenen metni değiştirmek için, `name` özelliğini düzenleyin. Varsayılan olarak, `id="Button1"` ilk `id="Button2"` düğme için, ikincisi, vb. için eklenmiştir.

**Giriş (düğme)** Tasarım görünümü yüzeyine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Button1" type="button" value="Button" name="Button1">
```

**Giriş (sıfırlama)**

![HTMLpageResetButton ekran görüntüsü](../../ide/reference/media/vxreset.gif)

`input` Öğesi`type="reset"`ekler. Görüntülenen metni değiştirmek için, `name` özelliğini düzenleyin. Varsayılan olarak, `id="Reset1"` ilk sıfırlama `id="Reset2"` düğmesine, ikincisi için eklenir ve bu şekilde devam eder.

**Girişi (sıfırlama)** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Reset1" type="reset" value="Reset" name="Reset1">
```

**Giriş (Gönder)**

![HTMLpageToolbarSubmitButton ekran görüntüsü](../../ide/reference/media/vxsubmit.gif)

`input` Öğesi`type="submit"`ekler. Görüntülenen metni değiştirmek için, `name` özelliğini düzenleyin. Varsayılan olarak, `id="Submit1"` ilk gönder `id="Submit2"` düğmesine, ikincisi için eklenir ve bu şekilde devam eder.

**Girişi (Gönder)** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Submit1" type="submit" value="Submit" name="Submit1">
```

**Giriş (metin)**

![HTMLpageToolbarTextField ekran görüntüsü](../../ide/reference/media/vxtextfield.gif)

Belgenize bir `input` `type="text"` öğesi ekler. Görüntülenen varsayılan metni değiştirmek için `value` özniteliği düzenleyin. Varsayılan olarak, `id="Text1"` ikinci `id="Text2"` için ilk metin alanı için eklenir ve bu şekilde devam eder.

**Girişi (metin)** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Text1" TYPE="text" value="Text Field" name="Text1">
```

> [!IMPORTANT]
>Tüm Kullanıcı girişlerini doğrulamanız önerilir. Daha fazla bilgi için bkz. [ASP.NET Web Pages (Razor) sitelerindeki kullanıcı girişini doğrulama](/aspnet/web-pages/overview/ui-layouts-and-themes/validating-user-input-in-aspnet-web-pages-sites).

**Giriş (dosya)**

![HTML sayfa dosyası alanı](../../ide/reference/media/vxfilefield.gif)

Belgenize bir `input` `type="file"` öğesi ekler. Varsayılan olarak, `id="File1"` ikinci `id="File2"` için ilk dosya alanı için eklenir ve bu şekilde devam eder.

**Giriş (dosya)** Tasarım görünümü yüzeyine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="File1" type="file" name="File1">
```

> [!IMPORTANT]
> Tüm Kullanıcı girişlerini doğrulamanız önerilir. Daha fazla bilgi için bkz. [ASP.NET Web Pages (Razor) sitelerindeki kullanıcı girişini doğrulama](/aspnet/web-pages/overview/ui-layouts-and-themes/validating-user-input-in-aspnet-web-pages-sites).

**Giriş (parola)**

![Visual Studio parolası alanı](../../ide/reference/media/vxpassword.gif)

`input` Öğesi`type="password"`ekler. Varsayılan olarak, `id="Password1"` ilk parola `id="Password2"` alanı için, ikincisi için eklenir ve bu şekilde devam eder.

**Giriş (parola)** Tasarım görünümü yüzeyine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Password1" type="password" name="Password1">
```

> [!IMPORTANT]
> Uygulamanız kullanıcı adlarını ve parolaları iletitirse, Web sitenizi, iletimi şifrelemek için Güvenli Yuva Katmanı (SSL) kullanacak şekilde yapılandırmanız gerekir. Daha fazla bilgi için bkz. [bağlantıları güvenli hale getirme](/previous-versions/tn-archive/bb418917(v=technet.10)). Ayrıca, tüm kullanıcı girişlerini doğrulamanız önerilir. Daha fazla bilgi için bkz. [ASP.NET Web Pages (Razor) sitelerindeki kullanıcı girişini doğrulama](/aspnet/web-pages/overview/ui-layouts-and-themes/validating-user-input-in-aspnet-web-pages-sites).

**Giriş (onay kutusu)**

![HTML Web sayfası araç kutusu seçeneği](../../ide/reference/media/vxcheckbox.gif)

`input` Öğesi`type="checkbox"`ekler. Görüntülenen metni değiştirmek için, `name` özelliğini düzenleyin. Varsayılan olarak, `id="Checkbox1"` ilk onay `id="Checkbox2"` kutusu için, ikincisi için eklenmiştir ve bu şekilde devam eder.

**Girişi (onay kutusu)** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Checkbox1" type="checkbox" name="Checkbox1">
```

**Giriş (radyo)**

![VisualStudioHTMLpageRadioButton ekran görüntüsü](../../ide/reference/media/vxradio.gif)

`input` Öğesi`type="radio"`ekler. Görüntülenen metni değiştirmek için, `name` özelliğini düzenleyin. Varsayılan olarak, `id="Radio1"` ilk radyo `id="Radio2"` düğmesine, ikincisi için eklenir ve bu şekilde devam eder.

**Girişi (radyo)** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Radio1" type="radio" name="Radio1">
```

**Giriş (gizli)**

![HTML sayfası gizli öğesi](../../ide/reference/media/vxhidden.gif)

`input` Öğesi`type="hidden"`ekler. Varsayılan olarak, `id="Hidden1"` ilk gizli `id="Hidden2"` alan için, ikincisi için eklenir ve bu şekilde devam eder.

**Girişi (gizli)** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<input id="Hidden1" type="hidden" name="Hidden1">
```

**Metin Alanı**

![HTMLpage araç çubuğu metin alanı](../../ide/reference/media/vxtextarea.gif)

Bir `textarea` öğesi ekler. Metin alanını yeniden boyutlandırabilir veya görüntüleme alanının ötesinde genişleyen metni görüntülemek için kaydırma çubuklarını kullanabilirsiniz. Görüntülenen varsayılan metni değiştirmek için `value` özniteliği düzenleyin. Varsayılan `id="textarea1"` olarak, ikinci `id=" textarea 2"` için ilk metin alanı eklenir ve bu şekilde devam eder.

**Textarea** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, belgenize AŞAĞıDAKI gibi HTML biçimlendirmesi eklenir:

```html
<textarea id=" textarea 1 name=" textarea 1" rows=2 cols=20></textarea>
```

> [!IMPORTANT]
> Tüm Kullanıcı girişlerini doğrulamanız önerilir. Daha fazla bilgi için bkz. [ASP.NET Web Pages (Razor) sitelerindeki kullanıcı girişini doğrulama](/aspnet/web-pages/overview/ui-layouts-and-themes/validating-user-input-in-aspnet-web-pages-sites).

**Tablo**

![HTMLpageToolbarTable ekran görüntüsü](../../ide/reference/media/vxtable.gif)

Bir `table` öğesi ekler.

**Tabloyu** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, belgenize AŞAĞıDAKI gibi HTML biçimlendirmesi eklenir:

```html
<table cellspacing="1" width="75%" border=1> <tr><td></td></tr></table>
```

**Görüntü**

![HTML sayfası resim öğesi](../../ide/reference/media/vximage.gif)

Bir `img` öğesi ekler. `src` Kendi`alt` metnini belirtmek için bu öğeyi düzenleyin.

**Görüntüyü** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, belgenize AŞAĞıDAKI gibi HTML biçimlendirmesi eklenir:

```html
<img alt="" src="">
```

**Seçin**

![HTML sayfası araç kutusu açılan kutusu](../../ide/reference/media/vxdropdown.gif)

Bir açılan `select` öğe ekler ( `size` özniteliği olmadan). Varsayılan olarak, `id="select1"` ilk liste `id="select2"` kutusu için, ikinci için eklenmiştir ve bu şekilde devam eder.

**Seçimi** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, belgenize AŞAĞıDAKILER gibi HTML biçimlendirmesi eklenir:

```html
<select id="select1" name="select1"><option selected></option></select>
```

Boyut özelliğinin değerini artırarak çok satırlı `select` bir öğe oluşturabilirsiniz.

**Yatay kural**

![HTML sayfası yatay kural öğesi](../../ide/reference/media/vxhorizontal.gif)

Bir `hr` öğesi ekler. Çizginin kalınlığını artırmak için `size` özniteliği düzenleyin.

**Yatay kuralı** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, AŞAĞıDAKI gibi HTML biçimlendirmesi belgenize eklenir:

```html
<hr width="100%" size=1>
```

**DIV**

![HTML sayfa etiketi](../../ide/reference/media/vxlabel.gif)

Özniteliği içeren bir `div` öğesi ekler. `ms_positioning="FlowLayout"` Genişlik ve Yükseklik dışında, bu öğe bir akış düzeni paneliyle aynıdır. `div` Öğe içinde bulunan metni biçimlendirmek için, açma etiketine bir `class="stylename"` öznitelik ekleyin.

**Div** Tasarım görünümü yüzeyi üzerine sürüklediğinizde, belgenize AŞAĞıDAKI gibi HTML biçimlendirmesi eklenir:

```html
<div ms_positioning="FlowLayout" style="width: 70px; position: relative; height: 15px">Label</div>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Araç Kutusu](../../ide/reference/toolbox.md)
