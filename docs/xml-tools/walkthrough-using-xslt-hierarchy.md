---
title: 'İzlenecek yol: XSLT hiyerarşisi kullanma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: dcbb61e0a23d1a530d9c104337454b7a8ba66ca7
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55020769"
---
# <a name="walkthrough-use-xslt-hierarchy"></a>İzlenecek yol: XSLT hiyerarşisi kullanma

XSLT hiyerarşisi araç birçok XML geliştirme görevlerinizi basitleştirir. Genellikle bir XSLT stil sayfası kullanan `includes` ve `imports` yönergeleri. Derleme asıl stil sayfası içinden başlatır, ancak bir hata sonucunda bir XSLT stil sayfası derleme gördüğünüzde, hata asıl stil sayfası başka bir kaynaktan gelebilir. Hatanın düzeltilmesi veya stil sayfası düzenleme eklenen veya içeri aktarılan stil sayfaları için erişim gerektirebilir. Stil sayfasında hata ayıklayıcı ile Adımlama dahildir ve içeri aktarılan stil sayfaları açabilir ve bir veya daha fazlası dahil stil sayfaları belirli bir noktada bir kesme noktası eklemek isteyebilirsiniz.

Başka bir senaryo Burada XSLT hiyerarşisi araç yararlı olabilir, yerleşik bir şablon kuralları üzerinde kesme noktaları koyuyor. Özel şablonlar için stil sayfası her modu oluşturulur ve tarafından çağrılabilir şablon kuralları `xsl:apply-templates` zaman başka bir şablonu eşleşen düğüm. Yerleşik şablonlar kurallarında hata ayıklama uygulamak için XSLT hata ayıklayıcısı kurallarla dosyanın geçici klasörde oluşturur ve bunları birlikte asıl stil sayfası derler. Bazı kodun içine Adımlama olmadan `xsl:apply-template`, asıl stil sayfasında dahil stil sayfaları bulun veya bulmak ve stil sayfası ile yerleşik bir şablon kuralları açmak zor olabilir.

Bu konudaki örnek, bir başvurulan stil sayfasında hata ayıklama gösterir.

## <a name="to-debug-in-a-referenced-style-sheet"></a>Başvurulan stil sayfasında hata ayıklamak için

1. Bir XML belgesi Visual Studio'da açın. Bu örnek aşağıdaki belge kullanır:

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <?xml-stylesheet type="text/xsl" href="xslinclude.xsl"?>
    <COLLECTION>
      <BOOK>
        <TITLE>Lover Birds</TITLE>
        <AUTHOR>Cynthia Randall</AUTHOR>
        <PUBLISHER>Lucerne Publishing</PUBLISHER>
      </BOOK>
      <BOOK>
        <TITLE>The Sundered Grail</TITLE>
        <AUTHOR>Eva Corets</AUTHOR>
        <PUBLISHER>Lucerne Publishing</PUBLISHER>
      </BOOK>
      <BOOK>
        <TITLE>Splish Splash</TITLE>
        <AUTHOR>Paula Thurman</AUTHOR>
        <PUBLISHER>Scootney</PUBLISHER>
      </BOOK>
    </COLLECTION>
    ```

1. Aşağıdaki *xslincludefile.xsl*:

    ```xml
    <?xml version='1.0'?>
    <xsl:stylesheet version="1.0"
          xmlns:xsl="http://www.w3.org/1999/XSL/Transform"
          xml:space="preserve">

    <xsl:template match="TITLE">
       Title - <xsl:value-of select="."/><BR/>
    </xsl:template>

    <xsl:template match="AUTHOR">
       Author - <xsl:value-of select="."/><BR/>
    </xsl:template>

    <xsl:template match="PUBLISHER">
       Publisher - <xsl:value-of select="."/><BR/><!-- removed second <BR/> -->
    </xsl:template>

    </xsl:stylesheet>
    ```

3.  Aşağıdaki *xslinclude.xsl* dosyası:

    ```xml
    <?xml version='1.0'?>
    <xsl:stylesheet version="1.0"
          xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

      <xsl:output method="xml" omit-xml-declaration="yes"/>

      <xsl:template match="/">
        <xsl:for-each select="COLLECTION/BOOK">
          <xsl:apply-templates select="TITLE"/>
          <xsl:apply-templates select="AUTHOR"/>
          <xsl:apply-templates select="PUBLISHER"/>
          <BR/>
          <!-- add this -->
        </xsl:for-each>
      </xsl:template>

      <!-- The following template rule will not be called,
      because the related template in the including stylesheet
      is called. If we move this template so that
      it follows the xsl:include instruction, this one
      will be called instead.-->
      <xsl:template match="TITLE">
        <DIV STYLE="color:blue">
          Title: <xsl:value-of select="."/>
        </DIV>
      </xsl:template>

      <xsl:include href="xslincludefile.xsl" />
    </xsl:stylesheet>
    ```

4.  Yönerge bir kesme noktası ekleyin `<xsl:include href="xslincludefile.xsl" />`.

5.  Hata ayıklama başlatılamıyor.

6.  Hata ayıklayıcı yönerge durduğunda `<xsl:include href="xslincludefile.xsl" />`, basın **içine adımla** düğmesi. Hata ayıklama başvurulan stil sayfasına devam edebilir. Hiyerarşi görünür ve tasarımcı doğru yolunu görüntüler.

## <a name="see-also"></a>Ayrıca bkz.

- [İzlenecek yol: XSLT Profil Oluşturucusu](../xml-tools/walkthrough-xslt-profiler.md)