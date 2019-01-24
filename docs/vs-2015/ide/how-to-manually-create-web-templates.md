---
title: 'Nasıl yapılır: Web şablonlarını elle oluşturma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio templates, Web
- templates [Visual Studio], Web
- Web templates [Visual Studio]
- project templates [Visual Studio], Web
ms.assetid: 731c4027-a152-48c5-bfc4-93490bf1949f
caps.latest.revision: 20
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 4884ef313d969ae59b8aea704490eeb2e4e5a91c
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54782216"
---
# <a name="how-to-manually-create-web-templates"></a>Nasıl yapılır: Web şablonlarını elle oluşturma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir Web şablonu oluşturma, diğer türlerdeki şablonları oluşturmaktan daha farklıdır. Web projesi şablonları görünür çünkü **yeni Web sitesi Ekle** iletişim kutusu ve Web proje öğesi kategorilere ayrılabilir programlama dili, .vstemplate dosyası şablonu bir Web şablonu belirtin ve programlama tanımlayın dili.  
  
> [!NOTE]
>  Web şablonları kullanılarak belirtilen bir boş .webproj dosyası içermelidir `File` özniteliği `Project` öğesi. Web projeleri, proje dosyalarını gerektirmeyen rağmen bir Web şablonu düzgün çalışır, böylece bu dosya gereklidir.  
  
### <a name="to-manually-create-a-web-template"></a>El ile bir Web şablonu oluşturmak için  
  
1. Web projesi oluşturun.  
  
2. Değiştirme veya proje dosyaları silin veya yeni dosyalar projeye ekleyin.  
  
3. Bir XML dosyası oluşturun ve projeniz gibi aynı dizinde bir .vstemplate dosya adı uzantısı kullanarak kaydedin. Projede eklemeyin [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].  
  
4. Proje şablonu meta verilerini sağlamak için .vstemplate XML dosyasına yazar. Daha fazla bilgi için aşağıdaki bölümdeki örnekte bakın.  
  
5. Bulun `ProjectType` .vstemplate dosyasını ve metin değerini kümesi öğesinde `Web`.  
  
6. Aşağıdaki `ProjectType` öğe, Ekle bir `ProjectSubType` öğesi ve metin şablonunun programlama dili değeri ayarlayın. Programlama dili, aşağıdaki değerlerden biri olabilir:  
  
   - CSharp  
  
   - VisualBasic  
  
     Örneğin:  
  
   ```  
   <TemplateData>  
       ...  
       <ProjectType>Web</ProjectType>  
       <ProjectSubType>CSharp</ProjectSubType>  
       ...  
   </TemplateData>  
   ```  
  
7. (Bu içerir .vstemplate dosyası), şablonunuzda dosyaları seçin, seçime sağ tıklayın, **göndermek için**ve ardından **sıkıştırılmış (daraltılmış) klasör**. Dosyaları bir .zip dosyasına sıkıştırılır.  
  
8. .Zip şablon dosyası koymak [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] proje şablonu dizini. Varsayılan olarak, bu \My Documents\Visual Studio dizindir *sürüm*\My dışarı aktarılan şablonları\\.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnek, bir Web projesi şablonu için bir temel .vstemplate dosyası gösterilmektedir.  
  
```  
<VSTemplate Version="2.0.0" Type="Project"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">>  
    <TemplateData>  
        <Name>MyWebProjecStarterKit</Name>  
        <Description>A simple Web template</Description>  
        <Icon>icon.ico</Icon>  
        <ProjectType>Web</ProjectType>  
        <ProjectSubType>CSharp</ProjectSubType>  
        <DefaultName>WebSite</DefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <Project File="WebApplication.webproj">  
            <ProjectItem>icon.ico</ProjectItem>  
            <ProjectItem OpenInEditor="true">Default.aspx</ProjectItem>  
            <ProjectItem>Default.aspx.cs</ProjectItem>  
        </Project>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)   
 [Visual Studio Şablon Şeması Başvurusu](../extensibility/visual-studio-template-schema-reference.md)
