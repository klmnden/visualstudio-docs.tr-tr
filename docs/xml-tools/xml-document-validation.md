---
title: XML Düzenleyicisi'nde XML belgesi doğrulama
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: conceptual
ms.assetid: abb353bd-6c4a-4978-b03b-a8c245bbfb55
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: eaf0ee4a039586e1f35883a2ce7a16f356f322b5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53899736"
---
# <a name="xml-document-validation"></a>XML belgesi doğrulama

XML Düzenleyicisi'ni XML 1.0 sözdizimi denetler ve siz yazarken veri doğrulaması da gerçekleştirir. Düzenleyici, bir belge türü tanımı (DTD'nin) ya da bir şema kullanarak doğrulayabilirsiniz. Kırmızı dalgalı alt çizgiler, doğru biçimlendirilmiş XML 1.0 hataları vurgulayın. Mavi dalgalı alt çizgiler DTD'nin veya şema doğrulamasını anlamsal hata gösterir. Her bir hata hata listesinde bir ilişkili giriş var. Dalgalı alt çizginin fare duraklatarak, hata iletisi de görüntüleyebilirsiniz.

 Doğrulama kullanılan şemalar ile eşleştirerek bulundu `targetNamespace` öğenin xmlns bildirimi ile derlenmiş bir şema. Derlenen şemalar bir öncelik sırasına göre listelenen aşağıdaki konumlara yüklenir:

-   Belirtilen dosya adından **şemaları** belge alanını **özellikleri** penceresi.

-   Satır içi şema veya DTD'nin.

-   Bir dış DTD'nin veya `xsd:schemaLocation` ve `xsd:noNamespaceSchemaLocation` özniteliği

-   Bir "x-schema" XDR Şema ad alanı URI.

Boş hedef ad alanı şema sahip olduğunda şemaları de aşağıdaki ek konumlarda bulunabilir:

-   Şema içeren başka bir düzenleyici penceresi.

-   Geçerli çözümdeki şema.

-   Şema önbellek dizini bir şema.

## <a name="xslt-files"></a>XSLT dosyaları
 XSLT dosyası düzenlenirken *xslt.xsd* doğrulama için şema önbelleğinde bulunan dosya kullanılır. Doğrulama hatalarını, Mavi dalgalı çizgiler gösterilir. XSLT derleyici hatalarını, kırmızı dalgalı alt çizgiler gösterilir.

## <a name="xml-schema-xsd-files"></a>XML Şeması (XSD) dosyaları
 Bir XML şema dosyası düzenlenirken *xsdschema.xsd* doğrulama için şema önbelleğinde bulunan dosya kullanılır. Doğrulama hatalarını, Mavi dalgalı çizgiler gösterilir. Derleme hataları de dalgalı kırmızı alt çizgi ile gösterilir.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)