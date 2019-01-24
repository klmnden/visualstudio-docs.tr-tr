---
title: 'Nasıl yapılır: XML kod parçacıklarını oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: d8556dd7-1382-4af7-ba80-3e873c9416be
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4c676032c2d0bc6c47023c5fd43bc759cccff8de
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54773228"
---
# <a name="how-to-create-xml-snippets"></a>Nasıl yapılır: XML Kod Parçacıklarını Oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
XML Düzenleyicisi'ni yeni kod parçacıkları oluşturmak için kullanılabilir. "Kod parçacığı" adlı bir XML kod parçacığı Düzenleyici içeren yeni kod parçacıkları oluşturmak için diğer bir deyişle bir ortak kod parçacığı.  
  
## <a name="to-create-a-new-xml-snippet"></a>Yeni bir XML kod parçacığı oluşturmak için  
 Yeni bir XML kodu oluşturmak için kod parçacığı yeni bir XML dosyası oluşturun ve kullanın **parçacık Ekle** özelliği.  
  
1.  Üzerinde **dosya** menüsünde tıklatın **yeni** ve ardından **dosya**.  
  
2.  Tıklayın **XML dosyası** ve ardından **açık**.  
  
3.  Düzenleyici bölmesine sağ tıklayıp **parçacık Ekle**.  
  
4.  Seçin **kod parçacığı** listesi ve ENTER tuşuna basın.  
  
5.  Yeni kod parçacığını değişiklikleri yapın.  
  
6.  Gelen **dosya** menüsünü seçin **Kaydet XMLFile.xml**.  
  
     **Dosyayı farklı Kaydet** iletişim kutusu görüntülenir.  
  
7.  Yeni kod parçacığı için bir ad girin ve seçin **kod parçacığı dosyaları** gelen **farklı kaydetme türü** açılır pencere.  
  
8.  Kullanım **kaydetmek** My Documents\Visual Studio 2005\Code Snippets\XML\My XML kod parçacıklarını klasöre dosya konumunu değiştirin ve ENTER tuşuna basın, aşağı açılan liste **Kaydet**.  
  
## <a name="snippet-description"></a>Kod parçacığı açıklaması  
 Bu bölümde Demirbaş kod parçacığında temel öğelerinden bazıları açıklanmaktadır. XML kod parçacıkları tarafından kullanılan şema öğeleri hakkında daha fazla bilgi için bkz: [kod parçacıkları şema başvurusu](../ide/code-snippets-schema-reference.md).  
  
### <a name="snippettype-element"></a>SnippetType Öğesi  
 Düzenleyici iki kod parçacığı türlerini destekler:  
  
```  
<SnippetTypes>  
  <SnippetType>SurroundsWith</SnippetType>  
  <SnippetType>Expansion</SnippetType>  
</SnippetTypes>  
```  
  
 `Expansion` Türü çağırdığınızda, kod parçacığı görünüp görünmeyeceğini belirler **parçacık Ekle** komutu. `SurroundsWith` Türü çağırdığınızda, kod parçacığı görünüp görünmeyeceğini belirler **Surrounds ile** komutu.  
  
### <a name="code-element"></a>Code Öğesi  
 `Code` Öğesi, kod parçacığında çağrıldığında eklenecek XML metni tanımlar.  
  
> [!NOTE]
>  XML kod parçacığı metin içinde alınmalıdır bir `<![CDATA[...]]>` bölümü.  
  
 Aşağıdaki `Code` Demirbaş kod parçacığı tarafından oluşturulan öğesi.  
  
```  
<Code Language="XML">  
  <![CDATA[<test>  
  <name>$name$</name>  
  $selected$ $end$</test>]]>  
</Code>  
```  
  
 `Code` Öğesi üç değişkenler içerir.  
  
- $name$ kullanıcı tanımlı değişkendir. Oluşturur bir `name` "adı" için varsayılan olarak düzenlenebilir bir değere sahip öğe. Kullanıcı tanımlı değişkenler, kullanılarak tanımlanır `Literal` öğesi.  
  
- Seçili $$ önceden tanımlanmış bir değişkendir. Bu kod parçacığı çağırmadan önce XML Düzenleyicisi'nde seçili metni temsil eder. Bu değişken yerleşimini seçili metin, seçimi çevreleyen kod parçacığında nerede görüneceğini belirler.  
  
- $end$ önceden tanımlanmış bir değişkendir. Bu değişken, kullanıcı kod parçacığı alanları düzenleme bitirmek için ENTER tuşuna bastığında şapka (^) burada taşınır belirler.  
  
  Yukarıdaki `Code` öğe aşağıdaki XML metni ekler:  
  
```  
<test>  
  <name>name</name>  
</test>  
```  
  
 Name öğesi değeri, düzenlenebilir bir bölge işaretlenir.  
  
### <a name="literal-element"></a>Literal Öğesi  
 `Literal` Öğesi dosyasına eklendikten sonra özelleştirilebilir yerine konacak metin tanımlamak için kullanılır. Örneğin, değişmez değer dizeleri, sayısal değerler ve bazı değişken adları değişmez değer olarak bildirilebilir. Herhangi bir sayıda değişmez değerleri, XML kod parçacığı içinde tanımlayabilirsiniz ve kod parçacığı içinde birden çok kez den başvurabilir. Aşağıdaki örneğidir bir `Literal` varsayılan değeri olan "name" $name$ değişken tanımlayan öğe  
  
```  
<Literal>  
  <ID>name</ID>  
  <Default>name</Default>  
</Literal  
```  
  
 Değişmez değerleri, işleve de başvurabilir. XML Düzenleyicisi adlı işlevi içerir **LookupPrefix**. **LookupPrefix** işlevi bu kod parçacığı çağrılır ve varsa, ad alanı için tanımlanan ad alanı öneki döndürür ve iki nokta üst üste (:) içeren XML belgesindeki konumdan belirtilen ad alanı URI arar ad. Aşağıdaki örneğidir bir `Literal` kullanan öğesi **LookupPrefix** işlevi.  
  
```  
<Literal Editable="false">  
   <ID>prefix</ID>  
   <Function>LookupPrefix("namespaceURI")</Function>  
</Literal>  
```  
  
 $Prefix$ değişken sonra XML kod parçacığı başka bir yerde kullanılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [XML kod parçacıkları](../xml-tools/xml-snippets.md)   
 [Nasıl yapılır: XML kod parçacıklarını kullanma](../xml-tools/how-to-use-xml-snippets.md)   
 [Nasıl yapılır: XML şemasından XML kod parçacığı oluşturma](../xml-tools/how-to-generate-an-xml-snippet-from-an-xml-schema.md)
