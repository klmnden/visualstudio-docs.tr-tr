---
title: Sıralama, filtreleme ve gruplandırma içinde XML Şeması Gezgini
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: 4a914de0-9ffc-4526-9603-92e460e52513
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: ad0c790ced2d25c63faab8260278b4e02d3015f9
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53820863"
---
# <a name="sorting-filtering-and-grouping-xml-schema-explorer"></a>Sıralama, filtreleme ve gruplandırma (XML Şeması Gezgini)

Bu konu başlığı üzerinden seçeneklerle **sıralama, filtreleme ve gruplandırma seçeneklerini** menüsünde **XML Şeması Gezgini** araç çubuğu.

## <a name="filter-options"></a>Filtre Seçenekleri

 Aşağıdaki filtre seçenekleri kullanılabilir. Varsayılan olarak, **ad alanlarını göster** ve **şema dosyalarını Göster** seçenekleri seçilidir.

-   **Ad alanlarını göster**.

-   **Şema dosyalarını Göster**.

-   **Oluşturucuları Göster (dizisi/seçim/tümü)**.

## <a name="sorting-options"></a>Sıralama seçenekleri

 Aşağıdaki sıralama seçenekleri kullanılabilir. Varsayılan değer **türe göre sırala**. **Sıralama ölçütü** seçenekleri dosyalar ve ad alanları için geçerli değildir.

-   **Türe Göre Sırala**.

-   **Ada göre sırala**.

-   **Belge sırada**.

### <a name="sort-by-type"></a>Türe göre sırala

 Zaman **türe göre sırala** seçeneği seçildiğinde, genel düğümler, aşağıdaki düzende sıralanır. Düğüm, her grup alfabetik olarak sıralanır.

1.  `import` düğümleri.

2.  `include` düğümleri.

3.  `redefine` düğümleri.

4.  `attribute` düğümleri.

5.  `attributeGroup` düğümleri.

6.  `complexType` düğümleri.

7.  `simpleType` düğümleri.

8.  `element` düğümleri.

9. `group` düğümleri.

### <a name="sort-by-name"></a>Ada göre sırala

 Zaman **ada göre sırala** seçeneği seçildiğinde, genel düğümler, aşağıdaki düzende sıralanır:

1.  `import` düğümleri (alfabetik sırada ad alanları).

2.  `include` düğümleri (alfabetik sırada `schemaLocation` öznitelikleri).

3.  `redefine` düğümleri (alfabetik sırada `schemaLocation` öznitelikleri).

4.  Genel diğer düğümlere alfabetik olarak sıralayın.

### <a name="document-order"></a>Belge sırada

 **Belge sırada** seçeneği kullanılabilir olduğunda **şema dosyalarını Göster** seçeneği belirlenir. Zaman **belge sırada** seçildiğinde genel düğümler, şema dosyasında göründükleri sırada görüntülenir.

## <a name="persisting-sortfilter-options"></a>Kalıcı sıralama/filtre seçenekleri

 Sıralama, filtreleme ve gruplandırma Seçenekleri ayarları değiştirildi ne olursa olsun, çözüm veya dosya açıktı her bir kullanıcı için kayıt defterine kaydedildi.