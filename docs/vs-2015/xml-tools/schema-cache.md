---
title: Şema önbelleği | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-xml-tools
ms.topic: conceptual
ms.assetid: 35a7fcad-f3bf-4a96-9008-4306e7276223
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 5827debb4f79ef34bbdd059c6beb0003988a721c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54795554"
---
# <a name="schema-cache"></a>Şema Önbelleği
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]


XML Düzenleyicisi'ni %InstallRoot%\Xml\Schemas dizininde bulunan bir şema önbelleği sağlar. Şema önbelleği, bilgisayardaki tüm kullanıcılar için genel ve IntelliSense ve XML belgesi doğrulama için kullanılan standart XML şemaları içerir.  

 Belirtildiği şemaları XML Düzenleyicisi'ni de çözümde bulunan şemaları bulabilir, **şemaları** belge alanını **özellikleri** penceresi ve şemalar tarafından tanımlanan `xsi:schemaLocation` ve `xsi:noNamespaceSchemaLocation`öznitelikleri.  

 Aşağıdaki tablo, XML Düzenleyicisi ile yüklenen şemaları açıklar.  


|     Dosya adı      |                                                      Açıklama                                                      |
|-------------------|-----------------------------------------------------------------------------------------------------------------------|
|    catalog.xsd    |             XML Düzenleyicisi şema katalog dosyaları için şema. Şema kataloglarının hakkında daha fazla bilgi için aşağıya bakın.             |
| DotNetConfig.xsd  |                 Web.Config dosyaları için şema "<http://schemas.microsoft.com/.NETConfiguration/v2.0>".                 |
|    msbuild.xsd    |              MSBuild oluşturma dosyaları için şema "<http://schemas.microsoft.com/developer/msbuild/2003>".              |
|    msdata.xsd     | Tarafından eklenen XSD ek açıklamalar şeması <xref:System.Data.DataSet> sınıfı, "urn: schemas-microsoft-schemas-msdata". |
|     msxsl.xsd     |                  Şema Microsoft XSLT betik bloğu uzantıları urn: schemas-microsoft-com:xslt.                   |
| SnippetFormat.xsd |                 Kod parçacığı XML dosyaları için şema. % InstallDir%\VC#\Expansions örnekler için bkz.                 |
|    Soap1.1.xsd    |            Basit Nesne Erişim Protokolü (SOAP) 1.1 şeması http://schemas.xmlsoap.org/soap/envelope/.            |
|    Soap1.2.xsd    |                                     Basit Nesne erişim protokolü 1.2 şeması.                                     |
| SiteMapSchema.xsd |            ASP.NET site haritası XML dosyası için şema "<http://schemas.microsoft.com/AspNet/SiteMap-File-1.0>".             |
|     wsdl.xsd      |                    Web hizmeti Açıklama dili için şema http://schemas.xmlsoap.org/wsdl/.                     |
|     xenc.xsd      |                            XML şifreleme şeması http://www.w3.org/2000/09/xmldsig#.                             |
|     xhtml.xsd     |                                    XHTML için şema http://www.w3.org/1999/xhtml.                                     |
|     xlink.xsd     |                                  XLink1.0 için şema http://www.w3.org/1999/xlink.                                   |
|      xml.xsd      |              Şema XML: Space ve XML: lang özniteliklerini açıklayan http://www.w3.org/XML/1998/namespace.               |
|    xmlsig.xsd     |                        XML dijital imzalar için şema http://www.w3.org/2000/09/xmldsig#.                         |
|   xsdschema.xsd   |                            XSD kendisini tanımlayan bir şema http://www.w3.org/2001/XMLSchema.                            |
|     xslt.xsd      |                           XML Şeması dönüştürür, http://www.w3.org/1999/XSL/Transform.                            |

## <a name="updating-schemas-in-the-cache"></a>Önbellek şemalarda güncelleştiriliyor  
 XML Düzenleyicisi paket yüklenir ve çalışırken değişiklikler için izleyen Düzenleyicisi şema önbellek dizini yükler. Bir şema eklediyseniz bilinen şemalar bir bellek içi dizine otomatik olarak yüklenir. Bir şema kaldırılmışsa, bellek içi dizinden otomatik olarak kaldırılır. Bir şema güncelleştirildiyse, bu şema bellek içi önbellek otomatik olarak çıkarır.  

> [!NOTE]
>  Şema önbellek dizini bilgisayarınıza genel olduğundan, yalnızca standart ve bilgisayarınızda oluşturduğunuz tüm Visual Studio projelerine yararlı şemaları burada eklemeniz gerekir.  

 XML Düzenleyicisi şema katalog dosyaları herhangi bir sayıda şema önbellek dizini de destekler. Şema kataloglarının Düzenleyicisi hakkında bilmek istediğiniz her zaman şemaları için başka bir konuma işaret edebilir. Catalog.xsd dosya katalog dosyası biçimini tanımlar ve şema önbellek dizininde bulunur. Varsayılan katalog catalog.xml dosyasıdır ve Installdır % bulunan diğer şemaların bağlantılar içerir. Bir örnekleme catalog.xml dosyanın verilmiştir:  

```  
<SchemaCatalog xmlns="http://schemas.microsoft.com/xsd/catalog">  
  <Schema href="%InstallDir%/help/schemas/Favorites.xsd" targetNamespace="urn:Favorites-Schema"/>  
  <Schema href="%InstallDir%/help/schemas/Links.xsd" targetNamespace="urn:Links-Schema"/>  
  <Schema href="%InstallDir%/help/schemas/MyHelp.xsd" targetNamespace="urn:VSHelp-Schema"/>  
</SchemaCatalog>  
```  

 `href` Özniteliği şemaya işaret eden bir dosya yolu veya http URL'si olabilir. Katalog belge göreli dosya yolu olabilir. Aşağıdaki değişkenleri tarafından ayrılmış %%, düzenleyici tarafından tanınır ve yolunda genişletilir:  

- Installdır  

- Sistem  

- ProgramFiles  

- Programlar  

- CommonProgramFiles  

- ApplicationData  

- CommonApplicationData  

- LCID  

  Katalog belge içerebilir bir `Catalog` gösteren diğer katalog öğesi. Kullanabileceğiniz `Catalog` ekibiniz veya şirketiniz tarafından paylaşılan merkezi bir katalog veya iş ortaklarınızla paylaşılan çevrimiçi katalog işaret edecek şekilde öğesi. `href` Özniteliktir diğer katalogları dosya yolu veya http URL'si. Aşağıdaki örneğidir `Catalog` öğesi:  

```  
<Catalog href="file://c:/xcbl/xcblCatalog.xml"/>  
```  

 Kataloğu, ayrıca nasıl şemaları özel kullanarak XML belge ile ilişkilendirilen denetleyebilirsiniz `Association` öğesi. Bu öğe hiçbir hedef ad alanı olduğu için XML Düzenleyicisi'ni sahip olmayan bir şema tüm otomatik ilişkilendirme yapmak yararlı olabilir belirli dosya uzantısına sahip olan şemalar ilişkilendirir bir `targetNamespace` özniteliği. Aşağıdaki örnekte `Association` öğesi ilişkilendirir dotNetConfig şema "yapılandırma" dosya uzantısına sahip tüm dosyaları:  

```  
<Association extension="config" schema="%InstallDir%/xml/schemas/dotNetConfig.xsd"/>  
```  

## <a name="localized-schemas"></a>Yerelleştirilmiş şemaları  
 Çoğu durumda, yerelleştirilmiş şemaları için girişler catalog.xml dosya içermiyor. Yerelleştirilmiş şema dizini gösterecek catalog.xml dosyasına ek girişler ekleyebilirsiniz.  

 Aşağıdaki örnekte yeni bir `Schema` yerelleştirilmiş şemaya işaret edecek şekilde LCID % değişken % kullanan öğe oluşturuldu.  

```  
<Schema href="%InstallRoot%/Common7/IDE/Policy/Schemas/%LCID%/TDLSchema.xsd"  
  targetNamespace="http://www.microsoft.com/schema/EnterpriseTemplates/TDLSchema"/>  
```  

## <a name="changing-the-location-of-the-schema-cache"></a>Şema önbellek konumunu değiştirme  
 Şema önbelleği kullanmaya konumu özelleştirebilirsiniz **çeşitli** seçenekler sayfası. Sık kullanılan şema bir dizininiz varsa, düzenleyici bu şemaları kullanacak şekilde yapılandırılabilir.  

> [!NOTE]
>  Bu değişiklik, yalnızca geçerli Visual Studio kullanıcı etkiler.  

#### <a name="to-change-the-schema-cache-location"></a>Şema önbellek konumunu değiştirmek için  

1.  Gelen **Araçları** menüsünde **seçenekleri**.  

2.  Genişletin **metin düzenleyici**, genişletme **XML**ve ardından **çeşitli**.  

3.  Tıklayın **Gözat** düğmesini **şemaları** alan.  

4.  Şema önbelleği klasörü seçin ve tıklayın **Tamam**.  

#### <a name="to-add-another-directory-of-common-schemas"></a>Ortak şema başka bir dizin eklemek için  

1.  XML Düzenleyicisi şema önbellek dizini catalog.xml dosyayı düzenleyin.  

2.  Yeni bir `<Catalog href="…"/>` ek şemaları dizinine işaret eden bir öğe.  

3.  Değişikliklerinizi kaydedin.  

     Katalog otomatik olarak yüklenir.  

## <a name="see-also"></a>Ayrıca Bkz.  
 [XML Düzenleyicisi](../xml-tools/xml-editor.md)
