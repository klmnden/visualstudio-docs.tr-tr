---
title: Derleme Sistemini Özelleştirme
description: Bu makale, Mac için Visual Studio tarafından kullanılan MSBuild derleme sistemine kısa bir giriş niteliğindedir
author: heiligerdankgesang
ms.author: dominicn
ms.date: 09/19/2019
ms.assetid: 6958B102-8527-4B40-BC65-3505DB63F9D3
ms.openlocfilehash: 0c511c448136210038f1034321a2828e5153add1
ms.sourcegitcommit: 53bc4c11b82882ab658e34c65ae374060f823531
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/19/2019
ms.locfileid: "71128383"
---
# <a name="customizing-the-build-system"></a>Yapı sistemini özelleştirme

Microsoft Build Engine, uygulama oluşturmaya yönelik bir platformdur. MSBuild olarak da bilinen altyapı, Microsoft tarafından geliştirilmiştir ve .NET uygulamalarının oluşturulmasına izin verir. Mono çerçevesinin Ayrıca, **xbuild**adlı Microsoft Build Engine uygulamasına sahip olması gerekir. Ancak, şu anda xbuild tüm işletim sistemlerinde MSBuild kullanımı için kullanıma hazır.

**MSBuild** , Mac için Visual Studio 'daki projeler için yapı sistemi olarak kullanılır ve kaynak dosyalar gibi bir giriş kümesi alarak ve bunları yürütülebilir dosyalar gibi çıkışlara dönüştürür. Derleyici gibi araçları çağırarak bu çıktıyı elde eder.

## <a name="msbuild-file"></a>MSBuild dosyası

MSBuild, projenizin bir parçası olan *öğeleri* (görüntü kaynakları gibi) ve projenizi oluşturmak Için gereken *özellikleri* tanımlayan bir proje dosyası adlı bir XML dosyası kullanır. Bu proje dosyası `proj`, projeler için `.csproj` C# gibi her zaman bir dosya uzantısına sahip olacaktır.

### <a name="viewing-the-msbuild-file"></a>MSBuild dosyasını görüntüleme

Proje adına sağ tıklayıp **Finder 'Da göster '** i seçerek MSBuild dosyasını bulun. Finder penceresinde, aşağıdaki görüntüde gösterildiği gibi, `.csproj` dosyası dahil olmak üzere projenizle ilgili tüm dosya ve klasörler görüntülenir:

![Finder 'da csproj konumu](media/customizing-build-system-image1.png)

Mac için Visual Studio yeni bir `.csproj` sekmede göstermek için, proje adına sağ tıklayın ve **dosyayı Düzenle > Araçlar**'a gidin:

![Kaynak düzenleyicisinde csproj açılıyor](media/customizing-build-system-image2.png)

### <a name="composition-of-the-msbuild-file"></a>MSBuild dosyasının oluşturulması

Tüm MSBuild dosyaları, şöyle bir zorunlu `Project` kök öğesi içerir:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="14.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

Genellikle proje de bir `.targets` dosyayı içeri aktarır. Bu dosya, çeşitli dosyaların nasıl işleyeceğini ve oluşturulacağını betimleyen kuralların çoğunu içerir. İçeri aktarma genellikle `proj` dosyanızın en altına doğru görünür ve projeler için C# şuna benzer şekilde görünür:

```xml
<Import Project="$(MSBuildBinPath)\Microsoft.CSharp.targets" />
```

Hedef dosya başka bir MSBuild dosyasıdır. Bu dosya, birden fazla proje tarafından yeniden kullanılabilen MSBuild kodunu içerir. Örneğin `Microsoft.CSharp.targets` `MSBuildBinPath` , özelliği (veya değişkeni) tarafından temsil edilen bir dizinde bulunan dosyası, C# C# kaynak dosyalardan derleme oluşturma mantığını içerir.

### <a name="items-and-properties"></a>Öğeler ve Özellikler

MSBuild 'de iki temel veri türü vardır: *öğeler* ve *Özellikler*aşağıdaki bölümlerde daha ayrıntılı olarak açıklanmıştır.

#### <a name="properties"></a>Özellikler

Özellikler, derleme seçenekleri gibi derlemeyi etkileyen ayarları depolamak için kullanılan anahtar/değer çiftleridir.

Bunlar bir PropertyGroup kullanılarak ayarlanırlar ve herhangi bir sayıda özellik içerebilen herhangi bir sayıda PropertiesGroups içerebilir.

Örneğin, bir basit konsol uygulaması için PropertyGroup aşağıdaki XML gibi görünebilir:

```xml
<PropertyGroup>
    <Configuration Condition=" '$(Configuration)' == '' ">Debug</Configuration>
    <Platform Condition=" '$(Platform)' == '' ">x86</Platform>
    <ProjectGuid>{E248730E-1393-43CC-9183-FFA42F63BE81}</ProjectGuid>
    <OutputType>Exe</OutputType>
    <RootNamespace>refactoring</RootNamespace>
    <AssemblyName>refactoring</AssemblyName>
    <TargetFrameworkVersion>v4.5</TargetFrameworkVersion>
</PropertyGroup>
```

Özellikler, `$()` söz dizimi kullanılarak ifadelerden ifade edilebilir. Örneğin, `$(Foo)` `Foo` özelliğinin değeri olarak değerlendirilir. Özellik ayarlanmamışsa, herhangi bir hata olmadan boş bir dize olarak değerlendirilir.

#### <a name="items"></a>Öğeler

Öğeler, derleme sistemine listeler veya kümeler olarak giriş ile ilgili bir yol sağlar ve genellikle dosyaları temsil eder. Her öğenin bir öğe *türü*, bir öğe *belirtimi*ve isteğe bağlı rastgele *meta veriler*vardır. MSBuild 'in ayrı öğeler üzerinde çalışmadığına, belirli bir türün tüm öğelerini (öğe *kümesi* olarak adlandırılır) aldığını unutmayın.

Öğeler bir `ItemGroup`bildirerek oluşturulur. Herhangi bir sayıda öğe içerebilen herhangi bir sayıda ItemGroups olabilir.

Örneğin, aşağıdaki kod parçacığı iOS başlatma ekranlarını oluşturur. Başlatma ekranları yapı türüne `BundleResource`sahiptir ve bu özellik, görüntünün yolu olarak belirtimdir:

```xml
 <ItemGroup>
    <BundleResource Include="Resources\Default-568h%402x.png" />
    <BundleResource Include="Resources\Default%402x.png" />
    <BundleResource Include="Resources\Default.png" />
    <BundleResource Include="Resources\Default-Portrait.png" />
    <BundleResource Include="Resources\Default-Portrait%402x.png" />
    <BundleResource Include="Resources\Default-Landscape%402x.png" />
  </ItemGroup>
 ```

 Öğe kümelerine `@()` sözdizimi kullanılarak deyimlerden başvurulabilir. Örneğin, `@(BundleResource)` paketleme leresource öğe kümesi olarak değerlendirilir. Bu, tüm paket \ kaynak öğeleri anlamına gelir. Bu türden bir öğe yoksa, herhangi bir hata olmadan boş olur.

## <a name="resources-for-learning-msbuild"></a>Öğrenme MSBuild için kaynaklar

Aşağıdaki kaynaklar MSBuild hakkında daha ayrıntılı bilgi edinmek için kullanılabilir:

* [MSBuild genel bakış](/visualstudio/msbuild/msbuild)
* [MSBuild Kavramları](/visualstudio/msbuild/msbuild-concepts)
