---
title: 'Nasıl yapılır: XML Dosyalarını Düzenleme'
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: 07fa3ecf-6345-4d30-9d85-d5ef5b083319
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b25eebad9efc70e4fda45131e232983e81961625
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62840375"
---
# <a name="how-to-edit-xml-files"></a>Nasıl yapılır: XML dosyalarını düzenleme

XML Düzenleyicisi'ni XML dosyaları için yeni düzenleyicisidir. Visual Studio projesi ile ilişkili bir dosya veya tek başına bir XML dosyası üzerinde kullanılabilir. XML Düzenleyicisi'ni aşağıdaki dosya uzantıları ile ilişkilidir: *.config*, *.dtd*, *.xml*, *.xsd*, *.xdr*, *.xsl*, *.xslt*, ve *.vssettings*. XML Düzenleyicisi'ni de belirli bir düzenleyici kayıtlı olan ve XML veya DTD'nin içeriğini içeren başka bir dosya türü ile ilişkilidir.

> [!NOTE]
> XHTML belgeleri, HTML düzenleyici tarafından işlenir.

Bir XML dosyasını düzenlemek için düzenlemek istediğiniz dosyayı çift tıklatın.

## <a name="add-a-new-xml-file-to-a-project"></a>Yeni bir XML dosyası bir projeye ekleyin.

1. Gelen **proje** menüsünde **Yeni Öğe Ekle**.

2. Seçin **XML dosyası** gelen **şablonları** bölmesi.

3. Dosya adını girin **adı** alan ve ENTER tuşuna **Ekle**.

   XML dosyası projenize eklenir ve XML Düzenleyicisi'nde açılır. Varsayılan XML bildirimi dosyasını içeren `<?xml version="1.0" encoding="utf-8" ?>`.

## <a name="add-an-existing-xml-file-to-a-project"></a>Varolan bir XML dosyası bir projeye ekleyin.

1. Gelen **proje** menüsünde **varolan öğeyi Ekle**.

   **Varolan öğeyi Ekle** iletişim kutusu görüntülenir.

2. Bir XML dosyasını seçip ENTER tuşuna **Ekle**.

## <a name="create-a-new-xml-or-xslt-file"></a>Yeni bir XML veya XSLT dosyası oluşturma

1. Gelen **dosya** menüsünde **yeni**.

   **Yeni dosya** iletişim kutusu görüntülenir.

2. Seçin **XML dosyası** seçin veya yeni bir XML dosyası; oluşturmak için **XSLT dosyası** yeni bir XSLT stil sayfası oluşturmak için.

3. Tıklayın **açık**.

## <a name="create-an-empty-project-for-xml-files"></a>XML dosyaları için boş bir proje oluşturun

::: moniker range="vs-2017"

1. Gelen **dosya** menüsünde **yeni** > **proje**.

   **Yeni Proje** iletişim kutusu görünür.

2. Select dilediğiniz kod dilini seçin. **boş proje**.

3. **Tamam**'ı tıklatın.

::: moniker-end

::: moniker range=">=vs-2019"

1. Gelen **dosya** menüsünde **yeni** > **proje**.

2. Girin **boş proje** şablon arama kutusunda **boş proje (.NET Framework)** şablonu ve ardından **sonraki**.

3. **Oluştur**'u tıklatın.

::: moniker-end

4. XML dosyaları projeye ekleyin.

   XML Düzenleyicisi bu projeye eklemek şemaları bulur ve bunları doğrulama ve IntelliSense herhangi bir XML, şema veya bu proje açıkken düzenlediğiniz XSLT dosyaları için kullanır.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)
- [XML belge özellikleri, özellik penceresi](../xml-tools/xml-document-properties-properties-window.md)
- [Nasıl yapılır: Bir XML belgesinden XML şeması oluşturma](../xml-tools/how-to-create-an-xml-schema-from-an-xml-document.md)