---
title: 'İzlenecek yol: XSLT hiyerarşisi kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 5e60c8ec-cd05-4597-b856-55038218acf4
caps.latest.revision: 8
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: ed644c1dda4ac3674ef60d0027c37532fc6d0f92
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60075630"
---
# <a name="walkthrough-using-xslt-hierarchy"></a>İzlenecek yol: XSLT hiyerarşisi kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XSLT hiyerarşisi araç birçok XML geliştirme görevlerinizi basitleştirir. Genellikle bir XSLT stil sayfası kullanan `includes` ve `imports` yönergeleri. Derleme asıl stil sayfası içinden başlatır, ancak bir hata sonucunda bir XSLT stil sayfası derleme gördüğünüzde, hata asıl stil sayfası başka bir kaynaktan gelebilir. Hatanın düzeltilmesi veya stil sayfası düzenleme eklenen veya içeri aktarılan stil sayfaları için erişim gerektirebilir. Stil sayfasında hata ayıklayıcı ile Adımlama dahildir ve içeri aktarılan stil sayfaları açabilir ve bir veya daha fazlası dahil stil sayfaları belirli bir noktada bir kesme noktası eklemek isteyebilirsiniz.  
  
 Başka bir senaryo Burada XSLT hiyerarşisi araç yararlı olabilir, yerleşik bir şablon kuralları üzerinde kesme noktaları koyuyor. Özel şablonlar için stil sayfası her modu oluşturulur ve tarafından çağrılabilir şablon kuralları `xsl:apply-templates` zaman başka bir şablonu eşleşen düğüm. Yerleşik şablonlar kurallarında hata ayıklama uygulamak için XSLT hata ayıklayıcısı kurallarla dosyanın geçici klasörde oluşturur ve bunları birlikte asıl stil sayfası derler. Bazı kodun içine Adımlama olmadan `xsl:apply-template`, asıl stil sayfasında dahil stil sayfaları bulun veya bulmak ve stil sayfası ile yerleşik bir şablon kuralları açmak zor olabilir.  
  
 Bu konudaki örnek, bir başvurulan stil sayfasında hata ayıklama gösterir.  
  
### <a name="procedure-title"></a>Yordam başlığı  
  
1. Bir XML belgesi Visual Studio'da açın. Bu örnekte aşağıdaki `collection.xml` belge.  
  
    ```  
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
  
2. Aşağıdaki `xslincludefile.xsl`:  
  
    ```  
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
  
3. Aşağıdaki `xslinclude.xsl` dosyası:  
  
    ```  
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
  
4. Bir kesme noktası yönerge ekleyin: `<xsl:include href="xslincludefile.xsl" />`  
  
5. Hata ayıklama başlatılamıyor.  
  
6. Hata ayıklayıcı yönerge durduğunda `<xsl:include href="xslincludefile.xsl" />`, adımla düğmesine basın. Hata ayıklama başvurulan stil sayfasına devam ettirilemez olduğunu unutmayın. Hiyerarşi görünür ve tasarımcı doğru yolunu görüntüler.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [İzlenecek yol: XSLT Profil Oluşturucu](../xml-tools/walkthrough-xslt-profiler.md)
