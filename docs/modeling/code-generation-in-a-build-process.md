---
title: Derleme Sürecinde Kod Oluşturma
ms.date: 03/22/2018
ms.topic: conceptual
helpviewer_keywords:
- text templates, build tasks
- text templates, transforming by using msbuild
author: gewarren
ms.author: gewarren
manager: jillfra
dev_langs:
- CSharp
- VB
ms.workload:
- multiple
ms.openlocfilehash: b3d61a5bcd530afb951f98f84f1f4e38e36f96d6
ms.sourcegitcommit: 9cfd3ef6c65f671a26322320818212a1ed5955fe
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/26/2019
ms.locfileid: "68533311"
---
# <a name="code-generation-in-a-build-process"></a>Derleme işleminde kod üretimi

[Metin dönüşümü](../modeling/code-generation-and-t4-text-templates.md) , Visual Studio çözümünün [derleme sürecinin](/azure/devops/pipelines/index) bir parçası olarak çağrılabilir. Metin dönüştürme için özelleştirilmiş yapı görevleri vardır. T4 yapı görevleri tasarım zamanı metin şablonlarını çalıştırır ve aynı zamanda çalışma zamanı (önişlenmiş) metin şablonlarını derler.

Kullandığınız oluşturma motoruna bağlı olarak, yapı görevleri farklı işlevleri yerine getirebilirler. Visual Studio 'da çözümü oluşturduğunuzda, [hostspecific = "true"](../modeling/t4-template-directive.md) özniteliği ayarlandıysa bir metin şablonu Visual Studio API 'Sine (EnvDTE) erişebilir. Bu, çözümü komut satırından oluşturduğunuzda ya da Visual Studio aracılığıyla bir sunucu derlemesi başlattığınızda doğru değildir. Bu durumlarda, yapı MSBuild tarafından oluşturulur ve farklı bir T4 ana bilgisayar kullanılır. Bu, MSBuild kullanarak bir metin şablonu oluşturduğunuzda, proje dosya adları gibi şeylere aynı şekilde erişemeyeceğiniz anlamına gelir. Ancak, [Yapı parametrelerini kullanarak ortam bilgilerini metin şablonlarına ve yönerge işlemcilere geçirebilirsiniz](#parameters).

## <a name="buildserver"></a>Makinelerinizi yapılandırma

Geliştirme bilgisayarınızda derleme görevlerini etkinleştirmek için, Visual Studio için modelleme SDK 'sını yükler.

[!INCLUDE[modeling_sdk_info](includes/modeling_sdk_info.md)]

[Yapı sunucunuz](/azure/devops/pipelines/agents/agents) , Visual Studio 'nun yüklü olmadığı bir bilgisayarda çalışıyorsa, aşağıdaki dosyaları geliştirme makinenizden yapı bilgisayarına kopyalayın. ' * ' İçin en son sürüm numaralarını değiştirin.

- $ (ProgramFiles) \MSBuild\Microsoft\VisualStudio\v *. 0 \ Textşablon oluşturma

  - Microsoft.VisualStudio.TextTemplating.Sdk.Host.*.0.dll

  - Microsoft.TextTemplating.Build.Tasks.dll

  - Microsoft.TextTemplating.targets

- $ (ProgramFiles) \Microsoft Visual Studio *. 0 \ VSSDK\VisualStudioIntegration\Common\Assemblies\v4.0

  - Microsoft.VisualStudio.TextTemplating.*.0.dll

  - Microsoft.VisualStudio.TextTemplating.Interfaces.*.0.dll (several files)

  - Microsoft.VisualStudio.TextTemplating.VSHost.*.0.dll

- $ (ProgramFiles) \Microsoft Visual Studio *. 0 \ Common7\IDE\PublicAssemblies\

  - Microsoft.VisualStudio.TextTemplating.Modeling.*.0.dll
  
> [!TIP]
> Bir yapı sunucusunda textşablon oluşturma derleme hedeflerini çalıştırırken Microsoft. CodeAnalysis yöntemi  için,RoslynderlemelerininderlemeyürütülebiliriyleaynıdizindeolanRoslynadlıbirdizindeolduğundaneminolun(`MissingMethodException` Örneğin, *MSBuild. exe*).

## <a name="edit-the-project-file"></a>Proje dosyasını düzenleme

MSBuild 'teki bazı özellikleri yapılandırmak için proje dosyanızı düzenleyin, örneğin, metin dönüştürme hedeflerini içeri aktarma.

**Çözüm Gezgini**, projenizin sağ tıklama menüsünden **Kaldır** ' ı seçin. Bu .csproj veya .vbproj dosyasını XML düzenleyicisinde düzenlemenize olanak tanır. Düzenlemeden sonra **yeniden yükle**' yi seçin.

## <a name="import-the-text-transformation-targets"></a>Metin dönüştürme hedeflerini içeri aktarma

.Vbproj veya .csproj dosyasında şöyle bir satır bulun:

`<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />`

\- veya -

`<Import Project="$(MSBuildToolsPath)\Microsoft.VisualBasic.targets" />`

Bu satırın ardından, Metin Şablon Oluşturma almayı ekleyin:

```xml
<!-- Optionally make the import portable across VS versions -->
  <PropertyGroup>
    <!-- Get the Visual Studio version: -->
    <VisualStudioVersion Condition="'$(VisualStudioVersion)' == ''">16.0</VisualStudioVersion>
    <!-- Keep the next element all on one line: -->
    <VSToolsPath Condition="'$(VSToolsPath)' == ''">$(MSBuildExtensionsPath32)\Microsoft\VisualStudio\v$(VisualStudioVersion)</VSToolsPath>
  </PropertyGroup>

<!-- This is the important line: -->
  <Import Project="$(VSToolsPath)\TextTemplating\Microsoft.TextTemplating.targets" />
```

## <a name="transform-templates-in-a-build"></a>Yapı içindeki şablonları dönüştürme

Dönüştürme görevini kontrol etmek için proje dosyanızın içine ekleyebileceğiniz bazı özellikler vardır:

- Dönüştürme görevini her yapı başlangıcında çalıştır:

    ```xml
    <PropertyGroup>
        <TransformOnBuild>true</TransformOnBuild>
    </PropertyGroup>
    ```

- Salt okunan dosyaların üzerine yazılır, örneğin, kullanıma alınmamış oldukları için:

    ```xml
    <PropertyGroup>
        <OverwriteReadOnlyOutputFiles>true</OverwriteReadOnlyOutputFiles>
    </PropertyGroup>
    ```

- Her şablonu her zaman dönüştür:

    ```xml
    <PropertyGroup>
        <TransformOutOfDateOnly>false</TransformOutOfDateOnly>
    </PropertyGroup>
    ```

     Varsayılan olarak, T4 MSBuild görevi şundan eskiyse bir çıkış dosyası oluşturur:
     
     - şablon dosyası
     - dahil edilen tüm dosyalar
     - daha önce şablon tarafından veya kullandığı bir yönerge işlemcisi tarafından okunmuş olan dosyalar
     
     Bu, yalnızca şablonun ve çıkış dosyasının tarihlerini karşılaştıran Visual Studio 'daki **Tüm Şablonları Dönüştür** komutu tarafından kullanılandan daha güçlü bir bağımlılık sınamadır.

Projenizde yalnızca metin dönüştürmeleri gerçekleştirmek için TransformAll görevini çağırın:

`msbuild myProject.csproj /t:TransformAll`

Belirli metin şablonu dönüştürmek için:

`msbuild myProject.csproj /t:Transform /p:TransformFile="Template1.tt"`

TransformFile içinde joker karakterler kullanabilirsiniz:

`msbuild dsl.csproj /t:Transform /p:TransformFile="GeneratedCode\**\*.tt"`

## <a name="source-control"></a>Kaynak denetimi

Kaynak denetim sistemi ile yerleşik herhangi bir tümleştirme yoktur. Bununla birlikte, örneğin, bir oluşturulan dosyayı kullanıma almak ve iade etmek için kendi uzantılarınızı ekleyebilirsiniz. Varsayılan olarak, metin dönüştürme görevi salt okunurdur olarak işaretlenen bir dosyanın üzerine yazılmasını önler. Böyle bir dosya ile karşılaşıldığında, Visual Studio Hata Listesi bir hata günlüğe kaydedilir ve görev başarısız olur.

Salt okunur dosyaların üzerine yazılması gerektiğini belirtmek için bu özelliği ekleyin:

`<OverwriteReadOnlyOutputFiles>true</OverwriteReadOnlyOutputFiles>`

Özelleştirmediğiniz adımını özelleştirmediğiniz takdirde, bir dosyanın üzerine yazıldığında hata listesi bir uyarı kaydedilir.

## <a name="customize-the-build-process"></a>Yapı işlemini özelleştirme

Oluşturma işleminde diğer görevlerden önce metin dönüştürme gerçekleşir. Dönüşümden önce ve sonra çağrılan görevleri ve `$(BeforeTransform)` `$(AfterTransform)`özelliklerini ayarlayarak tanımlayabilirsiniz:

```xml
<PropertyGroup>
    <BeforeTransform>CustomPreTransform</BeforeTransform>
    <AfterTransform>CustomPostTransform</AfterTransform>
  </PropertyGroup>
  <Target Name="CustomPreTransform">
    <Message Text="In CustomPreTransform..." Importance="High" />
  </Target>
  <Target Name="CustomPostTransform">
    <Message Text="In CustomPostTransform..." Importance="High" />
  </Target>
```

' `AfterTransform`De, dosya listelerine başvurabilirsiniz:

- GeneratedFiles - işlem tarafından yazılan dosyaların listesi. Varolan salt okuma dosyalarını `%(GeneratedFiles.ReadOnlyFileOverwritten)` içeren dosyalar için doğru olacaktır. Bu dosyalar kaynak denetiminden denetlenebilir.

- NonGeneratedFiles - üzerine yazılmamış, salt okunur dosyaların listesi.

Örneğin, GeneratedFiles'ı kullanıma almak için bir görev tanımlarsınız.

## <a name="outputfilepath-and-outputfilename"></a>OutputFilePath ve OutputFileName

Bu özellikler yalnızca MSBuild tarafından kullanılır. Visual Studio'da kod üretimi etkilemez. Bunlar, oluşturulan çıktı dosyasını farklı bir klasör veya dosyaya yeniden yönlendirir. Hedef klasörün zaten bulunması gerekir.

```xml
<ItemGroup>
  <None Include="MyTemplate.tt">
    <Generator>TextTemplatingFileGenerator</Generator>
    <OutputFilePath>MyFolder</OutputFilePath>
    <LastGenOutput>MyTemplate.cs</LastGenOutput>
  </None>
</ItemGroup>
```

Yeniden yönlendirileceği `$(IntermediateOutputPath)`yararlı bir klasör.

Bir çıkış dosya adı belirtirseniz, şablonlarda çıkış yönergesinde belirtilen uzantıya göre öncelik kazanır.

```xml
<ItemGroup>
  <None Include="MyTemplate.tt">
    <Generator>TextTemplatingFileGenerator</Generator>
    <OutputFileName>MyOutputFileName.cs</OutputFileName>
    <LastGenOutput>MyTemplate.cs</LastGenOutput>
  </None>
</ItemGroup>
```

Visual Studio 'Nun içindeki şablonları tek tek dosya **oluşturucuyu kullanarak dönüştürüyorsanız** de bir outputFilename veya OutputFilePath belirtilmesi önerilmez. Dönüştürmeyi nasıl tetiklediğinize bağlı olarak farklı dosya yolları ile karşılaşırsınız. Bu kafa karıştırıcı olabilir.

## <a name="add-reference-and-include-paths"></a>Başvuru ve ekleme yolları Ekle

Ana bilgisayar, şablonlarda başvurulan derlemeler için arama yaptığı varsayılan bir grup yola sahiptir. Bu gruba ekleme yapmak için:

```xml
<ItemGroup>
    <T4ReferencePath Include="$(VsIdePath)PublicAssemblies\" />
    <!-- Add more T4ReferencePath items here -->
</ItemGroup>
```

Ekleme kodu dosyalarının aranacağı klasörleri ayarlamak için, noktalı virgülle ayrılmış bir liste sağlayın. Genellikle varolan klasör listesine eklersiniz.

```xml
<PropertyGroup>
    <IncludeFolders>
$(IncludeFolders);$(MSBuildProjectDirectory)\Include;AnotherFolder;And\Another</IncludeFolders>
</PropertyGroup>
```

## <a name="parameters"></a>Yapı bağlamı verilerini şablonlara geçirme

Proje dosyasında parametre değerlerini ayarlayabilirsiniz. Örneğin, [Yapı](../msbuild/msbuild-properties.md) özelliklerini ve [ortam değişkenlerini](../msbuild/how-to-use-environment-variables-in-a-build.md)geçirebilirsiniz:

```xml
<ItemGroup>
  <T4ParameterValues Include="ProjectFolder">
    <Value>$(ProjectDir)</Value>
    <Visible>false</Visible>
  </T4ParameterValues>
</ItemGroup>
```

Bir metin şablonunda, şablon yönergesinde `hostspecific` öğesini ayarlayın. Değerleri almak için [Parameter](../modeling/t4-parameter-directive.md) yönergesini kullanın:

```
<#@template language="c#" hostspecific="true"#>
<#@ parameter type="System.String" name="ProjectFolder" #>
The project folder is: <#= ProjectFolder #>
```

Yönerge işlemcisinde [ITextTemplatingEngineHost. ResolveParameterValue](/previous-versions/visualstudio/visual-studio-2012/bb126369\(v\=vs.110\))öğesini çağırabilirsiniz:

```csharp
string value = Host.ResolveParameterValue("-", "-", "parameterName");
```

```vb
Dim value = Host.ResolveParameterValue("-", "-", "parameterName")
```

> [!NOTE]
> `ResolveParameterValue`yalnızca MSBuild 'i `T4ParameterValues` kullandığınızda verileri alır. Visual Studio kullanarak şablonu dönüştürdüğünüzde, parametrelerin varsayılan değerleri vardır.

## <a name="msbuild"></a>Derleme ve ekleme yönergeleri içindeki proje özelliklerini kullanma

**$ (SolutionDir)** gibi Visual Studio makroları MSBuild 'de çalışmıyor. Bunun yerine, proje özelliklerini kullanabilirsiniz.

Bir proje özelliği tanımlamak için *. csproj* veya *. vbproj* dosyanızı düzenleyin. Bu örnek, **Mylibfolder**adlı bir özelliği tanımlar:

```xml
<!-- Define a project property, myLibFolder: -->
<PropertyGroup>
    <myLibFolder>$(MSBuildProjectDirectory)\..\libs</myLibFolder>
</PropertyGroup>

<!-- Tell the MSBuild T4 task to make the property available: -->
<ItemGroup>
    <T4ParameterValues Include="myLibFolder">
      <Value>$(myLibFolder)</Value>
    </T4ParameterValues>
  </ItemGroup>
```

Artık derlemede ve ekleme yönergelerinde proje özelliklerini kullanabilirsiniz:

```
<#@ assembly name="$(myLibFolder)\MyLib.dll" #>
<#@ include file="$(myLibFolder)\MyIncludeFile.t4" #>
```

Bu yönergeler, hem MSBuild içinde hem de Visual Studio ana bilgisayarlarında T4parameterValues değerlerini alır.

## <a name="q--a"></a>Soru - Yanıt

**Neden yapı sunucusundaki şablonları dönüştürmek istiyorum? Kodumu iade etmeden önce Visual Studio 'daki şablonları zaten dönüştürtim.**

Dahil edilen bir dosyayı veya şablon tarafından okunan başka bir dosyayı güncelleştirirseniz, Visual Studio dosyayı otomatik olarak dönüştürmez. Derleme kapsamında şablonların dönüştürülmesi, her şeyin güncel olduğundan emin olmanızı sağlar.

**Metin şablonlarını dönüştürmek için diğer seçenekler nelerdir?**

- [TextTransform yardımcı programı](../modeling/generating-files-with-the-texttransform-utility.md) komut betiklerine uygulanabilir. Çoğu durumda, MSBuild kullanmak daha kolay olur.

- [Visual Studio uzantısında metin dönüştürmeyi çağırın](../modeling/invoking-text-transformation-in-a-vs-extension.md).

- [Tasarım zamanı metin şablonları](../modeling/design-time-code-generation-by-using-t4-text-templates.md) , Visual Studio tarafından dönüştürülür.

- [Çalışma zamanı metin şablonları](../modeling/run-time-text-generation-with-t4-text-templates.md) uygulamanızdaki çalışma zamanında dönüştürülür.

## <a name="see-also"></a>Ayrıca bkz.

::: moniker range="vs-2017"

- *% ProgramFiles (x86)% \ Microsoft Visual Studio\2017\Enterprise\msbuild\Microsoft\VisualStudio\v15.0\TextTemplating\Microsoft.TextTemplating.targets* konumundaki T4 MSBuild şablonunda iyi bir kılavuzluk var

::: moniker-end

::: moniker range=">=vs-2019"

- *% ProgramFiles (x86)% \ Microsoft Visual Studio\2019\Enterprise\msbuild\Microsoft\VisualStudio\v16.0\TextTemplating\Microsoft.TextTemplating.targets* konumundaki T4 MSBuild şablonunda iyi bir kılavuzluk var

::: moniker-end

- [T4 metin şablonu yazma](../modeling/writing-a-t4-text-template.md)
