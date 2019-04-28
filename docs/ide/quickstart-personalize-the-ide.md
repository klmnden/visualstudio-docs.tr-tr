---
title: Kümesi renk teması ve yazı tipleri
ms.date: 11/20/2017
ms.topic: quickstart
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a43ade295d14934f452123407f9896eebdaf26c7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62953432"
---
# <a name="personalize-the-visual-studio-ide-and-editor"></a>Düzenleyici ve Visual Studio IDE'yi kişiselleştirme

5-10 dakika olan Bu öğreticide, size Visual Studio renk teması koyu tema seçerek özelleştireceksiniz. Biz de iki farklı türde metin düzenleyicisinde metin renklerini özelleştireceksiniz.

::: moniker range="vs-2017"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/vs/older-downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=vs+2017+download) ücretsiz yüklemek için sayfa.

::: moniker-end

::: moniker range=">=vs-2019"

Visual Studio henüz yüklemediyseniz, Git [Visual Studio indirmeleri](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ücretsiz yüklemek için sayfa.

::: moniker-end

## <a name="set-the-color-theme"></a>Renk teması ayarlayabilir

Visual Studio'nun kullanıcı arabirimi için varsayılan renk teması adlı **mavi**. Kendisine değiştirelim **koyu**.

1. Menü çubuğunda, olan menüleri satırının gibi **dosya** ve **Düzenle**, seçin **Araçları** > **seçenekleri**.

1. Üzerinde **ortam** > **genel** seçenekler sayfası, değişiklik **renk teması** seçimi **koyu**seçin **Tamam**.

   Tüm Visual Studio geliştirme ortamı (IDE) için renk teması değişiklikleri **koyu**.

   ::: moniker range="vs-2017"

   ![Visual Studio 2017'de koyu tema](media/quickstart-personalize-dark-theme.png)

   ::: moniker-end

   ::: moniker range="vs-2019"

   ![Visual Studio 2019 koyu temada](media/vs-2019/dark-theme.png)

   ::: moniker-end

> [!TIP]
> Yükleyerek ek önceden tanımlı Temalar yükleyebilirsiniz **Visual Studio Color Theme Editor** gelen [Visual Studio Market](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.VisualStudio2017ColorThemeEditor). Bu aracı yükledikten sonra ek renk temaları görünür **renk teması** aşağı açılan listesi.

## <a name="change-text-color"></a>Metin rengini değiştirme

Şimdi biz düzenleyici için bazı metin renklerini özelleştireceksiniz. İlk olarak, varsayılan renkleri görmek için yeni bir XML dosyası oluşturalım.

1. Menü çubuğundan seçin **dosya** > **yeni** > **dosya**.

1. İçinde **yeni dosya** iletişim kutusunun **genel** kategorisi seçin **XML dosyası**ve ardından **açık**.

1. Aşağıdaki XML içeren satırın altına yapıştırın `<?xml version="1.0" encoding="utf-8"?>`.

   ```xml
   <Catalog>
     <Book id="bk101">
     <Author>Garghentini, Davide</Author>
     <Title>XML Developer's Guide</Title>
     <Genre>Computer</Genre>
     <Price>44.95</Price>
     <PublishDate>2000-10-01</PublishDate>
     <Description>
       An in-depth look at creating applications with XML.
     </Description>
   </Book>
   <Book id="bk102">
     <Author>Garcia, Debra</Author>
     <Title>Midnight Rain</Title>
     <Genre>Fantasy</Genre>
     <Price>5.95</Price>
     <PublishDate>2000-12-16</PublishDate>
     <Description>
       A former architect battles corporate zombies, an evil
       sorceress, and her own childhood to become queen of the world.
     </Description>
   </Book>
   </Catalog>
   ```

   Satır numaralarını Turkuaz-mavi renk ve XML özniteliklerini olduğuna dikkat edin (gibi `id="bk101"`) bir açık mavi renk kodludur. Bu öğeler için metin rengini değiştirmek için ekleyeceğiz.

   ![XML dosyası yazı tipi renkleri](media/quickstart-personalize-xml-file.png)

1. Açmak için **seçenekleri** iletişim kutusunda **Araçları** > **seçenekleri** menü çubuğundan.

1. Altında **ortam**, seçin **yazı tipleri ve renkler** kategorisi.

   Dikkat altındaki metin **ayarlarını göster** diyor **metin düzenleyici**&mdash;istediğimiz budur. Yalnızca yerleri burada yazı tipleri ve metin rengini özelleştirebilirsiniz kapsamlı bir listesini görmek için açılan listeyi genişletin.

1. Satır numaraları metnin rengini değiştirmek için **görüntü öğeleri** listesinde **satır numarası**. İçinde **öğe ön plan** kutusunda **Zeytin**.

   ![Seçenekler iletişim kutusu, yazı tipleri ve renkler kategorisi](media/quickstart-personalize-line-number-color.png)

   Bazı diller, kendi özel yazı tipleri ve renkler ayarları vardır. C++ geliştiricisisiniz ve işlevleri için kullanılan rengi değiştirmek istediğinizde, örneğin, arayabileceğiniz **C++ işlevlerini** içinde **görüntü öğeleri** listesi.

1. Biz iletişim kutusu dışına çıkmadan önce de XML öznitelikleri rengini değiştirelim. İçinde **görüntü öğeleri** listesinde, aşağı kaydırarak **XML özniteliği** ve bu seçeneği belirleyin. İçinde **öğe ön plan** kutusunda **Küf**. Seçin **Tamam** bizim seçimlerini kaydetmek ve iletişim kutusunu kapatın.

   Satır numaraları artık Zeytin bir renk ve XML öznitelikleri, parlak Küf Yeşili. Bir C++ ya da C# kod dosyası gibi başka bir dosya türünü açarsanız, satır numaralarını Zeytin renkte göründüğünü göreceksiniz.

   ![Yeni yazı tipi renkleri olan XML dosyası](media/quickstart-personalize-xml-file-new-colors.png)

Biz, Visual Studio'daki renkler özelleştirme yalnızca birkaç yolu incelediniz. Diğer özelleştirme seçeneklerinin hakkında bilgi edineceksiniz umuyoruz **seçenekleri** iletişim kutusu, gerçek anlamda Visual Studio kendi yapma.

## <a name="see-also"></a>Ayrıca bkz.

- [Düzenleyiciyi özelleştirme](../ide/customizing-the-editor.md)
- [Visual Studio IDE’ye Genel Bakış](../get-started/visual-studio-ide.md)