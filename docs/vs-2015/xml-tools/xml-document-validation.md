---
title: XML belgesi doğrulama | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: abb353bd-6c4a-4978-b03b-a8c245bbfb55
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: bde8d47c7437700d43339bf614f48a571997dfd7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68158585"
---
# <a name="xml-document-validation"></a>XML Belgesi Doğrulama
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XML Düzenleyicisi'ni XML 1.0 sözdizimi denetler ve siz yazarken veri doğrulaması da gerçekleştirir. Düzenleyici, bir belge türü tanımı (DTD'nin) ya da bir şema kullanarak doğrulayabilirsiniz. Kırmızı dalgalı alt çizgiler, doğru biçimlendirilmiş XML 1.0 hataları vurgulayın. Mavi dalgalı alt çizgiler DTD'nin veya şema doğrulamasını anlamsal hata gösterir. Her bir hata hata listesinde bir ilişkili giriş var. Dalgalı alt çizginin fare duraklatarak, hata iletisi de görüntüleyebilirsiniz.  
  
 Doğrulama kullanılan şemalar ile eşleştirerek bulundu `targetNamespace` öğenin xmlns bildirimi ile derlenmiş bir şema. Derlenen şemalar bir öncelik sırasına göre listelenen aşağıdaki konumlara yüklenir:  
  
- Belirtilen dosya adından **şemaları** belge penceresinin alan.  
  
- Satır içi şema veya DTD'nin.  
  
- Bir dış DTD'nin veya `xsd:schemaLocation` ve `xsd:noNamespaceSchemaLocation` özniteliği  
  
- Bir "x-schema" XDR Şema ad alanı URI.  
  
  Boş hedef ad alanı şema sahip olduğunda şemaları de aşağıdaki ek konumlarda bulunabilir:  
  
- Şema içeren başka bir düzenleyici penceresi.  
  
- Geçerli çözümdeki şema.  
  
- Şema önbellek dizini bir şema.  
  
## <a name="xslt-files"></a>XSLT dosyaları  
 XSLT dosyası düzenlenirken, şema önbelleğinde bulunan xslt.xsd dosyasını doğrulaması için kullanılır. Doğrulama hatalarını, Mavi dalgalı çizgiler gösterilir. XSLT derleyici hatalarını, kırmızı dalgalı alt çizgiler gösterilir.  
  
## <a name="xml-schema-xsd-files"></a>XML Şeması (XSD) dosyaları  
 Bir XML şema dosyası düzenlenirken, şema önbelleğinde bulunan xsdschema.xsd dosyasını doğrulaması için kullanılır. Doğrulama hatalarını, Mavi dalgalı çizgiler gösterilir. Derleme hataları de dalgalı kırmızı alt çizgi ile gösterilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Düzenleyicisi](../xml-tools/xml-editor.md)
