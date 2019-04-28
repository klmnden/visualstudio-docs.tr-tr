---
title: XML şemaları
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.xmleditor.schemasdialog
ms.assetid: 0271fa26-2205-49bd-96e0-ae1441571808
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f5323582bfe945bc031b9fd02fcf96bb615bcceb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62807951"
---
# <a name="xml-schemas-dialog-box"></a>XML Şemaları iletişim kutusu

**XML şemaları** iletişim kutusu, bir XML belgesi ile ilişkilendirmek için hangi XML Şeması Tanım Dili (XSD) şeması/şemaları seçmek için kullanılır. Şema önbelleğinden bir şema seçin veya önbelleğinde bulunmayan bir şema belirtin. Seçili şemaları şema kümesinin bir parçası olarak kabul edilir. Şema kümesi, IntelliSense ve ayrıca XML belgesi doğrulama için kullanılır.

Erişebildiğiniz **XML şemaları** ya tıklayarak iletişim kutusunu **şemaları** düğmesini seçerek veya belge Özellikler penceresinde **şemaları** gelen**XML** menüsü.

## <a name="uielement-list"></a>UIElement Listesi

**Kullanma**

XML Şeması nasıl kullanıldığının seçin.

- **Otomatik**. Bu şema geçerli belgede tarafından'kullanımda değildir, ancak otomatik ilişkilendirmesi için kullanılabilir. XML belgesi eşleşen bir ad alanı bildirirse `targetNamespace` bu şema şema otomatik olarak ilişkilendirilir ve şema kümesindeki dahil edilir.

- **Bu şemayı kullan**. Bu şemayı geçerli belgede tarafından kullanılıyor. Açıkça ya da kullanıcının sahip olduğu bu sütuna tıklayarak bu şema kullanılması istenen veya şema eşleşmesi temeline göre otomatik olarak ilişkili `targetNamespace`.

- **Seçili şemaları kullanma**. Eşleşen bir şemaya sahip olsa bile bu şemayı geçerli belgede tarafından kullanılmaz `targetNamespace`. Bu ayar şema önbelleği veya çözüm aynı şemaya yönelik birden fazla sürümü olduğunda çakışmaları çözümlemek için yararlı olabilir.

**Target Namespace**

XML şeması ile ilişkili hedef ad alanı görüntüler.

**Dosya adı**

XML Şeması dosya adını görüntüler.

**Add**

Açılır **açık XSD şeması** form veya iletişim şema kümesine eklenecek ek şemaları seçmenize olanak sağlar. Şema için bir şema eklediğinizde ayarlayın, **kullanım** sütun değeri ayarı **Bu şemayı kullan**.

**Kaldır**

Şu anda seçili şeması, şema kümeden kaldırır. Bu, bellek içi şema önbelleğinden ancak dosya sisteminden şemayı kaldırır.

## <a name="see-also"></a>Ayrıca bkz.

- [Nasıl yapılır: Kullanılacak XML şemalarını seçin](../xml-tools/how-to-select-the-xml-schemas-to-use.md)
- [Şema önbelleği](../xml-tools/schema-cache.md)