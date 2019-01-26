---
title: R Markdown
description: Yüksek kaliteli raporları, sunumları ve panolar oluşturmak için Visual Studio'da R Markdown belgeleri oluşturma
ms.date: 11/16/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: jillfra
ms.workload:
- data-science
ms.openlocfilehash: 3a15899d561088ee9911cb08eaa4f5887b996a3e
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55000139"
---
# <a name="create-r-markdown-documents"></a>R Markdown belgeleri oluşturma

[R Markdown](https://rmarkdown.rstudio.com/) yüksek kalitede belgeler, raporlar, sunular ve panolar R analizi dönüştüren bir belge biçimidir.

R araçları için Visual Studio (RTVS) R Markdown öğe şablonu sağlar, Düzenleyici (IntelliSense dahil olmak üzere Düzenleyicisi içinde R kod için), dosya oluşturma özellikleri destekler ve Canlı Önizleme.

## <a name="using-r-markdown"></a>R Markdown kullanma

1. Visual Studio’yu kapatın.
1. (Yalnızca bir kez) Yükleme `pandoc` gelen [pandoc.org](http://pandoc.org/installing.html).
1. Pandoc yüklemesini seçmelisiniz Visual Studio'yu yeniden başlatın.
1. Yükleme `knitr` ve `rmarkdown` bunu yapabilirsiniz paketleri [etkileşimli pencere](interactive-repl-for-r-in-visual-studio.md):

    ```R
    install.packages("knitr")
    install.packages("rmarkdown")

    ```
1. Yeni bir R Markdown dosyası kullanarak oluşturmak **dosya** > **yeni** > **dosya** menü komutu ve seçerek **R**  >  **R Markdown** listeden. Bir proje bağlamında, Çözüm Gezgini'nde projeye sağ tıklayıp **ekleyin R Markdown** (veya **Ekle** > **yeni öğe** seçerek**R Markdown** listeden).

1. Yeni dosyasının varsayılan içeriklerini aşağıdaki gibidir:

    ~~~markdown
    ---
    title: "Untitled"
    output: html_document
    ---

    This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and Microsoft Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

    When you click the **R Tools | Publish | Preview** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

    ```{r}
    summary(cars)
    ```

    You can also embed plots, for example:

    ```{r, echo=FALSE}
    plot(cars)
    ```

    Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

    ~~~

## <a name="previews"></a>Önizlemeler

Visual Studio 2017 sürüm 15.5 ve daha sonra otomatik olarak R Markdown için Canlı Önizleme sağlar. Düzenleyici ve önizleme arasında otomatik eşitlemeyi etkinleştirmek için işaretleyin **R Araçları** > **Markdown** > **otomatik eşitleme** ( **CTRL**+**Shift**+**Y**). Otomatik eşitleme kullanmıyorsanız, preview kullanarak yenileyebilirsiniz **R Araçları** > **Markdown** > **yeniden R Markdown önizlemesi**.

Microsoft Word biçimleri Düzenleyicisi'nde sağ tıklatın ve aşağıdakilerden birini seçerek ve dosyanın PDF, HTML biçimindeki de önizleyebilirsiniz **Önizleme** komutları. Aynı komutları da kullanılabilir **R Araçları** > **Markdown** menüsü. (Bu komutlar Visual Studio'nun önceki sürümlerinde bulunan **R Araçları** > **Yayımla** menü.)

![RMarkdown Canlı Önizleme ve diğer Önizleme menü komutları](media/rmarkdown-live-preview.png)
