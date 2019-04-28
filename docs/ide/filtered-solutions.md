---
title: Projelerin bir alt kümesini yükleme
ms.date: 04/22/2019
ms.prod: visual-studio-dev16
ms.topic: conceptual
helpviewer_keywords:
- filtered solution
- solution filtering
author: gewarren
ms.author: stsu
manager: jillfra
monikerRange: '>= vs-2019'
ms.openlocfilehash: 2612770b760bec70ec9ee6c679c47804d4e69f42
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63439823"
---
# <a name="filtered-solutions-in-visual-studio"></a>Visual Studio'da filtrelenmiş çözümleri

Genellikle büyük geliştirme takımları ile çok sayıda proje tek büyük bir çözümde kullanarak işbirliği yapın. Ancak, bireysel geliştiriciler genellikle bu projeler küçük bir kısmı üzerinde çalışır. Büyük çözümlerde açılırken performansını geliştirmek için Visual Studio 2019 sunulan *çözüm filtreleme*. Çözüm filtreleme yalnızca yüklenen seçmeli projeleriyle bir çözüm açın sağlar. Bir alt kümesini bir çözümde proje yüklemeyi çözüm yükü, yapı ve test çalışma zamanı azaltır ve etkinleştirir gözden geçirme daha odaklı.

Aşağıdaki özellikler mevcuttur:

- Daha hızlı bir çözüm açarak projeleri yüklemeden kodu alabilirsiniz. Çözüm açıldıktan sonra yükleme için hangi projelerin seçerek belirleyebilirsiniz.

- Bir çözümü yeniden açın, Visual Studio önceki oturumunuzda hangi projelerin yüklenmiş hatırlar ve yalnızca bu projeleri yükler.

- Bir veya daha fazla proje yükü yapılandırmaları kaydetme veya yapılandırma arkadaşlarıyla paylaşmak için bir çözüm filtre dosyası oluşturabilirsiniz.

## <a name="open-a-filtered-solution"></a>Filtrelenmiş bir çözüm açın

Doğrudan projeleri yüklemeden bir çözüm açabilmek **Proje Aç** iletişim aracılığıyla veya [komut satırı](#command-line).

### <a name="open-project-dialog"></a>Açık proje iletişim kutusu

Bir çözümü kullanarak tüm projeleri yüklemeden açmak için **Proje Aç** iletişim:

1. Seçin **dosya** > **açık** > **proje/çözüm** menü çubuğundan.

2. İçinde **Proje Aç** iletişim çözümünü seçin ve ardından **proje yüklenmemesine**.

   ![Visual Studio Proje Aç iletişim kutusunda seçili projeler yüklenmez](media/filtered-solutions/do-not-load-projects.png)

3. Seçin **açık**.

   Çözüm tüm yüklenmemiş projeleri ile açılır.

4. İçinde **Çözüm Gezgini**, yüklemek istediğiniz projeleri seçin (basın **Ctrl** birden fazla proje seçmek için tıklatırken) ve ardından proje üzerinde sağ tıklatın ve seçin **projeyi yeniden yükle** .

   ![Visual Studio Çözüm Gezgini'nde birden çok projeleri yeniden yükle](media/filtered-solutions/reload-project.png)

   Visual Studio çözümünü yerel olarak bir sonraki açışınızda hangi projelerin yüklenen hatırlanır.

### <a name="command-line"></a>Komut satırı

(Yeni Visual Studio 2019 sürüm 16.1.)

Komut satırından yüklemeden, tüm projeleri bir çözümü açmak için kullanmak [ `/donotloadprojects` ](../ide/reference/donotloadprojects-devenv-exe.md) aşağıdaki örnekte gösterildiği gibi geçin:

```cmd
devenv /donotloadprojects MySln.sln
```

## <a name="toggle-unloaded-project-visibility"></a>Yüklenmemiş proje görünürlüğünü Değiştir

Çözümdeki tüm projeleri veya yalnızca aşağıdaki seçeneklerden birini kullanarak yüklü olanları görmek seçebileceğiniz **Çözüm Gezgini**:

- Çözümü sağ tıklatın **yüklenmemiş projeleri göster** veya **yüklenmemiş projeleri Gizle**.

- Çözümü etkinleştirmek için düğümü seçin **tüm dosyaları göster** düğmesini; ardından yüklenmemiş projeleri görünürlüğünü açıp kapatmak için düğmeyi tıklayın.

   ![Visual Studio Çözüm Gezgini'nde tüm dosyaları düğmesini göster](media/filtered-solutions/show-all-files.PNG)

## <a name="load-project-dependencies"></a>Proje bağımlılıkları yükleyin

Yalnızca seçili projeleri burada yüklü olan bir çözümde bir proje proje bağımlılıklarınızı yüklenen tüm olmayabilir. Kullanım **yük proje bağımlılıkları** menü seçeneğini bir proje bağımlı tüm projeleri aynı zamanda yüklendiğinden emin olun. Bir veya daha fazla yüklenmiş projelerinde sağ **Çözüm Gezgini** ve **yük proje bağımlılıkları**.

![Visual Studio 2019 yük proje bağımlılıkları](media/filtered-solutions/load-project-dependencies.png)

## <a name="solution-filter-files"></a>Çözüm filtresi dosyaları

Proje yükü yapılandırmanızı paylaşabilir veya kaynak denetimine uygulamak istiyorsanız, bir çözüm filtre dosyası oluşturabilirsiniz (uzantısına sahip *.slnf*). Bir çözüm filtre dosyasını açtığınızda, çözüm yüklenen belirtilen projeleri ile gizli yüklenmemiş projeleri Visual Studio'da açılır. Yapabilecekleriniz [geçiş](#toggle-unloaded-project-visibility) yüklenmemiş projeleri görüntülemek için.

Çözüm filtresi dosyaları görsel olarak ayırt normal çözüm dosyaları ek Huni glifine çözümde yanındaki simge tarafından **Çözüm Gezgini**. Filtre ve yüklenen projelerin sayısını adını da çözüm adının yanında gösterilir.

![Çözüm filtre dosyası Visual Studio Çözüm Gezgini'nde Aç](media/filtered-solutions/solution-filter.PNG)

> [!NOTE]
> Çözüm filtresi dosyasını oluşturduktan sonra özgün çözüme yeni proje eklenirse, kaldırılan projelerinde olarak görünürler **Çözüm Gezgini**.

### <a name="create-a-solution-filter-file"></a>Bir çözüm filtre dosyası oluşturma

1. İçinde **Çözüm Gezgini**, çözüme sağ tıklayın ve seçin **çözüm filtre olarak Kaydet**.

   ![Visual Studio Çözüm Gezgini'nde çözüm filtre olarak Kaydet menüsü](media/filtered-solutions/save-as-solution-filter.png)

2. Bir ad ve çözüm filtre dosyası için konum seçin.

Bir çözüm filtre dosyasını oluşturduktan sonra eklenir, **son projeler ve çözümler** kolay erişim için liste:

![Visual Studio'da en son öğeyi aç](media/filtered-solutions/open-recent.png)

## <a name="see-also"></a>Ayrıca bkz.

- [Çözüm Gezgini'nde dosya iç içe yerleştime özelleştirme](file-nesting-solution-explorer.md)
- [Visual Studio performansını iyileştirme](optimize-visual-studio-performance.md)
