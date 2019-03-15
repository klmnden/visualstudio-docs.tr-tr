---
title: Visual Basic geliştiricileri için düzenleme giriş
description: Visual Studio Kod düzenleyicisinde bu 10 dakikalık bir giriş, Visual Studio yazma, gezinme ve Visual Basic kodu daha kolay anlama yapar yollardan bazılarını gösterir.
ms.custom: seodec18, get-started
ms.date: 11/20/2018
ms.technology: vs-ide-general
ms.topic: tutorial
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- VB
ms.workload:
- dotnet
ms.openlocfilehash: 3af730ae4d5b358eab223e2a5a8288daaf632071
ms.sourcegitcommit: 4ffb7be5384ad566ce46538032bf8561754c61a4
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2019
ms.locfileid: "58069638"
---
# <a name="learn-to-use-the-code-editor"></a>Kod Düzenleyicisi'ni kullanmayı öğrenin

Visual Studio Kod düzenleyicisinde 10 dakikalık giriş, Visual Studio yazma, gezinme ve kodu daha kolay anlama yapar yollarından bazıları aramak için bir dosya için kod ekleyeceğiz.

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2017) ücretsiz yüklemek için sayfa.

Bu makalede, zaten Visual Basic ile ilgili bilgi sahibi olduğunuz kabul edilmektedir. Siz değilseniz, öğreticiye bakın gibi öneririz [Visual Studio'daki Visual Basic ile çalışmaya başlama](../../get-started/visual-basic/tutorial-console.md) ilk.

> [!TIP]
> Bu makaleyi izlemek için Visual Basic ayarları için Visual Studio seçili olduğundan emin olun. Tümleşik geliştirme ortamı (IDE) için ayarları seçme hakkında daha fazla bilgi için bkz: [ortam ayarlarını Seç](visual-studio-ide.md#select-environment-settings).

## <a name="create-a-new-code-file"></a>Yeni bir kod dosyası oluşturma

Yeni bir dosya oluşturarak ve bazı kodlar eklemeden başlatın.

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın. Tuşuna **Esc** veya **kod olmadan devam** geliştirme ortamı'nı açmak için başlangıç penceresinde.

::: moniker-end

2. Gelen **dosya** menü çubuğunda menüsünde **yeni dosya**.

3. İçinde **yeni dosya** iletişim kutusunun **genel** kategorisi seçin **Visual Basic sınıfı**ve ardından **açık**.

   Visual Basic sınıfı çatısında önizlememiz ile düzenleyicideki yeni bir dosya açar. (Zaten bazı Kod Düzenleyicisi sunar, söz dizimi vurgulama gibi avantajları elde etmek için tam Visual Studio projesi oluşturmanız gerekmez fark. İhtiyacınız olan bir kod dosyası!)

   ![Visual Studio'da Visual Basic kod dosyası](media/tutorial-editor.png)

## <a name="use-code-snippets"></a>Kod parçacıkları kullanma

Visual Studio sağlar yararlı *kod parçacıkları* kod bloklarında kullanılan yaygın olarak hızla ve kolayca oluşturmak için kullanabilirsiniz. [Kod parçacıkları](../../ide/code-snippets.md) Visual Basic dahil olmak üzere farklı programlama dili için kullanılabilir C#ve C++. Visual Basic ekleyelim **alt** bizim dosyasına kod parçacığı.

1. İmlecinizi diyor satırın yukarısında `End Class`ve türü **alt**.

   Hakkında bilgi ile bir açılır iletişim kutusu görünür `Sub` anahtar sözcüğü ve nasıl ekleneceğini **alt** kod parçacığı.

   ![Visual Studio'da kod parçacığı için IntelliSense](media/tutorial-intellisense-snippet.png)

1. Tuşuna **sekmesini** iki kez kod parçacığını eklemek için.

   Alt yordam anahat `MySub()` dosyasına eklenir.

Kullanılabilir kod parçacıkları farklı programlama dili için farklılık gösterir. Visual Basic için kullanılabilir kod parçacıkları seçerek bakabilirsiniz **Düzenle** > **IntelliSense** > **parçacık Ekle** (veya tuşlarınabasın **CTRL**+**K**, **Ctrl**+**X**). Visual Basic için kod parçacıkları için aşağıdaki kategorilerde kullanılabilir:

![Visual Basic kod parçacığı listesi](media/tutorial-code-snippet-list.png)

Bir dosya bir metin dosyasına yazma, okuma bir kayıt defteri değeri, bir SQL sorgusu yürütme, oluşturma bilgisayarda varsa belirlemek için kod parçacıkları olan bir [her biri için... Sonraki deyimi](/dotnet/visual-basic/language-reference/statements/for-each-next-statement)ve çok daha fazlası.

## <a name="comment-out-code"></a>Kodu açıklama

Visual Studio menü çubuğunda altında düğmelerden araç çubuğunda, kodu daha üretken olmanıza yardımcı olabilir. Örneğin, IntelliSense tamamlanma moduna geç, artırmak veya satır girintisini Azalt veya kodu açıklama derlemeye istemediğiniz. ([IntelliSense](../../ide/using-intellisense.md) yöntemleri, diğerlerinin arasında eşleşen bir listesini görüntüleyen bir kodlama yardımcısıdır.) Bu bölümde, biz bazı kodu açıklama.

![Düzenleyici araç çubuğu düğmeleri](media/tutorial-editor-toolbar.png)

1. Aşağıdaki kodu yapıştırın `MySub()` yordamı gövdesi.

   ```vb
   ' _words is a string array that we'll sort alphabetically
   Dim _words = New String() {
   "the",
   "quick",
   "brown",
   "fox",
   "jumps"
   }

   Dim morewords = New String() {
   "over",
   "the",
   "lazy",
   "dog"
   }

   Dim query = From word In _words
               Order By word.Length
               Select word
   ```

1. Değil kullandığımız `morewords` dizi, ancak kullanabilir, daha sonra tamamen silmek istemediğiniz şekilde. Bunun yerine, şimdi bu satırları açıklama satırı yapar. Tüm tanımını seçin `morewords` için kapanış küme ayracı ve ardından **Seçilen satırdan yorum** araç çubuğunda. Klavyeyi kullanmak isterseniz, basın **Ctrl**+**K**, **Ctrl**+**C**.

   ![Açıklama düğmesi](media/tutorial-comment-out.png)

   Visual Basic açıklama karakterini `'` kodu açıklama eklemek için seçili her satırın başına eklenir.

## <a name="collapse-code-blocks"></a>Kod bloğu Daralt

İlginizi çeken bölümleri odaklanmak için kod bölümlerini daraltabilirsiniz. Uygulama, şimdi Daralt `_words` bir kod satırı için bir dizi. Küçük bir gri kutu içine eksi işaretiyle yazan satırı kenar boşluğunda seçin `Dim _words = New String() {`. Veya, klavye kullanıcısıysanız, herhangi bir dizi tanımı ve ENTER tuşuna imleci **Ctrl**+**M**, **Ctrl**+**M** .

![Anahat oluşturma Daralt düğmesi](media/tutorial-collapse.png)

Üç nokta ve ardından yalnızca ilk satırı, kod bloğu daraltır (`...`). Kod bloğunu tekrar artırmak için artık bir artı işareti veya tuşuna basın aynı gri kutusunda tıklayın **Ctrl**+**M**, **Ctrl**+**M**  yeniden. Bu özelliğin adı [anahat](../../ide/outlining.md) ve uzun yöntemleri veya tüm sınıflar daraltma özellikle yararlı olur.

## <a name="view-symbol-definitions"></a>Sembol tanımlarını görüntüleme

Visual Studio Düzenleyicisi, bir tür, yöntem vb. tanımını incelemek kolaylaştırır. Örneğin seçerek tanımını içeren dosyayı gitmek için bir yolu olan **Tanıma Git** herhangi bir sembol başvurulur. İçinde çalışmakta olduğunuz odağınızı uzağa dosya hareket etmediği bir bile daha hızlı yolu [Özet tanım](../../ide/go-to-and-peek-definition.md#peek-definition). Şimdi tanımda Özet `String` türü.

1. Word sağ `String` ve **Özet tanım** içerik menüsünde. Veya basın **Alt**+**F12**.

   Tanımını bir açılır pencere görünür `String` sınıfı. Açılır pencere veya hatta göz at peeked kodun başka bir tür tanımı içinde gezinebilirsiniz.

   ![Özet tanım penceresi](media/tutorial-peek-definition.png)

1. Açılır pencerenin sağ üst köşedeki "x" işareti olan küçük kutusunu seçerek baktı tanım penceresini kapatın.

## <a name="use-intellisense-to-complete-words"></a>Sözcükleri tamamlamak için IntelliSense kullanma

[IntelliSense](../../ide/using-intellisense.md) , kodlamaya, her bir kaynaktır. Bu, kullanılabilir üyeler bir türü veya farklı bir yöntem aşırı yüklemeleri için parametre ayrıntıları hakkında bilgi gösterebilirsiniz. IntelliSense, bunu ayırt etmek için yeterli sayıda karakter girdikten sonra bir sözcük tamamlamak için de kullanabilirsiniz. Bir Git programının çıktısı için standart yerdir konsol penceresine sıralı dizeler yazdırmak için kod satırı ekleyelim.

1. Aşağıda `query` aşağıdaki kod yazarak değişken Başlat:

   ```vb
   For Each str In qu
   ```

   IntelliSense, Göster gördüğünüz **hızlı bilgi** hakkında `query` simgesi.

   ![Visual Studio IntelliSense Sözcük tamamlama](media/tutorial-intellisense-completion-list.png)

1. Word geri kalanını eklemek için `query` IntelliSense'nın sözcük tamamlama işlevlerini kullanarak basın **sekmesini**.

1. Şu kod gibi aramak için kod bloğunu kapatmak tamamlayın.

   ```vb
   For Each str In query
       Console.WriteLine(str)
   Next
   ```

## <a name="refactor-a-name"></a>Bir adı yeniden düzenleyin

Hiç kimse ilk kez kod sağ alır ve bir değişkeni veya yöntemin adını değiştirmeniz gerekebilir şeyleri biridir. Visual Studio'nun deneyelim [yeniden düzenleme](../../ide/refactoring-in-visual-studio.md) yeniden adlandırmak için işlevselliği `_words` değişkenini `words`.

1. İmlecinizi tanımı `_words` değişkeni ve **Yeniden Adlandır** sağ tıklayın veya bağlam menüsünde.

   Bir açılır pencere **Yeniden Adlandır** iletişim kutusunun en üstünde görünür sağında Düzenleyici.

1. Değişkeniyle `_words` halen seçiliyken, istediğiniz adı yazın **sözcükleri**. Dikkat başvuru `words` sorguda da otomatik olarak yeniden adlandırıldı. Basmadan önce **Enter** veya **Uygula**seçin **açıklamaları dahil** onay kutusu **Yeniden Adlandır** açılan kutusu.

   ![Yeniden Adlandır iletişim kutusu](media/tutorial-rename.png)

1. Tuşuna **Enter** veya **Uygula**.

   Her iki oluşumlarını `words` başvuru yanı sıra adlandırılır `words` içinde kod açıklaması.

## <a name="next-steps"></a>Sonraki adımlar

> [!div class="nextstepaction"]
> [Projeler ve çözümler hakkında bilgi edinin](tutorial-projects-solutions.md)

## <a name="see-also"></a>Ayrıca bkz.

- [Kod parçacıkları](../../ide/code-snippets.md)
- [Kod gidin](../../ide/navigating-code.md)
- [Anahat Oluşturma](../../ide/outlining.md)
- [Tanıma ve Özet Tanıma Gitme](../../ide/go-to-and-peek-definition.md)
- [Yeniden Düzenleme](../../ide/refactoring-in-visual-studio.md)
- [IntelliSense kullanma](../../ide/using-intellisense.md)