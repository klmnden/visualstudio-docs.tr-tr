---
title: Visual Studio "15" için özel Proje ve öğe şablonlarını yükseltme | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: ad02477b-e101-4f32-aeb7-292bf95d5c2f
caps.latest.revision: 4
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 9137510f8d6949271a255b14b293f59366048f77
ms.sourcegitcommit: 240c8b34e80952d00e90c52dcb1a077b9aff47f6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2018
ms.locfileid: "49923452"
---
# <a name="upgrading-custom-project-and-item-templates-for-visual-studio-15"></a>Visual Studio "15" için özel Proje ve öğe şablonlarını yükseltme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Başlangıç Visual Studio "15" Preview 4, Visual Studio bir .vsix veya bir. msi'nin yüklenmiş proje ve öğe şablonlarını bulduğu şeklimiz değişiyor. Özel proje veya öğe şablonları kullanan uzantıları sahipseniz, uzantılarınız güncelleştirmeniz gerekiyor. Ne yapmanız gerekir, bu konuda açıklanmaktadır.  
  
 Bu değişiklik, yalnızca Visual Studio "15" etkiler. Visual Studio'nun önceki sürümlerini etkilemez.  
  
 Bir VSIX uzantısının bir parçası olarak bir proje veya öğe şablonu oluşturmak istiyorsanız, bkz. [oluşturma özel Proje ve öğe şablonlarını](../extensibility/creating-custom-project-and-item-templates.md).  
  
## <a name="template-scanning"></a>Tarama şablonu  
 Daha önce **devenv/Setup** veya **devenv /installvstemplates** proje ve öğe şablonlarını bulmak için yerel disk taranır. Preview 4'te başlayarak, tarama için kullanıcı düzeyi konum gerçekleştirilir (**%USERPROFILE%\Documents\\< Visual Studio sürümü\>\My dışarı aktarılan şablonları\\**) için kullanılır tarafından oluşturulan şablonlarını **dosya / dışarı aktarma şablonları** komutu.  
  
 Diğer (kullanıcı olmayan) konumları için konumu ve diğer özellikleri de şablon belirten bir manifest(.vstman) dosyası eklemeniz gerekir. .Vstman dosya şablonları için kullanılan .vstemplate dosyasıyla birlikte oluşturulur. Uzantınızı bir .vsix kullanarak yüklerseniz, bu uzantı Visual Studio "15" Preview 2 derleyerek gerçekleştirebilirsiniz. Ancak bir. msi'nin kullanırsanız, değişiklikler el ile yapmanız gerekir. Bu değişiklikleri yapmak için yapmanız gerekenler bir listesi için bkz **yükseltme ile yüklenen uzantıları için bir. MSI** bu konuda.  
  
## <a name="how-to-update-a-vsix-extension-with-project-or-item-templates"></a>Bir VSIX uzantısı, proje veya öğe şablonları ile güncelleştirme  
 Bu yordam, varolan bir VSIX uzantısı Visual Studio "15" Preview 2 güncelleştirmesi yüklü olunacağı açıklanmaktadır.  
  
1.  Visual Studio "15" Preview 2 sürümünde çözümü açın. Yükseltme kodu istenir. **Tamam**'ı tıklatın.  
  
2.  Yükseltme tamamlandıktan sonra yükleme hedef sürümünü değiştirmeniz gerekebilir. VSIX projesinde source.extension.vsixmanifest dosyasını açın ve seçin **hedefleri Yükle** sekmesi. Varsa **sürüm aralığı** alandır **[14.0]**, tıklayın **Düzenle** ve Visual Studio "15" içerecek şekilde değiştirin. Örneğin, ayarlayabilirsiniz **[14.0,15.0]** Visual Studio 2015 veya Visual Studio "15", veya için uzantıyı yüklemek için **[15.0]** yalnızca Visual Studio "15" yüklemek için.  
  
3.  Kodu yeniden derleyin.  
  
4.  Visual Studio’yu kapatın.  
  
5.  VSIX yükleyin.  
  
6.  Güncelleştirme, aşağıdakileri yaparak test edebilirsiniz:  
  
    1.  Dosya değişikliği tarama, aşağıdaki kayıt defteri anahtarı tarafından etkinleştirilir:  
  
         **reg hklm\software\microsoft\visualstudio\15.0\VSTemplate /v DisableTemplateScanning /t REG_DWORD /d 1 /reg:32 Ekle**  
  
    2.  Anahtarı ekledikten sonra Çalıştır **devenv /installvstemplates**.  
  
    3.  Visual Studio'yu yeniden açın. Beklenen konumda şablonunuzu bulmanız gerekir.  
  
    > [!NOTE]
    >  Visual Studio genişletilebilirlik proje şablonları kayıt defteri anahtarı mevcut olduğunda kullanılabilir değil. Kayıt defteri anahtarı silmelisiniz (ve yeniden **devenv /installvstemplates**) bunları kullanmak için.  
  
## <a name="other-recommendations-for-deploying-project-and-item-templates"></a>Proje ve öğe şablonlarını dağıtmak için diğer öneriler  
  
-   Sıkıştırılmış şablon dosyaları kullanmaktan kaçının. Şablon kaynakları ve içerik almak için açılması gereken dosya daraltılmış, bu nedenle bunlar kullanılacak costlier olur. Bunun yerine, şablon başlatma ' hızlandırmak için kendi dizin altında tek tek dosya olarak proje ve öğe şablonlarını dağıtmanız gerekir. VSIX uzantıları için SDK derleme görevleri otomatik olarak herhangi bir daraltılmış şablon VSIX dosyasını oluştururken sıkıştırmasını.  
  
-   Şablon bulma sırasında gereksiz kaynak derleme yüklerini önlemek için bir şablon adı, açıklama, simge veya Önizleme için paket/kaynak kimliği girdileri kullanmaktan kaçının. Bunun yerine, yerelleştirilmiş bildirimler yerelleştirilmiş adlar veya özellikleri kullanan her yerel ayar için bir şablon girişi oluşturmak için kullanabilirsiniz.  
  
-   Şablon olarak dosya öğeleri dahil olmak üzere, bildirim oluşturma, beklenen sonuçları sağlamayabilir. Bu durumda, el ile oluşturulan bildirim VSIX projesine eklemeniz gerekir.  
  
## <a name="file-changes-in-project-and-item-templates"></a>Proje ve öğe şablonlarını dosya değişiklikleri  
 Yeni dosyaları doğru oluşturabilmesi şablon dosyalarını, Visual Studio "15" sürümünü Visual Studio 2015 sürümü arasındaki fark noktalarını göstereceğiz.  
  
 Visual Studio 2015 tarafından oluşturulan varsayılan proje .vstemplate dosyası aşağıda verilmiştir:  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<VSTemplate Version="3.0.0" Type="Project" xmlns="http://schemas.microsoft.com/developer/vstemplate/2005" xmlns:sdk="http://schemas.microsoft.com/developer/vstemplate-sdkextension/2010">  
  <TemplateData>  
    <Name>ProjectTemplate1</Name>  
    <Description>ProjectTemplate1</Description>  
    <Icon>ProjectTemplate1.ico</Icon>  
    <ProjectType>CSharp</ProjectType>  
    <RequiredFrameworkVersion>2.0</RequiredFrameworkVersion>  
    <SortOrder>1000</SortOrder>  
    <TemplateID>05b79cc9-2146-4716-a8e5-7e085cdd2221</TemplateID>  
    <CreateNewFolder>true</CreateNewFolder>  
    <DefaultName>ProjectTemplate1</DefaultName>  
    <ProvideDefaultName>true</ProvideDefaultName>  
  </TemplateData>  
  <TemplateContent>  
    <Project File="ProjectTemplate.csproj" ReplaceParameters="true">  
      <ProjectItem ReplaceParameters="true" TargetFileName="Properties\AssemblyInfo.cs">AssemblyInfo.cs</ProjectItem>  
      <ProjectItem ReplaceParameters="true" OpenInEditor="true">Class1.cs</ProjectItem>  
    </Project>  
  </TemplateContent>  
</VSTemplate>  
  
```  
  
 VSIX projesi yeniden gelen sonuçlandı .vstman dosyayı (Bu bildirim VSIX proje dizininde bulabilirsiniz) şu şekildedir:  
  
```  
VSTemplateManifest Version="1.0" Locale="1033" xmlns="http://schemas.microsoft.com/developer/vstemplatemanifest/2015">  
  <VSTemplateContainer TemplateType="Project">  
    <RelativePathOnDisk>CSharp\1033\ProjectTemplate1</RelativePathOnDisk>  
    <TemplateFileName>ProjectTemplate1.vstemplate</TemplateFileName>  
    <VSTemplateHeader>  
      <TemplateData xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
        <Name>ProjectTemplate1</Name>  
        <Description>ProjectTemplate1</Description>  
        <Icon>ProjectTemplate1.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <RequiredFrameworkVersion>2.0</RequiredFrameworkVersion>  
        <SortOrder>1000</SortOrder>  
        <TemplateID>05b79cc9-2146-4716-a8e5-7e085cdd2221</TemplateID>  
        <CreateNewFolder>true</CreateNewFolder>  
        <DefaultName>ProjectTemplate1</DefaultName>  
        <ProvideDefaultName>true</ProvideDefaultName>  
      </TemplateData>  
    </VSTemplateHeader>  
  </VSTemplateContainer>  
</VSTemplateManifest>  
  
```  
  
 Tarafından sağlanan bilgileri [TemplateData](../extensibility/templatedata-element-visual-studio-templates.md) öğesi aynı kalır. **\<VSTemplateContainer >** öğesi ilişkili şablonu için .vstemplate dosyasını işaret eder.  
  
 Visual Studio 2015 tarafından oluşturulan varsayılan öğe .vstemplate dosyası aşağıda verilmiştir:  
  
```xml  
<?xml version="1.0" encoding="utf-8"?>  
<VSTemplate Version="3.0.0" Type="Item" xmlns="http://schemas.microsoft.com/developer/vstemplate/2005" xmlns:sdk="http://schemas.microsoft.com/developer/vstemplate-sdkextension/2010">  
  <TemplateData>  
    <Name>ItemTemplate1</Name>  
    <Description>ItemTemplate1</Description>  
    <Icon>ItemTemplate1.ico</Icon>  
    <TemplateID>bfeadf8e-a251-4109-b605-516b88e38c8d</TemplateID>  
    <ProjectType>CSharp</ProjectType>  
    <RequiredFrameworkVersion>2.0</RequiredFrameworkVersion>  
    <NumberOfParentCategoriesToRollUp>1</NumberOfParentCategoriesToRollUp>  
    <DefaultName>Class.cs</DefaultName>  
  </TemplateData>  
  <TemplateContent>  
    <References>  
      <Reference>  
        <Assembly>System</Assembly>  
      </Reference>  
    </References>  
    <ProjectItem ReplaceParameters="true">Class.cs</ProjectItem>  
  </TemplateContent>  
</VSTemplate>  
  
```  
  
 VSIX projesi yeniden gelen sonuçlandı .vstman dosyayı (Bu bildirim VSIX proje dizininde bulabilirsiniz) şu şekildedir:  
  
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
  
 Tarafından sağlanan bilgileri  **\<TemplateData >** öğesi aynı kalır. **\<VSTemplateContainer >** öğesi işaret ilişkili şablonu için .vstemplate dosyasının  
  
 .Vstman dosyanın farklı öğeler hakkında daha fazla bilgi için bkz. [Visual Studio şablon bildirim şeması başvurusu](../extensibility/visual-studio-template-manifest-schema-reference.md).  
  
## <a name="upgrades-for-extensions-installed-with-an-msi"></a>Uzantıları yükseltme ile yüklenen bir. MSI  
 Bazı MSI tabanlı uzantılar şablonları yaygın şablon konumları aşağıdaki gibi dağıtın:  
  
- **\<Visual Studio yükleme dizini > \Common7\IDE\\< ProjectTemplates/öğe şablonları >**  
  
- **\<Visual Studio yükleme dizini > \Common7\IDE\Extensions\\< ExtensionName\>\\< proje/öğe şablonları >**  
  
  Uzantınızı MSI tabanlı bir dağıtım gerçekleştiriyorsa, şablon bildirimi el ile oluşturun ve uzantı kurulumunda yer aldığından emin olun gerekir. Yukarıda listelenen .vstman örnekler karşılaştırmanız gerekir ve [Visual Studio şablon bildirim şeması başvurusu](../extensibility/visual-studio-template-manifest-schema-reference.md). ne kadar eklemeniz gerekir  
  
  Proje ve öğe şablonları için ayrı bildirimler oluşturmanız gerekir ve kök şablon dizini için belirtilen yukarıdaki işaret etmelidir. Uzantı ve yerel ayar başına bir bildirim oluşturmalısınız.  
  
## <a name="troubleshooting-template-installation"></a>Şablon yükleme sorunlarını giderme  
 Proje veya öğe şablonlarınızın dağıtımı sorunlarla karşılaşırsanız, tanılama günlük kaydını etkinleştirebilirsiniz.  
  
1. Günlüğe kaydetmeyi etkinleştirmek için kayıt defteri anahtarını ayarlamak için aşağıdaki komutu çalıştırın:  
  
    **reg HKCU\software\microsoft\visualstudio\15.0_Config\VSTemplate /v EnableTemplateDiscoveryLog /t REG_DWORD /d 1 Ekle**  
  
2. Visual Studio'yu başlatın ve her iki şablon ağaçları başlatmak için yeni proje ve yeni öğe iletişim kutularında başlatın. Şablon günlük görüntülenir **%LOCALAPPDATA%\Microsoft\VisualStudio\15.0\VsTemplateDiagnosticsList.csv**. Her şablon ağaç başlatma için bu günlük girdileri ekler.  
  
   Günlük dosyası şu sütunları içerir:  
  
-   **FullPathToTemplate**, aşağıdaki değerleri vardır:  
  
    -   bildirim tabanlı bir dağıtım için 1  
  
    -   disk tabanlı bir dağıtım için 0  
  
-   **TemplateFileName**  
  
-   Diğer şablonu özellikleri

