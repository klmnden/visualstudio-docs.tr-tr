---
title: 'Nasıl Yapılır: Bir XPath İfadesini Değerlendirme'
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 159ba4ef-75e4-4ac8-80dc-e064e0bec345
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: eac1668a5d85f1f40d6defe4682f028674b5bf0c
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53838654"
---
# <a name="how-to-evaluate-an-xpath-expression"></a>Nasıl Yapılır: Bir XPath İfadesini Değerlendirme

XPath ifadeleri ile değerlendirebilirsiniz **QuickWatch** iletişim kutusu. XPath ifadesi W3C XPath 1.0 öneri göre geçerli olmalıdır. Geçerli XSLT bağlam — diğer bir deyişle, `self::node()` düğümünde **Yereller** penceresi — için XPath ifadesini değerlendirme bağlamı sağlar.

 Aşağıdaki listede, hangi işlevlerin bir XPath ifadesi değerlendirilirken desteklenen açıklanmaktadır:

-   Yerleşik XPath işlevleri desteklenir.

-   Yerleşik XSLT işlevleri desteklenmez.

-   Kullanıcı tanımlı işlevleri desteklenmez.

> [!NOTE]
> Aşağıdaki yordam kullanır *belowAvg.xsl* ve *books.xml* dosyalarını [izlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md) konu.

## <a name="to-evaluate-an-xpath-expression"></a>Bir XPath ifadesini değerlendirme

1.  Bir kesme noktasında Ekle `xsl:if` başlangıç etiketi.

2.  Tıklayın **hata ayıklama XSL** XML Düzenleyicisi araç çubuğu düğmesi.

     Hata ayıklayıcıyı başlatır ve üzerinde sonları `xsl:if` etiketi.

3.  Sağ tıklayıp **QuickWatch**.

     **QuickWatch** iletişim kutusu görüntülenir.

4.  Girin `./price/text()` içinde **ifade** alanını **QuickWatch** iletişim kutusu ve tıklatın **yeniden değerlendir**.

     Geçerli kitap düğümün fiyatı görünür **değer** kutusu.

5.  XPath ifadesi değiştirme `./price/text() < $bookAverage` tıklatıp **yeniden değerlendir**.

     **Değer** kutusu gösterir XPath ifadesi olarak değerlendirilen `true`.

## <a name="see-also"></a>Ayrıca bkz.

- [XSLT Hatalarını Ayıklama](../xml-tools/debugging-xslt.md)