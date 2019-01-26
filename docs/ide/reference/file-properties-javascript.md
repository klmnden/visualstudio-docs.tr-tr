---
title: Dosya Özellikleri, JavaScript
ms.date: 06/21/2017
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
- javascript.project.property.expandedsdknode.fileversion
- javascript.project.property.expandedsdknode.uri
- javascript.project.property.expandedsdknode.filename
- javascript.project.property.reference.description
- javascript.project.property.reference.specificversion
- javascript.project.property.reference.identity
- javascript.project.property.fullpath
- javascript.project.property.packageaction
- javascript.project.property.reference.package
- javascript.project.property.copytooutputdirectory
- javascript.project.property.expandedsdknode.sdkpath
- javascript.project.property.reference.filetype
- javascript.project.property.reference.culture
- javascript.project.property.filename
- javascript.project.property.reference.resolvedpath
- javascript.project.property.reference.version
ms.assetid: 085913b8-a97b-45f7-85fa-bbb0902f3ee9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9fc9832ba7774f58d5f1826e633dfd9bf24ce205
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54946548"
---
# <a name="file-properties-javascript"></a>Dosya Özellikleri, JavaScript
Dosya özellikleri, proje sistemi dosyalarda gerçekleştirmesi gereken eylemleri belirtmek için kullanabilirsiniz. Örneğin, bir dosya için paket kaynak dosyası olarak eklenmesi gerekip gerekmediğini belirtmek için dosya özelliklerini ayarlayabilirsiniz.

 Çözüm Gezgini'nde herhangi bir dosya seçin ve ardından Özellikler penceresindeki özelliklerini inceleyin. JavaScript dosyaları dört özelliklere sahiptir: **Çıkış Dizinine Kopyala**, **paket eylemi**, **dosya adı**, ve **dosya yolu**.

## <a name="file-properties"></a>Dosya özellikleri
 Bu bölümde, JavaScript dosyaları için ortak olan özellikleri açıklanmaktadır.

### <a name="copy-to-output-directory-property"></a>Çıkış dizini özelliğini kopyalayın
 Bu özellik, koşullar altında seçili kaynak dosyasının çıkış dizinine kopyalanır belirtir. Seçin **kopyalamayın** dosya hiçbir zaman çıkış dizinine kopyalanacak ise. Seçin **her zaman Kopyala** dosyası her zaman çıkış dizinine kopyalanacak ise. Seçin **yeniyse Kopyala** yalnızca çıktı dizininde aynı ada sahip mevcut bir dosyayı daha yeni olduğunda kopyalanacak dosya olduğunda.

### <a name="package-action"></a>Paket eylemi
 **Paket eylemi** özelliği, bir yapı çalıştırıldığında Visual Studio ile bir dosyanın ne yaptığını gösterir. **Paket eylemi** değerlerden biri olabilir:

-   **Hiçbiri** -dosya paketi bildiriminde yer almaz. Örnek bir benioku dosyası gibi bir belge içeren bir metin dosyasıdır.

-   **İçerik** -dosya paketi bildiriminde bulunur. Örneğin, bu ayar bir .htm, .js, .css, görüntü, ses veya video dosyası için varsayılan değerdir.

-   **Bildirim** -dosya paketi bildiriminde yer almaz. Bunun yerine, dosya girişi için paket bildirimi oluşturulurken kullanılır. Package.appxmanifest dosyasını için varsayılan değer budur.

-   **Kaynak** -dosya paketi bildiriminde yer almaz. Bunun yerine, paket kaynak dizini (PRI) içinde paket bildirimi gider dosyasının içeriği dizine eklenir. Genellikle, kaynak dosyaları için de kullanılır.

İçin varsayılan değer **paket eylemi** çözüme ekleyin dosya uzantısını bağlıdır.

### <a name="file-name-property"></a>Dosya adı özelliği
 Dosya adı salt okunur bir değer görüntüler. Dosyayı yeniden adlandırmak için Çözüm Gezgini'nde sağ tıklayıp seçin **Yeniden Adlandır**.

### <a name="full-path-property"></a>Tam yol özelliği
 Tam yolunu dosyaya salt okunur bir değer görüntüler. Dosya yolunu değiştirmek için sürükle ve bırak Çözüm Gezgini'nde dosyayı kullanabilirsiniz.

## <a name="reference-file-properties"></a>Başvuru dosyası özellikleri
 Bu bölümde, JavaScript kullanılarak oluşturulan bir UWP uygulaması başvurulan dosyaları için ortak olan özellikleri açıklanmaktadır. Çözüm Gezgini'nde bir .winmd dosyası, bir SDK başvurusu, projeden projeye başvuru veya bir bütünleştirilmiş kod başvurusu gibi bir başvuru seçtiğinizde, diğer özellikleri Özellikler penceresinde dosya türüne göre görüntüleyebilir.

### <a name="culture"></a>Kültür
 Başvuru ile ilişkili dil görüntüler.

### <a name="file-type"></a>Dosya türü
 Başvurunun dosya türü görüntüler.

### <a name="file-version"></a>Dosya Sürümü
 Başvurunun dosya sürümünü görüntüler.

### <a name="identity"></a>Kimlik
 Proje dosyasında depolanan projesinde kullanılan başvurunun kimliği görüntüler.

### <a name="package"></a>Paket
 Başvuru ile ilişkili paket bildirimi adını görüntüler.

### <a name="resolved-path"></a>Çözümlenen yol
 Projede kullanılan başvuru yolunu görüntüler.

### <a name="sdk-path"></a>SDK yolu
 Başvurulan SDK dosyanın yolunu görüntüler.

### <a name="uri"></a>URI
 Dosyayı farklı bir kaynak dosyası eklemek için projenin HTML veya JavaScript dosyalarında içermesi gereken URI görüntüler.

### <a name="version"></a>Sürüm
 Başvurunun sürümü görüntüler.

## <a name="see-also"></a>Ayrıca Bkz.

- [Proje ve Çözüm Özelliklerini Yönetme](../../ide/managing-project-and-solution-properties.md)