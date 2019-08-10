---
title: XML şema Gezgininde sıralama, filtreleme ve gruplandırma
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 4a914de0-9ffc-4526-9603-92e460e52513
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: daa629b4c26abf7b6ce801c30ea6f6fd41fbaa48
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926727"
---
# <a name="sorting-filtering-and-grouping-xml-schema-explorer"></a>Sıralama, filtreleme ve gruplandırma (XML şema Gezgini)

Bu konu başlığı altında, **XML şema Gezgini** araç çubuğundaki **sıralama, filtreleme ve gruplandırma seçenekleri** menüsünde bulunan seçenekler açıklanmaktadır.

## <a name="filter-options"></a>Filtre seçenekleri

Aşağıdaki filtre seçenekleri kullanılabilir. Varsayılan olarak, **ad alanlarını göster** ve **şema dosyalarını göster** seçenekleri seçilidir.

- **Ad alanlarını göster**.

- **Şema dosyalarını göster**.

- Oluşturucuları **göster (Sequence/Choice/All)** .

## <a name="sorting-options"></a>Sıralama seçenekleri

Aşağıdaki sıralama seçenekleri kullanılabilir. Varsayılan değer **türe göre sıralanır**. Seçeneklere **göre sırala** , dosyalar ve ad alanları için geçerlidir.

- **Türe göre sırala**.

- **Ada göre sıralayın**.

- **Belge sırası**.

### <a name="sort-by-type"></a>Türe göre sırala

**Türe göre sırala** seçeneği belirlendiğinde, genel düğümler aşağıdaki sırada sıralanır. Daha sonra düğümler her grup içinde alfabetik olarak sıralanır.

1. `import`düğümlerini.

2. `include`düğümlerini.

3. `redefine`düğümlerini.

4. `attribute`düğümlerini.

5. `attributeGroup`düğümlerini.

6. `complexType`düğümlerini.

7. `simpleType`düğümlerini.

8. `element`düğümlerini.

9. `group`düğümlerini.

### <a name="sort-by-name"></a>Ada göre sırala

**Ada göre sırala** seçeneği belirlendiğinde, genel düğümler aşağıdaki sıraya göre sıralanır:

1. `import`düğümler (ad alanlarının alfabetik sırasıyla).

2. `include`düğümler ( `schemaLocation` özniteliklerin alfabetik sırasına göre).

3. `redefine`düğümler ( `schemaLocation` özniteliklerin alfabetik sırasına göre).

4. Alfabetik sırada diğer genel düğümler.

### <a name="document-order"></a>Belge sırası

**Belge sırası** seçeneği, **şema dosyalarını göster** seçeneği belirlendiğinde kullanılabilir. **Belge sırası** seçildiğinde, genel düğümler, şema dosyasında göründükleri sırada görüntülenir.

## <a name="persisting-sortfilter-options"></a>Kalıcı sıralama/filtre seçenekleri

Sıralama, filtreleme ve gruplandırma seçenekleri, her kullanıcı için kayıt defterine kaydedilir, bu da ayarlar değiştirildiğinde hangi çözüm veya dosyaların açık olduğuna bakılmaksızın.