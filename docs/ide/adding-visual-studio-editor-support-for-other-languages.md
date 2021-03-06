---
title: Diğer diller için düzenleyici desteği eklendi
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- syntax colorization
- IntelliSense
- IDE, navigation
- documents [Visual Studio], navigation
- TextMate bundle
- TextMate language grammar
- language support
ms.assetid: d78c43ee-4ef2-42e5-984e-d137de4e7e92
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7ae0b2f606b4fe04ad390712f48ac1e06ff9bb86
ms.sourcegitcommit: 283f2dbce044a18e9f6ac6398f6fc78e074ec1ed
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/16/2019
ms.locfileid: "65805321"
---
# <a name="add-visual-studio-editor-support-for-other-languages"></a>Diğer diller için Visual Studio Düzenleyicisi desteği Ekle

Okuma ve farklı bir bilgisayara dil arasında gezinme Visual Studio Düzenleyicisi'ni nasıl destekler ve diğer diller için Visual Studio Düzenleyicisi desteği nasıl ekleyebileceğinizi öğrenin.

## <a name="syntax-colorization-statement-completion-and-navigate-to-support"></a>Söz dizimi renklendirme ve deyim tamamlama gitmek için destek

Visual Studio Düzenleyicisi söz dizimi renklendirme, deyim tamamlama (IntelliSense olarak da bilinir) gibi özellikleri ve _gitmek için_ daha kolayca yazma, okuma ve kodunuzu düzenleyin yardımcı olabilir. Aşağıdaki ekran görüntüsünde, Perl komut dosyasını Visual Studio'da düzenleme bir örnek gösterilmektedir. Söz dizimi, otomatik olarak renklendirilir. Örneğin, kod içindeki açıklamalar yeşil renktedir kodudur siyah yolları kırmızı ve deyimleri mavi. Visual Studio Düzenleyicisi söz dizimi renklendirme desteklediği herhangi bir dil için otomatik olarak uygular. Ayrıca, bilinen dil anahtar sözcüğü veya nesne girmeye başladığınızda, deyim tamamlama olası deyimleri ve nesnelerin bir listesini görüntüler. Deyim tamamlama daha hızlı ve kolay bir şekilde kod yazmanıza yardımcı olabilir.

![Perl komut söz dizimi renklendirme](../ide/media/vside_perledit.png)

Visual Studio şu anda sağlar söz dizimi renklendirme ve temel deyim tamamlama desteği aşağıdaki dillerde kullanarak [TextMate dil bilgileri](https://manual.macromates.com/en/language_grammars). Favori dilinizi tabloda yoksa, endişelenmeyin&mdash;ekleyebilirsiniz.

|||||||
|-|-|-|-|-|-|
|BAT|F#|Java|Markdown|Rust|Visual Basic|
|Clojure|Git|JavaDoc|Objective-C|ShaderLab|C#|
|CMake|Groovy|JSON|Perl|ShellScript|Visual C++|
|CoffeeScript|HTML|DAHA AZ|Python|SQL|VBNet|
|CSS|INI|LUA|R|Swift|XML|
|Docker|Jade|Marka|Ruby|TypeScript|YAML|

Söz dizimi renklendirme ve temel deyim tamamlama ek olarak, Visual Studio de denilen bir özelliği olan [gitmek için](https://blogs.msdn.microsoft.com/benwilli/2015/04/09/visual-studio-tip-3-use-navigate-to/). Bu özellik, hızla kod dosyaları, dosya yolları ve kod semboller aramanıza olanak sağlar. Visual Studio aşağıdaki dillerde gitmek için destek sağlar.

- C#

- C++

- TypeScript

- JavaScript

- Visual Basic

- Git

- Java

- PHP

Bu dosya türlerini belirli bir dil henüz yüklenmemiştir desteği özellikleri açıklandığı gibi daha önce bile sahiptir. Bazı diller için özelleştirilmiş desteğini yükleme, IntelliSense gibi ek dil desteği veya ampuller gibi diğer Gelişmiş dil özellikleri sağlayabilir.

## <a name="add-support-for-non-supported-languages"></a>Desteklenmeyen dilleri desteği ekleme

Visual Studio kullanarak Düzenleyicisi'nde dil desteği sağlayan [TextMate dil bilgileri](https://manual.macromates.com/en/language_grammars). En sevdiğiniz programlama dili Visual Studio Düzenleyicisi'nde şu anda desteklenmemektedir, ilk olarak, web araması&mdash;TextMate paketi dil için zaten var olabilir. Bir bulamazsanız, yine de destek de kendiniz dil dilbilgisi ve kod parçacıkları için TextMate paketi model oluşturarak ekleyebilirsiniz.

Visual Studio aşağıdaki klasörde yeni TextMate dil bilgileri ekleyin:

*%userprofile%\\.vs\Extensions*

Bunlar kendi durumunuza uygularsanız, bu taban yolu altında aşağıdaki klasörleri ekleyin:

|Klasör adı|Açıklama|
|-----------------|-----------------|
|\\*\<dil adı >*|Dil klasörü. Değiştirin  *\<dil adı >* dil adı. Örneğin, *\Matlab*.|
|*\Syntaxes*|Dilbilgisi klasör. Dil bilgisi içeren *.json* dil için gibi dosyaları *Matlab.json*.|
|*\Snippets*|Kod parçacıklarının klasör. Dili için kod parçacıkları içerir.|

Windows içinde *% USERPROFILE %* yolunu Çözümler: *c:\Users\\\<kullanıcı adı >*. Varsa *uzantıları* klasörü, sisteminizde mevcut değil, oluşturmanız gerekir. Klasör zaten varsa, gizlenir.

> [!TIP]
> Düzenleyicide açık herhangi bir dosya varsa, bunları TextMate dil bilgileri ekledikten sonra söz dizimi vurgulama görmek için kapatıp gerekecektir.

TextMate dil bilgisi oluşturma hakkında daha fazla bilgi için bkz. [TextMate - dil dilbilgisi giriş](https://developmentality.wordpress.com/2011/02/08/textmate-introduction-to-language-grammars/) ve [bir Textmate paketi için bir dil dilbilgisi ve özel tema oluşturma hakkında notlar](https://benparizek.com/notebook/notes-on-how-to-create-a-language-grammar-and-custom-theme-for-a-textmate-bundle).

## <a name="see-also"></a>Ayrıca bkz.

- [Dil sunucusu Protokolü uzantısı ekleme](../extensibility/adding-an-lsp-extension.md)
- [İzlenecek yol: Kod parçacığı oluşturma](../ide/walkthrough-creating-a-code-snippet.md)
- [İzlenecek yol: Deyim tamamlama görüntüleme](../extensibility/walkthrough-displaying-statement-completion.md)
