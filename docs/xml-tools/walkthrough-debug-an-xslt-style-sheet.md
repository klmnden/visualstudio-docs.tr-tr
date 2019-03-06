---
title: XSLT stil sayfalarını hata ayıklama
ms.date: 03/05/2019
ms.topic: conceptual
ms.assetid: 3db9fa5a-f619-4cb6-86e7-64b364e58e5d
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e787ca3d2d29f04d6af27a5f36f1f84c9d0bc9f4
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526639"
---
# <a name="walkthrough-debug-an-xslt-style-sheet"></a>İzlenecek yol: Bir XSLT stil sayfasında hata ayıklama

Bu kılavuzda açıklanan adımları XSLT hata ayıklayıcının kullanımını göstermektedir. Değişkenleri görüntüleme, kesme noktaları ayarlama ve kod içerisinde ilerlemeye adımlar içerir. Hata ayıklayıcı bir defada bir satır kod yürütmek vermenize olanak tanır.

Bu kılavuz için hazırlamak için ilk iki kopyalama [örnek dosyaları](#sample-files) yerel bilgisayarınıza. Bir stil sayfası ve bir stil sayfası için giriş olarak kullanacağız XML dosyasıdır. Bu kılavuzda kullandığımız stil sayfası maliyeti ortalama kitap fiyat altında olan tüm kitaplar bulur.

> [!NOTE]
> XSLT hata ayıklayıcısı yalnızca Visual Studio Enterprise sürümünde kullanılabilir.

## <a name="start-debugging"></a>Hata Ayıklamayı Başlat

1. Gelen **dosya** menüsünde seçin **açık** > **dosya**.

2. Bulun *average.xsl aşağıda* seçin ve dosya **açık**.

   Stil sayfası XML Düzenleyicisi'nde açılır.

3. Gözat düğmesine tıklayın (**...** ) üzerinde **giriş** belge penceresinin alan. (Varsa **özellikleri** penceresi görünmüyorsa, dosyayı düzenleyicide Aç herhangi bir yere sağ tıklayın ve ardından **özellikleri**.)

4. Bulun *books.xml* dosya ve ardından **açık**.

   Bu XSLT dönüşümü için kullanılan kaynak dosyanın ayarlar.

5. Ayarlanmış bir [kesme noktası](../debugger/using-breakpoints.md) üzerinde 12. satırın *average.xsl aşağıda*. Birden çok yolla bunu yapabilirsiniz:

   - 12 satırındaki Düzenleyici kenar boşluğunda tıklayın.

   - 12. satırda herhangi bir yere tıklayın ve sonra basın **F9**.

   - Sağ `xsl:if` başlangıç etiketi ve ardından **kesme noktası** > **kesme noktası Ekle**.

      ![Visual Studio XSL dosyasında kesme noktası Ekle](media/insert-breakpoint.PNG)

6. Menü çubuğunda, **XML** > **XSLT hata ayıklamayı Başlat** (veya basın **Alt**+**F5**).

   Hata ayıklama işlemini başlatır.

   Düzenleyici'de, hata ayıklayıcı üzerinde konumlandırılmış `xsl:if` stil sayfası öğesi. Adlı başka bir dosya *average.xml aşağıda* Düzenleyicisi'nde; açılır girdi dosyasındaki her bir düğüm olarak doldurulacak çıkış dosyası budur *books.xml* işlenir.

   **Otolar**, **Yereller**, ve **Watch 1** windows Visual Studio penceresinin en altında görünür. **Yereller** penceresi, tüm yerel değişkenlerin ve geçerli değerlerini görüntüler. Bu stil sayfası ve ayrıca hata ayıklayıcı şu anda bağlam içinde olan düğümleri izlemek için kullandığı değişkenleri tanımlanan değişkenler içerir.

## <a name="watch-window"></a>Gözcü penceresi

İki değişken için ekleyeceğiz **Watch 1** giriş dosyası işlendi olarak biz değerlerini incelemeniz penceresi. (Ayrıca **Yereller** penceresini izlemek istediğiniz değişken zaten varsa, değerleri inceleyin.)

1. Gelen **hata ayıklama** menüsünde seçin **Windows** > **Watch** > **Watch 1**.

   **Watch 1** pencere görünür olur.

2. Tür `$bookAverage` içinde **adı** alan ve sonra basın **Enter**.

   Değerini `$bookAverage` değişkeni görüntüler **değer** alan.

3. Sonraki satıra yazın `self::node()` içinde **adı** alan ve sonra basın **Enter**.

   `self::node()` Geçerli bağlam düğümünün için değerlendirilen bir XPath ifadesidir. Değerini `self::node()` XPath ifadesidir ilk kitap düğümü. Bu dönüşüm ilerledikçe değiştirir.

4. Genişletin `self::node()` düğümünü ve sonra düğümü genişletmek kimin sahip değer `price`.

   ![XSLT Visual Studio'da hata ayıklama sırasında izleme penceresi](media/xslt-debugging-watch-window.png)

   Kitap fiyatı geçerli kitap düğümün değerini görmek ve karşılaştırmak için `$bookAverage` değeri. Kitap fiyat Ortalamanın altında olduğundan `xsl:if` hata ayıklama işlemi devam ederken koşul başarılı.

## <a name="step-through-the-code"></a>Kodunuz içinde adım adım

1. Tuşuna **F5** devam etmek için.

   İlk kitap düğümün memnun çünkü `xsl:if` koşulu, kitap düğümün eklenen *average.xml aşağıda* çıkış dosyası. Hata ayıklayıcı üzerinde yeniden konumlandırılmış kadar yürütülmeye devam `xsl:if` stil sayfası öğesinde. Hata ayıklayıcı Şimdi ikinci kitap düğümün konumlandırılmış *books.xml* dosya.

   İçinde **Watch 1** penceresinde `self::node()` için ikinci kitap düğümün değerini değiştirir. Fiyat öğenin değerini inceleyerek fiyat ortalamanın üstünde, bu nedenle olduğunu anlayabilirsiniz `xsl:if` koşul başarısız olmalıdır.

2. Tuşuna **F5** devam etmek için.

   İkinci kitap düğümün karşılamıyorsa çünkü `xsl:if` koşulu, kitap düğümün eklenmez *average.xml aşağıda* çıkış dosyası. Hata ayıklayıcı üzerinde yeniden konumlandırılmış kadar yürütülmeye devam `xsl:if` stil sayfası öğesinde. Hata ayıklayıcısı artık üçüncü konumlandırıldı `book` düğümünde *books.xml* dosya.

   İçinde **Watch 1** penceresinde `self::node()` üçüncü kitap düğümün değerini değiştirir. Değerini inceleme tarafından `price` öğesi, fiyat Ortalamanın altında olduğunu belirleyebilirsiniz. `xsl:if` Koşul başarılı olması gerekir.

3. Tuşuna **F5** devam etmek için.

   Çünkü `xsl:if` koşulu karşılandı üçüncü kitap eklenir *average.xml aşağıda* çıkış dosyası. XML belgesi içindeki tüm kitaplar işlenen ve hata ayıklayıcıyı durdurur.

## <a name="sample-files"></a>Örnek dosya

Aşağıdaki iki dosyada izlenecek yol tarafından kullanılır.

### <a name="below-averagexsl"></a>Aşağıda average.xsl

```xml
<?xml version='1.0'?>
<xsl:stylesheet version="1.0"
      xmlns:xsl="http://www.w3.org/1999/XSL/Transform">
  <xsl:output method="xml" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:variable name="bookCount" select="count(/bookstore/book)"/>
    <xsl:variable name="bookTotal" select="sum(/bookstore/book/price)"/>
    <xsl:variable name="bookAverage" select="$bookTotal div $bookCount"/>
    <books>
      <!--Books That Cost Below Average-->
      <xsl:for-each select="/bookstore/book">
        <xsl:if test="price &lt; $bookAverage">
          <xsl:copy-of select="."/>
        </xsl:if>
      </xsl:for-each>
    </books>
  </xsl:template>
</xsl:stylesheet>
```

### <a name="booksxml"></a>Books.XML

```xml
<?xml version='1.0'?>
<!-- This file represents a fragment of a book store inventory database -->
<bookstore>
  <book genre="autobiography" publicationdate="1981" ISBN="1-861003-11-0">
    <title>The Autobiography of Benjamin Franklin</title>
    <author>
      <first-name>Benjamin</first-name>
      <last-name>Franklin</last-name>
    </author>
    <price>8.99</price>
  </book>
  <book genre="novel" publicationdate="1967" ISBN="0-201-63361-2">
    <title>The Confidence Man</title>
    <author>
      <first-name>Herman</first-name>
      <last-name>Melville</last-name>
    </author>
    <price>11.99</price>
  </book>
  <book genre="philosophy" publicationdate="1991" ISBN="1-861001-57-6">
    <title>The Gorgias</title>
    <author>
      <name>Plato</name>
    </author>
    <price>9.99</price>
  </book>
</bookstore>
```

## <a name="see-also"></a>Ayrıca bkz.

- [XSLT Hatalarını Ayıklama](../xml-tools/debugging-xslt.md)