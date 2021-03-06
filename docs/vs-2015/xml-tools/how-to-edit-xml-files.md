---
title: 'Nasıl yapılır: XML dosyalarını düzenleme | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 07fa3ecf-6345-4d30-9d85-d5ef5b083319
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 60b94274404c82695628dc72bd88bdf48145b7c2
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63443436"
---
# <a name="how-to-edit-xml-files"></a>Nasıl yapılır: XML Dosyalarını Düzenleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

XML Düzenleyicisi'ni XML dosyaları için yeni düzenleyicisidir. Visual Studio projesi ile ilişkili bir dosya veya tek başına bir XML dosyası üzerinde kullanılabilir. XML Düzenleyicisi'ni aşağıdaki dosya uzantıları ile ilişkilidir: .config, .dtd, .xml, .xsd, .xdr, .xsl, .xslt ve .vssettings. XML Düzenleyicisi'ni de belirli bir düzenleyici kayıtlı olan ve XML veya DTD'nin içeriğini içeren başka bir dosya türü ile ilişkilidir.  
  
> [!NOTE]
> XHTML belgeleri, HTML düzenleyici tarafından işlenir.  
  
### <a name="to-edit-an-xml-file"></a>Bir XML dosyasını düzenlemek için  
  
1. Düzenlemek istediğiniz dosyaya çift tıklayın.  
  
### <a name="to-add-a-new-xml-file-to-a-project"></a>Yeni bir XML dosyası bir projeye eklemek için  
  
1. Gelen **proje** menüsünde **Yeni Öğe Ekle**.  
  
2. Seçin **XML dosyası** gelen **şablonları** bölmesi.  
  
3. Dosya adını girin **adı** alan ve ENTER tuşuna **Ekle**.  
  
     XML dosyasını projeye eklenir ve XML Düzenleyicisi'nde açılır. Varsayılan XML bildirimi dosyasını içeren `<?xml version="1.0" encoding="utf-8" ?>`.  
  
### <a name="to-add-an-existing-xml-file-to-a-project"></a>Varolan bir XML dosyası bir projeye eklemek için  
  
1. Gelen **proje** menüsünde **varolan öğeyi Ekle**.  
  
     **Varolan öğeyi Ekle** iletişim kutusu görüntülenir.  
  
2. Bir XML dosyasını seçip ENTER tuşuna **Ekle**.  
  
### <a name="to-create-a-new-xml-or-xslt-file"></a>Yeni bir XML veya XSLT dosyası oluşturmak için  
  
1. Gelen **dosya** menüsünde **yeni**.  
  
     **Yeni dosya** iletişim kutusu görüntülenir.  
  
2. Seçin **XML dosyası** seçin veya yeni bir XML dosyası; oluşturmak için **XSLT dosyası** yeni bir XSLT stil sayfası oluşturmak için.  
  
3. Tıklayın **açık**.  
  
### <a name="to-create-a-project-for-xml-files"></a>XML dosyaları için bir proje oluşturmak için  
  
1. Gelen **dosya** menüsünde **yeni**ve ardından **proje**.  
  
     **Yeni Proje** iletişim kutusu görünür.  
  
2. Select dilediğiniz kod dilini seçin. **boş proje**, tıklatıp **Tamam**.  
  
3. XML dosyaları projeye ekleyin.  
  
     XML Düzenleyicisi bu projeye eklemek şemaları bulur ve bunları doğrulama ve IntelliSense herhangi bir XML, şema veya bu proje açıkken düzenlediğiniz XSLT dosyaları için kullanır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Düzenleyicisi](../xml-tools/xml-editor.md)   
 [XML belge özellikleri, özellik penceresi](../xml-tools/xml-document-properties-properties-window.md)   
 [Nasıl yapılır: XML Belgesinden XML Şeması Oluşturma](../xml-tools/how-to-create-an-xml-schema-from-an-xml-document.md)
