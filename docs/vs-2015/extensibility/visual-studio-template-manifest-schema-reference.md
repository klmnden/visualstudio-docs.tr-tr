---
title: Visual Studio şablon bildirim Şeması Başvurusu | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: bc7d0a81-0df5-41a9-a912-1b30e5da1d13
caps.latest.revision: 4
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: cef2b1936ce3e7c5e9495aa65e9724c53317d17f
ms.sourcegitcommit: af428c7ccd007e668ec0dd8697c88fc5d8bca1e2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/16/2018
ms.locfileid: "51723422"
---
# <a name="visual-studio-template-manifest-schema-reference"></a>Visual Studio Şablon Bildirim Şeması Başvurusu
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bu şema için Visual Studio Proje veya öğe şablonları oluşturulan Visual Studio şablon bildirimi (.vstman) dosyalarının biçimi ve konumu ve şablon ilgili diğer bilgileri açıklar.  
  
 : Olduğundan ayrı bir öğe ve proje şablonu dizinleri, bildirim hiçbir öğe ve proje şablonlarının bir karışımını olmalıdır.  
  
> [!IMPORTANT]
>  Bu bildirimi, Visual Studio "15" Preview 2'den itibaren kullanılabilmektedir.  
  
## <a name="vstemplatemanifest-element"></a>VSTemplateManifest öğesi  
 Bildirimin kök öğesi.  
  
### <a name="attributes"></a>Öznitelikler  
  
-   **Sürüm**: şablon bildirimi sürümünü temsil eden bir dize. Gerekli.  
  
-   **Yerel ayar**: yerel ya da yerel ayarlara şablon bildirim temsil eden bir dize. Her yerel ayar için ayrı bir bildirim kullanmak için yerel ayar değeri tüm şablonları için geçerlidir. İsteğe bağlı.  
  
### <a name="child-elements"></a>Alt Öğeler  
  
-   **VSTemplateContainer** isteğe bağlı.  
  
-   **VSTemplateDir** isteğe bağlı.  
  
### <a name="parent-element"></a>Üst Öğe  
 Yok.  
  
## <a name="vstemplatecontainer"></a>VSTemplateContainer  
 Kapsayıcı şablon bildirimi öğeleri. Bir bildirim tanımladığı her şablon için bir şablon kapsayıcısı var.  
  
### <a name="attributes"></a>Öznitelikler  
 **VSTemplateType** : şablon türünü belirten bir dize değeri (`"Project"`, `"Item"`, veya `"ProjectGroup"`). Gerekli  
  
### <a name="child-elements"></a>Alt Öğeler  
  
-   **RelativePathOnDisk**: disk üzerinde şablon dosyasının göreli yol. Bu konumu gösterilen şablonu ağacında şablonu yerleşimini de tanımlar. **yeni proje** veya **yeni öğe** iletişim. Bir dizin ve tek tek dosyaları dağıtılan şablonlar için şablon dosyaları içeren dizine bu yolu gösterir. Bir .zip dosyası olarak dağıtılan şablonları için bu yolu, .zip dosyasının yolu olmalıdır.  
  
-   **VSTemplateHeader** : A [TemplateData](../extensibility/templatedata-element-visual-studio-templates.md) açıklayan üstbilgi öğesi.  
  
### <a name="parent-element"></a>Üst Öğe  
 **VSTemplateManifest**  
  
## <a name="vstemplatedir"></a>VSTemplateDir  
 Şablon bulunduğu dizin açıklar. Birden çok bildirim içerebilir **VSTemplateDir** girişlerinin yerelleştirilmiş adını ve şablon kategorisi ağacında görünümlerini denetlemek için sıralama dizinler için sıralama belirtin.  
  
 Kendi tasarımı nedeniyle **VSTemplateDir** girişleri, yalnızca yerel olmayan belirtilen bildirimleri içinde görünmelidir.  
  
### <a name="attributes"></a>Öznitelikler  
 Yok.  
  
### <a name="child-elements"></a>Alt Öğeler  
  
-   **RelativePath**: şablon yolu. Yüzden ilk tüm bildirimler için yol başına yalnızca bir giriş olabilir.  
  
-   **LocalizedName**: A **NameDescriptionIcon** yerelleştirilmiş adı belirten öğe. İsteğe bağlı.  
  
-   **SortOrder** : sıralama düzenini belirten bir dize. İsteğe bağlı.  
  
-   **ParentFolderOverrideName**: geçersiz kılınan üst klasörün adı. İsteğe bağlı. Bu öğeyi bir **adı** özniteliği, adını belirten bir dize değeridir.  
  
### <a name="parent-element"></a>Üst Öğe  
 **VSTemplateManifest**  
  
## <a name="namedescriptionicon"></a>NameDescriptionIcon  
 Yerelleştirilmiş şablonları için büyük olasılıkla bir açıklama ve adını belirtir. Bkz: **LocalizedName** yukarıda.  
  
### <a name="attributes"></a>Öznitelikler  
  
-   **Paket**: Paket belirten bir dize değeri. İsteğe bağlı.  
  
-   **Kimliği**: kimliğini belirten bir dize değeri İsteğe bağlı.  
  
### <a name="child-elements"></a>Alt Öğeler  
 Yok.  
  
### <a name="parent-element"></a>Üst Öğe  
 **LocalizedName**  
  
## <a name="examples"></a>Örnekler  
 Bir proje şablonu .vstman dosyası örneği verilmiştir.  
  
```xml  
<VSTemplateManifest Version="1.0" Locale="1033" xmlns="http://schemas.microsoft.com/developer/vstemplatemanifest/2015">  
  <VSTemplateContainer TemplateType="Project">  
    <RelativePathOnDisk>CSharp\1033\TestProjectTemplate</RelativePathOnDisk>  
    <TemplateFileName>TestProjectTemplate.vstemplate</TemplateFileName>  
    <VSTemplateHeader>  
      <TemplateData xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
        <Name>TestProjectTemplate</Name>  
        <Description>TestProjectTemplate</Description>  
        <Icon>TestProjectTemplate.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <RequiredFrameworkVersion>2.0</RequiredFrameworkVersion>  
        <SortOrder>1000</SortOrder>  
        <TemplateID>aac0aeea-7883-4003-992f-937d53d70ab1</TemplateID>  
        <CreateNewFolder>true</CreateNewFolder>  
        <DefaultName>TestProjectTemplate</DefaultName>  
        <ProvideDefaultName>true</ProvideDefaultName>  
      </TemplateData>  
    </VSTemplateHeader>  
  </VSTemplateContainer>  
</VSTemplateManifest>  
  
```  
  
 Bir öğe şablonu .vstman dosyası örneği verilmiştir.  
  
```  
VSTemplateManifest Version="1.0" Locale="1033" xmlns="http://schemas.microsoft.com/developer/vstemplatemanifest/2015">  
  <VSTemplateContainer TemplateType="Item">  
    <RelativePathOnDisk>CSharp\1033\ItemTemplate1</RelativePathOnDisk>  
    <TemplateFileName>ItemTemplate1.vstemplate</TemplateFileName>  
    <VSTemplateHeader>  
      <TemplateData xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
        <Name>ItemTemplate1</Name>  
        <Description>ItemTemplate1</Description>  
        <Icon>ItemTemplate1.ico</Icon>  
        <TemplateID>bfeadf8e-a251-4109-b605-516b88e38c8d</TemplateID>  
        <ProjectType>CSharp</ProjectType>  
        <RequiredFrameworkVersion>2.0</RequiredFrameworkVersion>  
        <NumberOfParentCategoriesToRollUp>1</NumberOfParentCategoriesToRollUp>  
        <DefaultName>Class.cs</DefaultName>  
      </TemplateData>  
    </VSTemplateHeader>  
  </VSTemplateContainer>  
</VSTemplateManifest>  
  
```

