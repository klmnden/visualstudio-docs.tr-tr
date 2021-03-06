---
title: Geliştiriciler için C# düzenlemelere giriş
description: Visual Studio 'da kod düzenleyicisine bu 10 dakikalık bir giriş, Visual Studio 'Nun kodu yazma, gezinme ve daha kolay şekilde anlama C# yaptığı bazı yolları gösterir.
ms.custom: seodec18, get-started
ms.date: 11/20/2018
ms.technology: vs-ide-general
ms.topic: tutorial
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
ms.workload:
- dotnet
ms.openlocfilehash: 517437bb1042d052520019c10899173cbc0bf988
ms.sourcegitcommit: 44e9b1d9230fcbbd081ee81be9d4be8a485d8502
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/30/2019
ms.locfileid: "70180257"
---
# <a name="learn-to-use-the-code-editor"></a>Kod Düzenleyicisi'ni kullanmayı öğrenin

Visual Studio Kod düzenleyicisinde 10 dakikalık giriş, Visual Studio yazma, gezinme ve kodu daha kolay anlama yapar yollarından bazıları aramak için bir dosya için kod ekleyeceğiz.

::: moniker range="vs-2017"

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range="vs-2019"

> [!TIP]
> Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads) ücretsiz yüklemek için sayfa.

::: moniker-end

Bu makalede zaten bildiğiniz varsayılmaktadır C#. Bu durumda, ilk olarak [Visual Studio 'da kullanmaya C# başlama ve ASP.NET Core](tutorial-aspnet-core.md) gibi bir öğreticiye bakmanız önerilir.

> [!TIP]
> Bu makaleyle birlikte izlemek için, Visual Studio için C# ayarların seçili olduğundan emin olun. Tümleşik geliştirme ortamı (IDE) için ayarları seçme hakkında daha fazla bilgi için bkz. [ortam ayarlarını seçme](visual-studio-ide.md#select-environment-settings).

## <a name="create-a-new-code-file"></a>Yeni bir kod dosyası oluşturma

Yeni bir dosya oluşturarak ve bazı kodlar eklemeden başlatın.

::: moniker range="vs-2017"

1. Visual Studio'yu açın.

::: moniker-end

::: moniker range=">=vs-2019"

1. Visual Studio'yu açın. Geliştirme ortamını açmak için **ESC** tuşuna basın veya başlangıç penceresinde **kod olmadan devam et** ' e tıklayın.

::: moniker-end

2. Menü çubuğundaki **Dosya** menüsünde **Yeni** > **Dosya**' yı seçin.

3. İçinde **yeni dosya** iletişim kutusunun **genel** kategorisi seçin **Visual C# sınıfı**ve ardından **açık**.

   C# sınıfı çatısında önizlememiz ile düzenleyicideki yeni bir dosya açar. (Bulunur. bir kod dosyası Kod Düzenleyicisi'nın sunduğu bazı avantajları elde etmek için tam Visual Studio projesi; tüm yapmanız gereken oluşturmanız da gerekmez dikkat edin!)

   ![C# kod dosyasını Visual Studio'da](../media/tutorial-editor.png)

## <a name="use-code-snippets"></a>Kod parçacıkları kullanma

Visual Studio sağlar yararlı *kod parçacıkları* kod bloklarında kullanılan yaygın olarak hızla ve kolayca oluşturmak için kullanabilirsiniz. [Kod parçacıkları](../../ide/code-snippets.md) C#, Visual Basic ve C++ gibi farklı programlama dili için kullanılabilir. C# ekleyelim `void Main` bizim dosyasına kod parçacığı.

1. İmlecinizi son kapanış ayracı kısalarak **}** dosyasında ve karakterleri yazdıktan `svm` (olduğu anlamına gelir `static void Main` &mdash;çok fazla ise ne bilmiyorsanız endişelenmeyin anlamına gelir).

   Hakkında bilgi ile bir açılır iletişim kutusu görünür `svm` kod parçacığı.

   ![Visual Studio'da kod parçacığı için IntelliSense](../media/tutorial-intellisense-snippet.png)

1. Tuşuna **sekmesini** iki kez kod parçacığını eklemek için.

   Gördüğünüz `static void Main()` yöntem imzası dosyasına eklenir. [Main()](/dotnet/csharp/programming-guide/main-and-command-args/) C# uygulamaları için giriş noktası bir yöntemdir.

Kullanılabilir kod parçacıkları farklı programlama dili için farklılık gösterir. Kullanılabilir kod parçacıkları seçerek dilinizi göz atabilirsiniz **Düzenle** > **IntelliSense** > **parçacık Ekle**ve ardından Dilinizin klasör seçme. C# ' ta listesi aşağıdaki gibi görünür:

![C# kod parçacığı listesi](../media/tutorial-code-snippet-list.png)

Liste oluşturmak için kod parçacıkları içeren bir [sınıfı](/dotnet/csharp/programming-guide/classes-and-structs/classes), [Oluşturucusu](/dotnet/csharp/programming-guide/classes-and-structs/constructors), [için](/dotnet/csharp/language-reference/keywords/for) döngü, bir [varsa](/dotnet/csharp/language-reference/keywords/if-else) veya [geçiş](/dotnet/csharp/language-reference/keywords/switch)deyimi ve daha fazlası.

## <a name="comment-out-code"></a>Kodu açıklama

Visual Studio menü çubuğunda altında düğmelerden araç çubuğunda, kodu daha üretken olmanıza yardımcı olabilir. Örneğin, IntelliSense tamamlama modunu açıp kapatabilirsiniz ([IntelliSense](../../ide/using-intellisense.md) yöntemleri, diğerlerinin arasında eşleşen bir listesini görüntüleyen bir kodlama yardımcısıdır) artırın veya bir satır girintisini Azalt veya istemediğiniz kod açıklama derlemek. Bu bölümde, biz bazı kodu açıklama.

![Düzenleyici araç çubuğu](../media/tutorial-editor-toolbar.png)

1. Aşağıdaki kodu yapıştırın `Main()` yöntem gövdesi.

    ```csharp
    // _words is a string array that we'll sort alphabetically
    string[] _words = {
        "the",
        "quick",
        "brown",
        "fox",
        "jumps"
    };

    string[] morewords = {
        "over",
        "the",
        "lazy",
        "dog"
    };

    IEnumerable<string> query = from word in _words
                                orderby word.Length
                                select word;
    ```

1. Değil kullandığımız `morewords` değişkeni, ancak kullanabilir, daha sonra tamamen silmek istemediğiniz şekilde. Bunun yerine, şimdi bu satırları açıklama satırı yapar. Tüm tanımını seçin `morewords` için kapanış noktalı virgül ve ardından **Seçilen satırdan yorum** araç çubuğunda. Klavyeyi kullanmak isterseniz, basın **Ctrl**+**K**, **Ctrl**+**C**.

   ![Açıklama düğmesi](../media/tutorial-comment-out.png)

   C# açıklama karakterleri `//` kodu açıklama eklemek için seçili her satırın başına eklenir.

## <a name="collapse-code-blocks"></a>Kod bloğu Daralt

Boş görmesini istemediğiniz [Oluşturucusu](/dotnet/csharp/programming-guide/classes-and-structs/constructors) için `Class1` oluşturulan, bu nedenle bizim kod görünümünü sekmenize Düzen vermenize için şimdi daraltılabilir. Küçük bir gri kutu içine eksi işareti ile Oluşturucu, ilk satırının kenar boşluğunda seçin. Veya, klavye kullanıcısıysanız, herhangi bir oluşturucu kodunu ve ENTER tuşuna imleci **Ctrl**+**M**, **Ctrl**+**M** .

![Anahat oluşturma Daralt düğmesi](../media/tutorial-collapse.png)

Üç nokta ve ardından yalnızca ilk satırı, kod bloğu daraltır (`...`). Kod bloğunu tekrar artırmak için artık bir artı işareti veya tuşuna basın aynı gri kutusunda tıklayın **Ctrl**+**M**, **Ctrl**+**M**  yeniden. Bu özelliğin adı [anahat](../../ide/outlining.md) ve uzun yöntemleri veya tüm sınıflar daraltma özellikle yararlı olur.

## <a name="view-symbol-definitions"></a>Sembol tanımlarını görüntüleme

Visual Studio Düzenleyicisi, bir tür, yöntem vb. tanımını incelemek kolaylaştırır. Bir yol, tanımı içeren dosyaya gitmeniz, örneğin **Tanıma Git** ' i seçerek veya sembolün başvurduğu her yerde **F12** tuşuna basarak. İçinde çalışmakta olduğunuz odağınızı uzağa dosya hareket etmediği bir bile daha hızlı yolu [Özet tanım](../../ide/go-to-and-peek-definition.md#peek-definition). Şimdi tanımda Özet `string` türü.

1. Tüm oluşması sağ `string` ve **Özet tanım** içerik menüsünde. Veya basın **Alt**+**F12**.

   Tanımını bir açılır pencere görünür `String` sınıfı. Açılır pencere veya hatta göz at peeked kodun başka bir tür tanımı içinde gezinebilirsiniz.

   ![Özet tanım penceresi](../media/tutorial-peek-definition.png)

1. Açılır pencerenin sağ üst köşedeki "x" işareti olan küçük kutusunu seçerek baktı tanım penceresini kapatın.

## <a name="use-intellisense-to-complete-words"></a>Sözcükleri tamamlamak için IntelliSense kullanma

[IntelliSense](../../ide/using-intellisense.md) , kodlamaya, her bir kaynaktır. Bu, kullanılabilir üyeler bir türü veya farklı bir yöntem aşırı yüklemeleri için parametre ayrıntıları hakkında bilgi gösterebilirsiniz. IntelliSense, bunu ayırt etmek için yeterli sayıda karakter girdikten sonra bir sözcük tamamlamak için de kullanabilirsiniz. Bir Git programının çıktısı için standart yerdir konsol penceresine sıralı dizeler yazdırmak için kod satırı ekleyelim.

1. Aşağıda `query` aşağıdaki kod yazarak değişken Başlat:

   ```csharp
   foreach (string str in qu
   ```

   IntelliSense, Göster gördüğünüz **hızlı bilgi** hakkında `query` simgesi.

   ![Visual Studio IntelliSense Sözcük tamamlama](../media/tutorial-intellisense-completion-list.png)

1. Word geri kalanını eklemek için `query` IntelliSense'nın sözcük tamamlama işlevlerini kullanarak basın **sekmesini**.

1. Şu kod gibi aramak için kod bloğunu kapatmak tamamlayın. Kod parçacıkları, yeniden girerek kullanarak bile kendinizi geliştirebilirsiniz `cw` ve tuşuna basarak **sekmesini** iki kez oluşturulacak `Console.WriteLine` kod.

   ```csharp
   foreach (string str in query)
   {
      Console.WriteLine(str);
   }
   ```

## <a name="refactor-a-name"></a>Bir adı yeniden düzenleyin

Hiç kimse ilk kez kod sağ alır ve bir değişkeni veya yöntemin adını değiştirmeniz gerekebilir şeyleri biridir. Visual Studio'nun deneyelim [yeniden düzenleme](../../ide/refactoring-in-visual-studio.md) yeniden adlandırmak için işlevselliği `_words` değişkenini `words`.

1. Tanımı imleci yerleştirin `_words` değişken ve **Yeniden Adlandır** sağ tıklayın veya bağlam menüsünü veya basın **Ctrl**+**R**, **Ctrl**+**R**.

   Bir açılır pencere **Yeniden Adlandır** iletişim kutusunun en üstünde görünür sağında Düzenleyici.

1. İstediğiniz adı girin **sözcükleri**. Dikkat başvuru `words` sorguda da otomatik olarak yeniden adlandırıldı. Basmadan önce **Enter**seçin **açıklamaları dahil** onay kutusu **Yeniden Adlandır** açılan kutusu.

   ![Yeniden Adlandır iletişim kutusu](../media/tutorial-rename.png)

1. Tuşuna **girin**.

   Her iki oluşumlarını `words` , başvuru yanı sıra yeniden adlandırıldığı `words` içinde kod açıklaması.

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
