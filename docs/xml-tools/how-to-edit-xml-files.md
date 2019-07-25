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
ms.openlocfilehash: 1bcc560c1e0cabd222da68e98de18d7b8bef6ec6
ms.sourcegitcommit: 0f5f7955076238742f2071d286ad8e896f3a6cad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68483406"
---
# <a name="how-to-edit-xml-files"></a>Nasıl yapılır: XML dosyalarını düzenleme

XML Düzenleyicisi, XML dosyaları için yeni düzenleyicidir. Tek başına bir XML dosyasında veya Visual Studio projesiyle ilişkili bir dosyada kullanılabilir. XML Düzenleyicisi şu dosya uzantılarıyla ilişkili: *. config*, *. dtd*, *. xml*, *. xsd*, *. xdr*, *. xsl*, *. XSLT*ve *. vssettings*. XML Düzenleyicisi Ayrıca, kayıtlı belirli bir düzenleyici bulunmayan ve XML veya DTD içeriği içeren başka herhangi bir dosya türü ile ilişkilendirilir.

> [!NOTE]
> XHTML belgeleri HTML Düzenleyicisi tarafından işlenir.

Bir XML dosyasını düzenlemek için, düzenlemek istediğiniz dosyaya çift tıklayın.

## <a name="add-a-new-xml-file-to-a-project"></a>Projeye yeni bir XML dosyası ekleyin

1. **Proje** menüsünde **Yeni öğe Ekle**' yi seçin.

2. **Şablonlar** bölmesinden **XML dosyası** ' nı seçin.

3. **Ad** alanına dosya adını girin ve **Ekle**' ye basın.

   XML dosyası projeye eklenir ve XML düzenleyicisinde açılır. Dosya varsayılan XML bildirimini içerir, `<?xml version="1.0" encoding="utf-8" ?>`.

## <a name="add-an-existing-xml-file-to-a-project"></a>Bir projeye var olan bir XML dosyası Ekle

1. **Proje** menüsünden **Varolan öğe Ekle**' yi seçin.

   **Varolan öğe Ekle** iletişim kutusu görüntülenir.

2. Bir XML dosyası seçin ve **Ekle**'ye basın.

## <a name="create-a-new-xml-or-xslt-file"></a>Yeni bir XML veya XSLT dosyası oluşturma

1. **Dosya** menüsünde **Yeni**' yi seçin.

   **Yeni dosya** iletişim kutusu görüntülenir.

2. Yeni bir XML dosyası oluşturmak için **XML dosyasını** seçin; veya yeni bir XSLT stil sayfası oluşturmak için **XSLT dosyası** ' nı seçin.

3. Tıklayın **açık**.

## <a name="create-an-empty-project-for-xml-files"></a>XML dosyaları için boş bir proje oluştur

::: moniker range="vs-2017"

1. **Dosya** menüsünden **Yeni** > **Proje**' yi seçin.

   **Yeni Proje** iletişim kutusu görünür.

2. Seçtiğiniz kod dilini seçin ve **boş proje (.NET Framework)** şablonunu seçin.

3.           **Tamam**'ı tıklatın.

::: moniker-end

::: moniker range=">=vs-2019"

1. **Dosya** menüsünden **Yeni** > **Proje**' yi seçin.

2. Şablon arama kutusuna **boş proje** girin, **boş proje (.NET Framework)** şablonunu seçin ve ardından **İleri**' ye tıklayın.

3.           **Oluştur**'a tıklayın.

::: moniker-end

4. Projeye XML dosyaları ekleyin.

   XML Düzenleyicisi, bu projeye eklediğiniz şemaları bulur ve bu proje açıkken düzenlediğiniz XML, şema veya XSLT dosyalarında doğrulama ve IntelliSense için kullanır.

## <a name="see-also"></a>Ayrıca bkz.

- [XML Düzenleyicisi](../xml-tools/xml-editor.md)
- [XML belgesi özellikleri, Özellikler penceresi](../xml-tools/xml-document-properties-properties-window.md)
- [Nasıl yapılır: XML belgesinden XML şeması oluşturma](../xml-tools/how-to-create-an-xml-schema-from-an-xml-document.md)