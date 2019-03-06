---
title: XSLT dönüştürmesi yürütme
ms.date: 03/05/2019
ms.topic: conceptual
ms.assetid: 56a0fe82-5231-487d-8b6e-a08a9b04e0fc
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e84b1c6303da4c0db39da1b3585a7d4548560feb
ms.sourcegitcommit: 3ca33862c1cfc3ccb83de3e95f1e69e860ab143a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57526379"
---
# <a name="how-to-execute-an-xslt-transformation-from-the-xml-editor"></a>Nasıl yapılır: XML düzenleyicisinden XSLT dönüştürmesi yürütme

XML Düzenleyicisi'ni bir XSLT stil sayfası bir XML belgesi ile ilişkilendirmek, dönüştürmeyi gerçekleştirmek ve çıktısını görüntülemek olanak sağlar. XSLT dönüşümü sonuç çıktısı, yeni bir belge penceresi görüntülenir.

**Çıkış** özellik çıkış dosya adını belirtir. Varsa **çıkış** özelliği boşsa, bir dosya adı, geçici dizin oluşturulur. Dosya uzantısı dayanır `xsl:output` öğesi, stil sayfası ve olabilir. *XML*,. *txt* veya. *htm*.

Varsa **çıkış** özelliği ile bir dosya adı belirtir bir. *htm* veya. *HTML* uzantısı, XSLT çıkış bir web tarayıcısı kullanarak önizlenen. Diğer tüm dosya uzantılarını kullanarak Visual Studio tarafından seçmiş varsayılan düzenleyicisi açılır. Örneğin, dosya uzantısı ise. *xml*, Visual Studio XML Düzenleyicisi'ni kullanır.

## <a name="execute-an-xslt-transformation-from-an-xml-file"></a>Bir XML dosyasından XSLT dönüştürmesi yürütme

1. Bir XML belgesi bir XML düzenleyicisinde açın.

2. Bir XSLT stil sayfası XML belge ile ilişkilendirin.

    - Ekleme bir `xml-stylesheet` işleme yönergesi için XML belgesi. Örneğin, belge giriş için şu satırı ekleyin: `<?xml-stylesheet type='text/xsl' href='filename.xsl'?>`

       -veya-

    - XSLT stil sayfası kullanılarak ekleme **özellikleri** penceresi. XML dosyası düzenleyicide açık Düzenleyicisi'nde herhangi bir yere sağ tıklayın ve seçin **özellikleri**. İçinde **özellikleri** penceresinde tıklatın **stil sayfası** alan ve Gözat düğmesini (…) seçin. XSLT stil sayfası seçin ve ardından **açık**.

3. Menü çubuğunda, **XML** > **XSLT hata ayıklama olmadan Başlat**. Veya basın **Ctrl**+**Alt**+**F5**.

   XSLT dönüşümü çıktısı, yeni bir belge penceresi görüntülenir.

   > [!NOTE]
   > XML belge ile ilişkilendirilmiş hiç stil sayfası varsa, bir iletişim kutusu kullanmak için stil sayfası girmenizi ister.

## <a name="execute-an-xslt-transformation-from-an-xslt-style-sheet"></a>Bir XSLT stil sayfasındaki XSLT dönüştürmesi yürütme

1. Bir XSLT stil sayfası XML düzenleyicisinde açın.

2. Bir XML belgesinde belirtin **giriş** belge alanını **özellikleri** penceresi.

   > [!NOTE]
   > XML belge dönüştürme için kullanılan giriş belgesidir. XSLT dönüşümü başlatıldığında, bir belge belirtilmezse **Dosya Aç** iletişim kutusu görünür ve o anda bir belge belirtebilirsiniz.

3. Menü çubuğunda, **XML** > **XSLT hata ayıklama olmadan Başlat**. Veya basın **Ctrl**+**Alt**+**F5**.

   XSLT dönüşümü çıktısı, yeni bir belge penceresi görüntülenir.

## <a name="specify-an-output-file-name"></a>Çıkış dosyası adı belirtin

Hem XML hem de XSL dosyaları için çıkış dosyası adı belirtebilirsiniz. Açık **özellikleri** penceresi ve bir dosya adı belirtin **çıkış** alan.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)