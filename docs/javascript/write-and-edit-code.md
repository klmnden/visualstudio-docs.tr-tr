---
title: JavaScript geliştiricileri için düzenleme giriş
description: Bu giriş Kod Düzenleyicisi'nde Visual Studio için Visual Studio anlamak daha kolay JavaScript kodu yazma ve gezinme yapar yollardan bazılarını gösterir.
ms.custom: ''
ms.date: 12/13/2018
ms.prod: visual-studio-dev15
ms.technology: vs-nodejs
ms.topic: conceptual
author: mikejo5000
ms.author: mikejo
manager: douge
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: 5f511b668c207ae719dbb981d7dc5640f0fa124c
ms.sourcegitcommit: f6dd17b0864419083d0a1bf54910023045526437
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/27/2018
ms.locfileid: "53802702"
---
# <a name="learn-to-use-the-code-editor"></a>Kod Düzenleyicisi'ni kullanmayı öğrenin

Bu kısa giriş Kod Düzenleyicisi'nde Visual Studio için Visual Studio yazma, gezinme ve kodu daha kolay anlama yapar yollarından bazıları inceleyeceğiz.

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=button+cta&utm_content=download+vs2017) ücretsiz yüklemek için sayfa. Uygulama geliştirme yaptığınız türüne bağlı olarak, yüklemeniz gerekebilir **Node.js geliştirme iş yükü** Visual Studio ile.

Bu makalede, zaten JavaScript geliştirme ile ilgili bilgi sahibi olduğunuz kabul edilmektedir. Siz değilseniz, öğreticiye bakın gibi öneririz [bir Node.js ve Express uygulaması oluşturma](../javascript/tutorial-nodejs.md) ilk.

> [!TIP]
> Bu makaleyi izlemek için JavaScript ayarları için Visual Studio seçili olduğundan emin olun. Tümleşik geliştirme ortamı (IDE) için ayarları seçme hakkında daha fazla bilgi için bkz: [ortam ayarları](../ide/environment-settings.md). Ayarları içeri aktardığınızda, içeri aktarma **JavaScript** ayarları.

## <a name="add-a-new-project-file"></a>Yeni bir proje dosyanıza ekleyin

Yeni dosyaları projenize eklemek için IDE kullanabilirsiniz.

1. Projenizi Visual Studio'da açın, bir klasör veya Çözüm Gezgini'nde (sağ bölme), proje düğümünü sağ tıklatın ve seçin **Ekle** > **yeni öğe**.

1. İçinde **yeni dosya** iletişim kutusunun **genel** kategorisi gibi eklemek istediğiniz dosya türünü seçin **JavaScript dosyası**ve ardından **Aç** .

    Yeni dosyayı projenize eklenir ve düzenleyicide açılır.

## <a name="use-intellisense-to-complete-words"></a>Sözcükleri tamamlamak için IntelliSense kullanma

IntelliSense, kodlamaya, her bir kaynaktır. Bu, kullanılabilir üyeler bir türü veya farklı bir yöntem aşırı yüklemeleri için parametre ayrıntıları hakkında bilgi gösterebilirsiniz. Aşağıdaki kodda yazarken `Router()`, geçirebileceğiniz bağımsız değişken türlerini görmek. Bu imza Yardımı çağrılır.

![IntelliSense kullanma](../javascript/media/write-code-signature-checking.png)

IntelliSense, bunu ayırt etmek için yeterli sayıda karakter girdikten sonra bir sözcük tamamlamak için de kullanabilirsiniz. İmlecinizi sonra koyarsanız `data` aşağıdaki kod ve türü string `get`, IntelliSense gösterir, tanımlı işlevler önceki kodda ya da tanımlanmış projenize eklediğiniz bir üçüncü taraf Kitaplığı'nda.

![IntelliSense kullanma](../javascript/media/write-code-intellisense.png)

Programlama öğelerin üzerine geldiğinizde IntelliSense de, türleri hakkında bilgi gösterebilirsiniz.

IntelliSense bilgilerini sağlamak için TypeScript dil hizmeti kullanabilirsiniz *d.ts* dosyaları ve JSDoc açıklamaları. En yaygın JavaScript kitaplıkları için *d.ts* dosyaları otomatik olarak alındı. IntelliSense bilgilerinin nasıl alındığını hakkında daha fazla ayrıntı için bkz. [JavaScript IntelliSense](../ide/javascript-intellisense.md?toc=/visualstudio/javascript/toc.json)

## <a name="check-syntax"></a>Sözdizimini denetle

Dil hizmeti Eslint'i söz dizimi denetimini ve linting sağlamak için kullanır. Sözdizimi denetimi düzenleyicide seçme seçeneklerini ayarlamak gerekiyorsa **Araçları** > **seçenekleri** > **JavaScript/TypeScript**  >  **Linting**. Genel Eslint'i yapılandırma dosyasına işaret linting seçenekleri.

Aşağıdaki kodda, yeşil sözdizimi (yeşil dalgalı çizgiler) ifade vurgulaması bakın. Söz dizimi vurgulama üzerine gelin.

![Görünüm söz dizimi hatası](../javascript/media/write-code-syntax-checking.png)

Bu ileti son satırının dil hizmeti virgül bekleniyor bildirir (`,`). Yeşil dalgalı bir uyarı gösterir. Kırmızı dalgalı çizgiler bir hata gösterir.

Alt bölmede tıklayabilirsiniz **hata listesi** uyarı ve dosya adı ve satır numarası ile birlikte bir açıklama görmek için sekmesinde.

![Hata Listesi görünümü](../javascript/media/write-code-error-list.png)

Bu kod, virgülle ekleyerek düzeltebilirsiniz (`,`) önce `"data"`.

## <a name="comment-out-code"></a>Kodu açıklama

Visual Studio menü çubuğunda altında düğmelerden araç çubuğunda, kodu daha üretken olmanıza yardımcı olabilir. Örneğin, IntelliSense tamamlama modunu açıp kapatabilirsiniz ([IntelliSense](../ide/using-intellisense.md) yöntemleri, diğerlerinin arasında eşleşen bir listesini görüntüleyen bir kodlama yardımcısıdır) artırın veya bir satır girintisini Azalt veya istemediğiniz kod açıklama derlemek. Bu bölümde, biz bazı kodu açıklama.

Bir veya daha fazla satır Kod Düzenleyicisi'nde seçin ve sonra **Seçilen satırdan yorum** düğmesi ![düğmesi yorum](../javascript/media/write-code-comment-out.png) araç. Klavyeyi kullanmak isterseniz, basın **Ctrl**+**K**, **Ctrl**+**C**.

JavaScript açıklama karakterleri `//` kodu açıklama eklemek için seçili her satırın başına eklenir.

## <a name="collapse-code-blocks"></a>Kod bloğu Daralt

Bazı bölgelerde kod görünümünü sekmenize Düzen vermenize gerek duyarsanız, daraltabilirsiniz. Küçük bir gri kutu içine eksi işareti ile bir işlevin ilk satırın kenar boşluğunda seçin. Veya, klavye kullanıcısıysanız, herhangi bir oluşturucu kodunu ve ENTER tuşuna imleci **Ctrl**+**M**, **Ctrl**+**M** .

![Anahat oluşturma Daralt düğmesi](../javascript/media/write-code-collapse-code.png)

Üç nokta ve ardından yalnızca ilk satırı, kod bloğu daraltır (`...`). Kod bloğunu tekrar artırmak için artık bir artı işareti veya tuşuna basın aynı gri kutusunda tıklayın **Ctrl**+**M**, **Ctrl**+**M**  yeniden. Bu özelliğin adı [anahat](../ide/outlining.md) ve uzun işlevler veya tüm sınıflar daraltma özellikle yararlı olur.

## <a name="view-definitions"></a>Tanımları görüntüle

Visual Studio Düzenleyicisi, türü, işlev, vb. tanımını incelemek kolaylaştırır. Örneğin seçerek tanımını içeren dosyayı gitmek için bir yolu olan **Tanıma Git** herhangi bir programlama öğesine başvurulur. İçinde çalışmakta olduğunuz odağınızı uzağa dosya hareket etmediği bir bile daha hızlı yolu [Özet tanım](../ide/go-to-and-peek-definition.md#peek-definition). Şimdi tanımda Özet `render` aşağıdaki örnekte yöntemi.

Sağ `render` ve **Özet tanım** içerik menüsünde. Veya basın **Alt**+**F12**.

   Tanımını bir açılır pencere görünür `render` yöntemi. Açılır pencere veya hatta göz at peeked kodun başka bir tür tanımı içinde gezinebilirsiniz.

   ![Özet tanım penceresi](../javascript/media/write-code-peek-definition.png)

1. Açılır pencerenin sağ üst köşedeki "x" işareti olan küçük kutusunu seçerek baktı tanım penceresini kapatın.

## <a name="use-code-snippets"></a>Kod parçacıkları kullanma

Visual Studio sağlar yararlı *kod parçacıkları* kod bloklarında kullanılan yaygın olarak hızla ve kolayca oluşturmak için kullanabilirsiniz. [Kod parçacıkları](../ide/code-snippets.md) JavaScript dahil olmak üzere farklı programlama dili için kullanılabilir. Ekleyelim bir `for` kod dosyanıza döngü.

İmlecinizi, kod parçacığını eklemek, sağ tıklayın ve istediğiniz **kod parçacığı** > **parçacık Ekle**.

![Visual Studio'da kod parçacığı](../javascript/media/write-code-insert-snippet.png)

Bir **parçacık Ekle** Kutusu Düzenleyicisi'nde görüntülenir. Seçin **genel** ve çift tıklatarak **için** listedeki bir öğe.

![İçin kod parçacığı bir for döngüsü Visual Studio'da](../javascript/media/write-code-insert-snippet-for-loop.png)

Bu ekler `for` kodunuzda döngü kod parçacığı:

```javascript
for (var i = 0; i < length; i++) {

}
```

Kullanılabilir kod parçacıkları seçerek dilinizi göz atabilirsiniz **Düzenle** > **IntelliSense** > **parçacık Ekle**ve ardından Dilinizin klasör seçme.

## <a name="see-also"></a>Ayrıca bkz.

- [Kod parçacıkları](../ide/code-snippets.md)
- [Kod gidin](../ide/navigating-code.md)
- [Anahat Oluşturma](../ide/outlining.md)
- [Tanıma ve Özet Tanıma Gitme](../ide/go-to-and-peek-definition.md)
- [Yeniden Düzenleme](../ide/refactoring-in-visual-studio.md)
- [IntelliSense kullanma](../ide/using-intellisense.md)
