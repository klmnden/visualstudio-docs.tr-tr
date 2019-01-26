---
title: 'İzlenecek yol: XSLT IntelliSense kullanma'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 079d95ac-2eaf-4ae1-9cd3-2c81a961a942
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3bef2b535541657b37bd085c70843cca0a6394ff
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55001413"
---
# <a name="walkthrough-using-xslt-intellisense"></a>İzlenecek yol: XSLT IntelliSense kullanma

Bu yönerge, XSLT IntelliSense otomatik tamamlama için bazı özniteliklerin değeri kullanma işlemini gösterir.

## <a name="to-use-intellisense-in-the-name-attribute-of-xslwith-param-and-xslcall-template-elements"></a>Xsl ad özniteliğinde IntelliSense kullanılacak: param ile ve Call-şablon öğeleri

1.  Aşağıdaki kodda, yeni XSLT dosyası ve kopya oluşturun:

    ```xml
    <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
    <!-- These 2 elements effectively assign
         $messages = resources/en.xml/<messages>,
         then $messages is used in the "localized-message" template.  -->
    <xsl:param name="lang">en</xsl:param>
    <xsl:variable name="messages"
          select="document(concat('resources/', $lang, '.xml'))/messages"/>

    <xsl:template name="msg23" match="msg23">
    </xsl:template>

    <xsl:template name="localized-message">
      <xsl:param name="msgcode"/>
      <!-- Show message string. -->
      <xsl:message terminate="yes">
        <xsl:value-of select="$messages/message[@name=$msgcode]"/>
      </xsl:message>
    </xsl:template>
    </xsl:stylesheet>
    ```

2.  İmlecinizi sonra Ekle `<xsl:template name="msg23" match="msg23">` basın **Enter**. Aşağıdaki yazmaya başlayın `xsl:call-template` öğesi:

    ```xml
    <xsl:call-template name="localized-message">
    </xsl:call-template>
    ```

     Şablon adları listesi görünür `name=""` özniteliği `xsl:call-template` yazarken öğesi.

3.  İmlecinizi sonra Ekle `<xsl:call-template name="localized-message">` basın **Enter**. Aşağıdaki yazmaya başlayın `xsl:with-param` öğesi:

    ```xml
    <xsl:with-param name="msgcode">msg23</xsl:with-param>
    ```

     Parametre adları listesi görünür `name=""` özniteliği `xsl:with-param` öğesi.

## <a name="to-use-intellisense-in-the-mode-attribute-of-an-xslapply-templates-element"></a>Xsl modu özniteliğinde IntelliSense kullanmak için: Uygulama Şablonları öğesi

1.  Aşağıdaki kodda, yeni XSLT dosyası ve kopya oluşturun:

    ```xml
    <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" version="1.0">
      <xsl:template match="/">
        <HTML>
          <BODY>
            <TABLE>
              <xsl:apply-templates select="customers/customer">
                <xsl:sort select="state"/>
                <xsl:sort select="name"/>
              </xsl:apply-templates>
            </TABLE>
          </BODY>
        </HTML>
      </xsl:template>
      <xsl:template match="customer">
        <TR>
          <xsl:apply-templates select="name" />
          <xsl:apply-templates select="address" />
          <xsl:apply-templates select="phone" />
        </TR>
      </xsl:template>
      <xsl:template match="name">
        <TD STYLE="font-size:14pt font-family:serif">
          <xsl:apply-templates />
        </TD>
      </xsl:template>
      <xsl:template match="address">
        <TD>
          <xsl:apply-templates />
        </TD>
      </xsl:template>
      <xsl:template match="phone">
        <TD>
          <xsl:apply-templates />
        </TD>
      </xsl:template>
      <xsl:template match="phone" mode="accountNumber">
        <xsl:param name="Area_Code"/>
        <TD STYLE="font-style:italic">
          1-<xsl:value-of select="."/>-001
        </TD>
      </xsl:template>
    </xsl:stylesheet>
    ```

2.  İmlecinizi sonra Ekle `<xsl:apply-templates select="phone" />` basın **Enter**. Aşağıdaki yazmaya başlayın `xsl: apply-templates` öğesi:

    ```xml
    <xsl:apply-templates select="phone"  mode="accountNumber">
    ```

     Şablon modlarının listesi görünür `mode=""` özniteliği `xsl:apply-templates` öğesi.

## <a name="to-use-intellisense-in-the-stylesheet-prefix-and-result-prefix-attributes-of-an-xslnamespace-alias-element"></a>IntelliSense bir xsl: namespace stil sayfası öneki ve sonuç önek öznitelikleri kullanılacak-diğer ad öğesi

1.  Aşağıdaki kodda, yeni XSLT dosyası ve kopya oluşturun:

    ```xml
    <xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:alt="http://www.w3.org/1999/XSL/Transform-alternate"
    version="1.0">
      <xsl:param name="browser" select="'InternetExplorer'"/>
      <xsl:template match="/">
        <alt:stylesheet>
          <xsl:choose>
            <xsl:when test="$browser='InternetExplorer'">
              <alt:import href="IERoutines.xsl"/>
              <alt:template match="/">
                <div>
                  <alt:call-template name="showTable"/>
                </div>
              </alt:template>
            </xsl:when>
            <xsl:otherwise>
              <alt:import href="OtherBrowserRoutines.xsl"/>
              <alt:template match="/">
                <div>
                  <alt:call-template name="showTable"/>
                </div>
              </alt:template>
            </xsl:otherwise>
          </xsl:choose>
        </alt:stylesheet>
      </xsl:template>
    </xsl:stylesheet>
    ```

2.  İmlecinizi sonra Ekle `<xsl:stylesheet xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:alt="http://www.w3.org/1999/XSL/Transform-alternate" version="1.0">` basın **Enter**. Aşağıdaki yazmaya başlayın `xsl:namespace-alias` öğesi:

    ```xml
    <xsl:namespace-alias stylesheet-prefix="alt" result-prefix="xsl"/>
    ```

     Ön ek listesini nasıl göründüğü fark `stylesheet-prefix` ve `result-prefix` özniteliklerini `xsl:namespace-alias` öğesi.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi IntelliSense özellikleri](../xml-tools/xml-editor-intellisense-features.md)