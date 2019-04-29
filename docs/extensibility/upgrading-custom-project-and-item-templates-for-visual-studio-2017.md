---
title: Özel proje ve öğe şablonları Visual Studio 2017 için yükseltme | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
ms.assetid: ad02477b-e101-4f32-aeb7-292bf95d5c2f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
monikerRange: vs-2017
ms.openlocfilehash: cb4defa206d176e57804e6d2473262568cd5edbf
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63434211"
---
# <a name="upgrade-custom-project-and-item-templates-for-visual-studio-2017"></a>Özel proje ve öğe şablonları Visual Studio 2017 için yükseltin

Visual Studio, Visual Studio 2017'den itibaren Visual Studio'nun önceki sürümleri için farklı bir şekilde bir .vsix veya bir. msi'nin tarafından yüklenmiş proje ve öğe şablonlarını bulur. Özel proje veya öğe şablonları kullanan uzantıları sahipseniz, uzantılarınız güncelleştirmeniz gerekiyor. Ne yapmanız gerekir, bu makalede açıklanır.

Bu değişiklik, yalnızca Visual Studio 2017 etkiler. Visual Studio'nun önceki sürümlerini etkilemez.

Bir VSIX uzantısının bir parçası olarak bir proje veya öğe şablonu oluşturmak istiyorsanız, bkz. [oluşturma özel Proje ve öğe şablonlarını](../extensibility/creating-custom-project-and-item-templates.md).

## <a name="template-scanning"></a>Tarama şablonu

Visual Studio'nun önceki sürümlerinde **devenv/Setup** veya **devenv /installvstemplates** proje ve öğe şablonlarını bulmak için yerel disk taranır. Visual Studio 2017'den itibaren tarama için kullanıcı düzeyi konum gerçekleştirilir. Varsayılan kullanıcı düzeyi konum **%USERPROFILE%\Documents\\< Visual Studio sürümü\>\Templates\\**. Bu konum için tarafından oluşturulan şablonlarını kullanılır **proje** > **şablonları dışarı aktar...**  , komut **otomatik olarak şablonu Visual Studio'ya içeri aktarma** seçeneği Sihirbazı'nda.

Diğer (kullanıcı olmayan) konumları için konumu ve diğer özellikleri de şablon belirten bir manifest(.vstman) dosyası eklemeniz gerekir. .Vstman dosya şablonları için kullanılan .vstemplate dosyasıyla birlikte oluşturulur. Uzantınızı bir .vsix kullanarak yüklerseniz, bu uzantı Visual Studio 2017'de derleyerek gerçekleştirebilirsiniz. Ancak bir. msi'nin kullanırsanız, değişiklikler el ile yapmanız gerekir. Bu değişiklikleri yapmak için yapmanız gerekenler bir listesi için bkz **yükseltme ile yüklenen uzantıları için bir. MSI** daha sonra bu sayfayı.

## <a name="how-to-update-a-vsix-extension-with-project-or-item-templates"></a>Bir VSIX uzantısı, proje veya öğe şablonları ile güncelleştirme

1. Çözümü Visual Studio 2017'de açın. Yükseltme kodu istenir. **Tamam**'ı tıklatın.

2. Yükseltme tamamlandıktan sonra yükleme hedef sürümünü değiştirmeniz gerekebilir. VSIX projesinde source.extension.vsixmanifest dosyasını açın ve seçin **hedefleri Yükle** sekmesi. Varsa **sürüm aralığı** alandır **[14.0]**, tıklayın **Düzenle** ve Visual Studio 2017 içerecek şekilde değiştirin. Örneğin, ayarlayabilirsiniz **[14.0,15.0]** Visual Studio 2015 veya Visual Studio 2017 veya için uzantıyı yüklemek için **[15.0]** yalnızca Visual Studio 2017'ye yüklemek için.

3. Kodu yeniden derleyin.

4. Visual Studio’yu kapatın.

5. VSIX yükleyin.

6. Güncelleştirme, aşağıdakileri yaparak test edebilirsiniz:

    1. Dosya değişikliği tarama, aşağıdaki kayıt defteri anahtarı tarafından etkinleştirilir:

         **reg hklm\software\microsoft\visualstudio\15.0\VSTemplate /v DisableTemplateScanning /t REG_DWORD /d 1 /reg:32 Ekle**

    2. Anahtarı ekledikten sonra Çalıştır **devenv /installvstemplates**.

    3. Visual Studio'yu yeniden açın. Beklenen konumda şablonunuzu bulmanız gerekir.

    > [!NOTE]
    > Visual Studio genişletilebilirlik proje şablonları kayıt defteri anahtarı mevcut olduğunda kullanılabilir değil. Kayıt defteri anahtarı silmelisiniz (ve yeniden **devenv /installvstemplates**) bunları kullanmak için.

## <a name="other-recommendations-for-deploying-project-and-item-templates"></a>Proje ve öğe şablonlarını dağıtmak için diğer öneriler

- Sıkıştırılmış şablon dosyaları kullanmaktan kaçının. Şablon kaynakları ve içerik almak için açılması gereken dosya daraltılmış, bu nedenle bunlar kullanılacak costlier olur. Bunun yerine, şablon başlatma ' hızlandırmak için kendi dizin altında tek tek dosya olarak proje ve öğe şablonlarını dağıtmanız gerekir. VSIX uzantıları için SDK derleme görevleri otomatik olarak herhangi bir daraltılmış şablon VSIX dosyasını oluştururken sıkıştırmasını.

- Paket/kaynak kimliği girdileri, şablon adı, açıklaması, simge için kullanmaktan kaçının veya şablon keşfi sırasında gereksiz kaynak derleme yüklerini önlemek için Önizleme. Bunun yerine, yerelleştirilmiş bildirimler yerelleştirilmiş adlar veya özellikleri kullanan her yerel ayar için bir şablon girişi oluşturmak için kullanabilirsiniz.

- Şablon olarak dosya öğeleri dahil olmak üzere, bildirim oluşturma, beklenen sonuçları sağlamayabilir. Bu durumda, VSIX projesine el ile oluşturulmuş bir bildirim eklemeniz gerekir.

## <a name="file-changes-in-project-and-item-templates"></a>Proje ve öğe şablonlarını dosya değişiklikleri
Böylece yeni dosyaları doğru bir şekilde oluşturabilir Visual Studio 2015 ve Visual Studio 2017 sürümleri şablon dosyaları arasındaki fark noktalarını göstereceğiz.

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

```xml
<VSTemplateManifest Version="1.0" Locale="1033" xmlns="http://schemas.microsoft.com/developer/vstemplatemanifest/2015">
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

 Tarafından sağlanan bilgileri [TemplateData](../extensibility/templatedata-element-visual-studio-templates.md) öğesi aynı kalır.  **\<VSTemplateContainer >** öğesi ilişkili şablonu için .vstemplate dosyasını işaret eder.

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

```xml
<VSTemplateManifest Version="1.0" Locale="1033" xmlns="http://schemas.microsoft.com/developer/vstemplatemanifest/2015">
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

 Tarafından sağlanan bilgileri  **\<TemplateData >** öğesi aynı kalır.  **\<VSTemplateContainer >** öğesi işaret ilişkili şablonu için .vstemplate dosyasının

 .Vstman dosyanın farklı öğeler hakkında daha fazla bilgi için bkz. [Visual Studio şablon bildirim şeması başvurusu](../extensibility/visual-studio-template-manifest-schema-reference.md).

## <a name="upgrades-for-extensions-installed-with-an-msi"></a>Uzantıları yükseltme ile yüklenen bir. MSI

Bazı MSI tabanlı uzantılar şablonları yaygın şablon konumları aşağıdaki dizinlerin gibi dağıtın:

- **\<Visual Studio yükleme dizini > \Common7\IDE\\< ProjectTemplates/öğe şablonları >**

- **\<Visual Studio yükleme dizini > \Common7\IDE\Extensions\\< ExtensionName\>\\< proje/öğe şablonları >**

Uzantınızı MSI tabanlı bir dağıtım gerçekleştiriyorsa, şablon bildirimi el ile oluşturun ve uzantı kurulumunda yer aldığından emin olun gerekir. Yukarıda listelenen .vstman örnekler karşılaştırın ve [Visual Studio şablon bildirim şeması başvurusu](../extensibility/visual-studio-template-manifest-schema-reference.md).

Proje ve öğe şablonları için ayrı bildirimler oluşturmak ve kök şablon dizini için belirtilen yukarıdaki işaret etmelidir. Uzantı ve yerel ayar başına bir bildirim oluşturun.

## <a name="see-also"></a>Ayrıca bkz.

- [Şablon bulma sorunlarını giderme](troubleshooting-template-discovery.md)
- [Özel proje ve öğe şablonları oluşturma](creating-custom-project-and-item-templates.md)