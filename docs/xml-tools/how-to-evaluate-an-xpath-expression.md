---
title: Hata ayıklama sırasında bir XPath ifadesini değerlendirme
ms.date: 03/05/2019
ms.topic: conceptual
ms.assetid: 159ba4ef-75e4-4ac8-80dc-e064e0bec345
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1585b54d084e3471583f9388d63f5c17e65fc3a7
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526328"
---
# <a name="evaluate-xpath-expressions"></a>XPath ifadelerini değerlendirme

XPath ifadeleri kullanarak değerlendirebilirsiniz **QuickWatch** hata ayıklama sırasında penceresi. XPath ifadesi W3C XPath 1.0 öneri göre geçerli olmalıdır. Geçerli XSLT bağlam (diğer bir deyişle, `self::node()` düğümünde **Yereller** pencere) için XPath ifadesini değerlendirme bağlamı sağlar.

Bir XPath ifadesi değerlendirilirken:

- Yerleşik XPath işlevleri desteklenir.

- Yerleşik XSLT işlevleri ve kullanıcı tanımlı işlevleri desteklenmez.

> [!NOTE]
> XSLT hata ayıklama yalnızca Visual Studio Enterprise sürümünde kullanılabilir.

## <a name="evaluate-an-xpath-expression"></a>Bir XPath ifadesini değerlendirme

Aşağıdaki yordam kullanır *average.xsl aşağıda* ve *books.xml* dosyalarını [izlenecek yol: Bir XSLT stil sayfasında hata ayıklama](../xml-tools/walkthrough-debug-an-xslt-style-sheet.md#sample-files) sayfası.

1. Bir kesme noktasında Ekle `xsl:if` başlangıç etiketi.

2. Hata ayıklama başlatmak için **XML** > **XSLT hata ayıklamayı Başlat** menü çubuğunda (veya basın **Alt**+**F5** ).

   Hata ayıklayıcıyı başlatır ve üzerinde sonları `xsl:if` etiketi.

3. Sağ tıklayıp **QuickWatch**.

   **QuickWatch** penceresi açılır.

4. Girin `./price/text()` içinde **ifade** alanını **QuickWatch** iletişim kutusuna ve ardından **yeniden değerlendir**.

   Geçerli kitap düğümün fiyatı görünür **değer** kutusu.

   ![Quickwatch penceresinde bir XPath ifadesini değerlendirme](media/quickwatch-price.png)

5. XPath ifadesi değiştirme `./price/text() < $bookAverage` tıklatıp **yeniden değerlendir**.

   **Değer** kutusu gösterir XPath ifadesi olarak değerlendirilen `true`.

## <a name="see-also"></a>Ayrıca bkz.

- [XSLT Hatalarını Ayıklama](../xml-tools/debugging-xslt.md)