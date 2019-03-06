---
title: XML Düzenleyicisi'ni ve şema Tasarımcısı
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vb.xmldesigner
helpviewer_keywords:
- XML [Visual Studio], resources
- Enterprise Templates, XML and
- discovery files, XML
- server controls, XML and
- Web server controls, XML
- XSL
- XML [Visual Studio], data sources
- XML schemas
- XML [Visual Studio], SGML relationship to
- CSS, style sheets for XML
- XML [Visual Studio], .NET Framework classes
- data [Visual Studio], XML
- classes [Visual Studio], XML
- style sheets, for XML
- Web services
- SGML, XML
- XML [Visual Studio]
- datasets [Visual Basic], XML Schemas
- XSD schemas
- XSL, style sheets
- XMLDataDocument class
ms.assetid: 1fd5de47-2d61-4180-9539-c2c4bf9ab768
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a8854aee047fa961c4f0973397cfc2fe6ac6e6ad
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526574"
---
# <a name="xml-tools-in-visual-studio"></a>Visual Studio'daki XML araçları

*Genişletilebilir Biçimlendirme Dili (XML)* veri tanımlamak için bir biçim sağlayan bir biçimlendirme dilidir. XML verileri ayırır ve Genişletilebilir Stil Sayfası Dili (XSL) gibi stil sayfaları ve geçişli stil sayfaları (CSS) kullanarak kendi sunu ilişkili. Visual Studio Araçları ve şemaları XML, XSLT ve XML ile çalışmak daha kolay hale getiren özellikleri içerir.

## <a name="xml-editor"></a>XML Düzenleyicisi

[XML Düzenleyicisi](xml-editor.md) XML belgeleri düzenlemek için kullanılır. Bu, tam XML sözdizimi denetimi, şema doğrulaması sırasında tür, renk kodlaması ve IntelliSense sağlar. Bir şema veya belge türü tanımı sağlanırsa, izin verilen öğeler ve öznitelikler listelemek için IntelliSense tarafından kullanılır.

Ek özellikler şunlardır:

- Kod parçacıkları şema tarafından oluşturulan XML kod parçacığı desteği

- Belge öğeleri daraltılabilir ve genişletilebilir, anahat oluşturma

- XSLT dönüşümleri yürütmek ve sonuçları metin, XML veya HTML görüntülemek için

- XML örneği belgesinden XML Şeması Tanım Dili (XSD) şemaları oluşturma yeteneği

- IntelliSense desteği dahil olmak üzere, XSLT stil sayfalarını düzenleme desteği

- XML Şema Gezgini

## <a name="xml-schema-designer"></a>XML Şema Tasarımcısı

[XML şema Tasarımcısı](xml-schema-designer.md) XML Şeması Tanım Dili (XSD) şemaları ile çalışmayı etkinleştirmek için Visual Studio ile XML Düzenleyicisi ile tümleşiktir.

## <a name="xslt-debugging"></a>XSLT hata ayıklama

Visual Studio destekler [XSLT stil sayfalarını hata ayıklama](../xml-tools/debugging-xslt.md). Hata ayıklayıcıyı kullanarak bir XSLT stil sayfası bir XSLT stil sayfası bir adımla koddan, kesme noktaları ayarlayın ve benzeri.

> [!NOTE]
> XSLT hata ayıklayıcısı yalnızca Visual Studio Enterprise sürümünde kullanılabilir.

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Xml?displayProperty=fullName>
- [XSLT dönüşümleri](/dotnet/standard/data/xml/xslt-transformations)
- [XPath veri modelini kullanarak XML verilerini işleme](/dotnet/standard/data/xml/process-xml-data-using-the-xpath-data-model)
- [XML Belge Nesne Modeli (DOM)](/dotnet/standard/data/xml/xml-document-object-model-dom)
- [XML Şema Nesne Modeli (SOM)](/dotnet/standard/data/xml/xml-schema-object-model-som)