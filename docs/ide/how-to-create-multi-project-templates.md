---
title: Birden çok proje şablonu oluşturma
ms.date: 04/17/2019
ms.topic: conceptual
helpviewer_keywords:
- Visual Studio templates, creating multi-project
- project templates, multi-project
- multi-project templates
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f24a7c0d07c804ca45bb31058061cda714ef6a51
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62430503"
---
# <a name="how-to-create-multi-project-templates"></a>Nasıl yapılır: Birden çok proje şablonu oluşturma

Birden fazla projeli şablonlar, iki veya daha fazla proje için kapsayıcı olarak davranır. Birden çok proje şablonu temel alan bir proje oluşturduğunuzda, şablondaki her projesi çözüme eklenir.

İki veya daha fazla proje şablonları ve bir kök şablonu türü birden çok proje şablonu olan **da ProjectGroup**.

Birden çok proje şablonu tek proje şablonlarından farklı davranır. Bunlar aşağıdaki benzersiz özelliklere sahiptir:

- Yeni bir proje oluşturmak için şablon kullanıldığında tek tek projelerde birden fazla projeli bir şablon adları atanamaz. Bunun yerine, **ProjectName** özniteliği **ProjectTemplateLink** öğesinde *vstemplate* dosyaya her proje için bir ad belirtin.

- Birden çok proje şablonu, farklı diller için proje içerebilir, ancak bir kategorideki tüm şablon yalnızca içine yerleştirilebilir. Şablon kategorisinde belirtin **ProjectType** öğesinin *vstemplate* dosya.

Birden çok proje şablonu sıkıştırılmadan aşağıdakileri içermesi gereken bir *.zip* dosyası:

- Bir kök *vstemplate* dosya tüm birden çok proje şablonu. Bu kök *vstemplate* oluşturduğunuz yeni proje iletişim kutusunda görüntülenen meta veri dosyası içerir. Ayrıca nerede bulunacağını belirtmektedir *vstemplate* dosyaları şablonda projeler için. Bu dosya kök dizininde *.zip* dosya.

- Tam proje şablonu için gerekli dosyaları içeren iki veya daha fazla klasör. Tüm kod dosyaları proje klasörleri içerir ve ayrıca bir *vstemplate* proje dosyası.

Örneğin, birden çok proje şablonu *.zip* sahip iki proje dosyası aşağıdaki dosyalar ve dizinler sahip olabilir:

- *MultiProjectTemplate.vstemplate*
- *\Project1\MyTemplate.vstemplate*
- *\Project1\Project1.vbproj*
- *\Project1\Class.vb*
- *\Project2\MyTemplate.vstemplate*
- *\Project2\Project2.vbproj*
- *\Project2\Class.vb*

Kök *vstemplate* birden çok proje şablonu, aşağıdaki yollarla bir tek proje şablonundan farklı dosya:

- **Türü** özniteliği **VSTemplate** öğeye sahip değeri **da ProjectGroup** yerine **proje**. Örneğin:

    ```xml
    <VSTemplate Version="2.0.0" Type="ProjectGroup"
        xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    ```

- **TemplateContent** öğesi içeren bir **ProjectCollection** bir veya daha fazla olan öğeyi **ProjectTemplateLink** yolları için tanımlayanöğeler*vstemplate* bulunan proje dosyaları. Örneğin:

    ```xml
    <TemplateContent>
        <ProjectCollection>
            <ProjectTemplateLink>
                Project1\MyTemplate.vstemplate
            </ProjectTemplateLink>
            <ProjectTemplateLink>
                Project2\MyTemplate.vstemplate
            </ProjectTemplateLink>
        </ProjectCollection>
    </TemplateContent>
    ```

> [!TIP]
> Yeni Proje iletişim kutusu ve içerdiği tek tek projeler için birden çok proje şablonu yalnızca istiyorsanız, iç şablon olarak işaretlemek [gizli](../extensibility/hidden-element-visual-studio-templates.md). Örneğin:
>
> ```xml
> <VSTemplate Type="Project" ... >
>     <TemplateData>
>         ...
>         <Hidden>true</Hidden>
>     </TemplateData>
>     ...
> </VSTemplate>
> ```

## <a name="create-a-multi-project-template-from-an-existing-solution"></a>Varolan bir çözümden birden çok proje şablonu oluşturma

1. Bir çözüm oluşturun ve iki veya daha fazla proje ekleyin.

2. Bunlar için bir şablonu dışarı aktarılmasına izin hazır olana kadar projeleri özelleştirin.

   > [!TIP]
   > Kullanıyorsanız [şablon parametreleri](template-parameters.md) ve istediğiniz üst şablonundan değişkenlerine başvurmak parametrenin adı ön eki `ext_`. Örneğin: `$ext_safeprojectname$` Ayrıca, **CopyParameters** özniteliği **ProjectTemplateLink** öğesine **true**.
   >
   > ```xml
   > <ProjectTemplateLink ProjectName="MyProject" CopyParameters="true">...</ProjectTemplateLink>
   > ```

3. Üzerinde **proje** menüsünde seçin **şablonu dışarı aktar**.

   **Şablonu Dışarı Aktarma Sihirbazı** açılır.

4. Üzerinde **seçtiğiniz şablon türüne** sayfasında **proje şablonu**. İçin bir şablonu dışarı aktarma ve ardından istediğiniz projeleri seçin **sonraki**. (Bu adımları çözümde her proje için yinelemeniz.)

5. Üzerinde **şablon seçenekleri** şablonunuz için bir ad ve isteğe bağlı bir açıklama, simge ve önizleme görüntüsü girin. Seçin **son**.

   Proje içine aktarılır bir *.zip* dosya ve belirtilen çıkış konuma yerleştirdi.

   > [!NOTE]
   > Her proje olmalıdır ayrı ayrı bir şablona dışarı, bu nedenle önceki adımları çözümde her proje için yineleyin.

6. Her proje için bir alt ile şablon için bir dizin oluşturun.

7. Her projenin içeriğini ayıklayın *.zip* dosyasına, oluşturduğunuz karşılık gelen alt dizini.

8. Temel dizinde olan bir XML dosyası oluşturmak bir *.vstemplate* dosya uzantısı. Bu dosya için birden çok proje şablonu meta verileri içerir. Dosya yapısı için aşağıdaki örneğe bakın. Her proje için göreli bir yol belirttiğinizden emin olun *vstemplate* dosya.

9. Temel dizin ve sağ tıklayın veya bağlam menüsünden tüm dosyaları seçin, **göndermek** > **sıkıştırılmış (daraltılmış) klasör**.

   Dosya ve klasörler halinde sıkıştırılmış bir *.zip* dosya.

10. Kopyalama *.zip* kullanıcı proje şablonu dizine dosya. Varsayılan olarak, bu dizindir *%USERPROFILE%\Documents\Visual Studio \<sürüm\>\Templates\ProjectTemplates*.

11. Visual Studio'da **dosya** > **yeni** > **proje** ve, şablonun göründüğünden emin olun.

## <a name="two-project-example"></a>İki proje örneği

Bu örnek, basit bir çoklu proje kök gösterir *vstemplate* dosya. Bu örnekte, şablon iki proje vardır **My Windows Application** ve **My Class Library**. **ProjectName** özniteliği **ProjectTemplateLink** öğesi projeye verilen adını belirtir.

> [!TIP]
> Varsa **ProjectName** özniteliği belirtilmezse, adı *vstemplate* dosyası, proje adı olarak kullanılır.

```xml
<VSTemplate Version="2.0.0" Type="ProjectGroup"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>Multi-Project Template Sample</Name>
        <Description>An example of a multi-project template</Description>
        <Icon>Icon.ico</Icon>
        <ProjectType>VisualBasic</ProjectType>
    </TemplateData>
    <TemplateContent>
        <ProjectCollection>
            <ProjectTemplateLink ProjectName="My Windows Application">
                WindowsApp\MyTemplate.vstemplate
            </ProjectTemplateLink>
            <ProjectTemplateLink ProjectName="My Class Library">
                ClassLib\MyTemplate.vstemplate
            </ProjectTemplateLink>
        </ProjectCollection>
    </TemplateContent>
</VSTemplate>
```

## <a name="example-with-solution-folders"></a>Örnek çözüm klasörleri

Bu örnekte **SolutionFolder** projeleri iki gruplara bölmek için öğe **matematik sınıfları** ve **grafik sınıflarını**. Şablonda dört projeleri, ikisi her çözüm klasöründe yer alır.

```xml
<VSTemplate Version="2.0.0" Type="ProjectGroup"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">
    <TemplateData>
        <Name>Multi-Project Template Sample</Name>
        <Description>An example of a multi-project template</Description>
        <Icon>Icon.ico</Icon>
        <ProjectType>VisualBasic</ProjectType>
    </TemplateData>
    <TemplateContent>
        <ProjectCollection>
            <SolutionFolder Name="Math Classes">
                <ProjectTemplateLink ProjectName="MathClassLib1">
                    MathClassLib1\MyTemplate.vstemplate
                </ProjectTemplateLink>
                <ProjectTemplateLink ProjectName="MathClassLib2">
                    MathClassLib2\MyTemplate.vstemplate
                </ProjectTemplateLink>
            </SolutionFolder>
            <SolutionFolder Name="Graphics Classes">
                <ProjectTemplateLink ProjectName="GraphicsClassLib1">
                    GraphicsClassLib1\MyTemplate.vstemplate
                </ProjectTemplateLink>
                <ProjectTemplateLink ProjectName="GraphicsClassLib2">
                    GraphicsClassLib2\MyTemplate.vstemplate
                </ProjectTemplateLink>
            </SolutionFolder>
        </ProjectCollection>
    </TemplateContent>
</VSTemplate>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Proje ve öğe şablonları oluşturma](../ide/creating-project-and-item-templates.md)
- [Nasıl yapılır: Proje şablonları oluşturma](../ide/how-to-create-project-templates.md)
- [Visual Studio Şablon Şeması Başvurusu (genişletilebilirlik)](../extensibility/visual-studio-template-schema-reference.md)
- [SolutionFolder öğesi (Visual Studio şablonları)](../extensibility/solutionfolder-element-visual-studio-templates.md)
- [ProjectTemplateLink öğesi (Visual Studio şablonları)](../extensibility/projecttemplatelink-element-visual-studio-templates.md)