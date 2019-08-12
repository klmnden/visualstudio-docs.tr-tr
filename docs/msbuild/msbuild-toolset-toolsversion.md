---
title: MSBuild Araç Takımı (araçları sürümü) | Microsoft Docs
ms.date: 01/31/2018
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, multitargeting
- targeting a specific .NET framework [MSBuild]
- MSBuild, targeting a specific .NET framework
- multitargeting [MSBuild]
ms.assetid: 40040ee7-4620-4043-a6d8-ccba921421d1
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f87513a8124b728568f78bee9efdf48fb35a5301
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68926382"
---
# <a name="msbuild-toolset-toolsversion"></a>MSBuild Araç Takımı (ToolsVersion)

MSBuild bir uygulama oluşturmak için bir görev, hedef ve araç araç kümesi kullanır. Genellikle, bir MSBuild Araç Takımı *Microsoft. Common. Tasks* dosyasını, *Microsoft. Common. targets* dosyasını ve *CSC. exe* ve *Vbc. exe*gibi derleyicileri içerir. Çoğu araç kümesi, .NET Framework birden fazla sürümüne ve birden fazla sistem platformuna uygulama derlemek için kullanılabilir. Ancak, MSBuild 2,0 araç takımı yalnızca .NET Framework 2,0 ' i hedeflemek için kullanılabilir.

## <a name="toolsversion-attribute"></a>Araçları sürüm özniteliği
::: moniker range=">=vs-2019"
 Proje dosyasındaki `ToolsVersion` [Proje](../msbuild/project-element-msbuild.md) öğesindeki özniteliğinde araç takımını belirtin. Aşağıdaki örnek, projenin MSBuild "Current" araç takımı kullanılarak oluşturulması gerektiğini belirtir.

```xml
<Project ToolsVersion="Current" ... </Project>
```

::: moniker-end

::: moniker range="vs-2017"
 Proje dosyasındaki `ToolsVersion` [Proje](../msbuild/project-element-msbuild.md) öğesindeki özniteliğinde araç takımını belirtin. Aşağıdaki örnek, projenin MSBuild 15,0 araç kümesi kullanılarak oluşturulması gerektiğini belirtir.

```xml
<Project ToolsVersion="15.0" ... </Project>
```

::: moniker-end

> [!NOTE]
> Bazı proje türleri `sdk` `ToolsVersion`yerine özniteliğini kullanır. Daha fazla bilgi için bkz. [.NET Core için csproj biçimine](/dotnet/core/tools/csproj)yönelik [paketler, meta veriler ve çerçeveler](/dotnet/core/packages) ve eklemeler.

## <a name="how-the-toolsversion-attribute-works"></a>Araçları sürüm özniteliği nasıl kullanılır?

 Visual Studio 'da bir proje oluşturduğunuzda veya mevcut bir projeyi yükselttiğinizde, adlı `ToolsVersion` bir öznitelik proje dosyasına otomatik olarak eklenir ve değeri Visual Studio sürümüne dahil olan MSBuild sürümüne karşılık gelir. Daha fazla bilgi için bkz. [Çerçeve hedefleme genel bakış](../ide/visual-studio-multi-targeting-overview.md).

 Bir proje `ToolsVersion` dosyasında bir değer tanımlandığında, MSBuild bu değeri, projenin kullanabildiği araç kümesi özelliklerinin değerlerini belirlemekte kullanır. Bir araç takımı özelliği `$(MSBuildToolsPath)`, .NET Framework araçlarının yolunu belirtir. Yalnızca bu araç takımı özelliği ( `$(MSBuildBinPath)`veya) gereklidir.

 Visual Studio 2013 başlayarak, MSBuild Araç Takımı sürümü Visual Studio sürüm numarasıyla aynıdır. MSBuild, proje dosyasında belirtilen araç kümesi sürümünden bağımsız olarak Visual Studio içinde ve komut satırında bu araç takımını varsayılan olarak belirler.  Bu davranış,-, sürüm bayrağı kullanılarak geçersiz kılınabilir. Daha fazla bilgi için bkz. [araçları sürüm ayarlarını geçersiz kılma](../msbuild/overriding-toolsversion-settings.md).

 Aşağıdaki örnekte, MSBuild, `MSBuildToolsPath` ayrılmış özelliğini kullanarak *Microsoft. CSharp. targets* dosyasını bulur.

```xml
<Import Project="$(MSBuildToolsPath)\Microsoft.CSharp.targets" />
```

 Değerini `MSBuildToolsPath` özel bir araç kümesi tanımlayarak değiştirebilirsiniz. Daha fazla bilgi için bkz. [Standart ve özel araç takımı yapılandırması](../msbuild/standard-and-custom-toolset-configurations.md).

 Komut satırında bir çözüm oluşturduğunuzda ve `ToolsVersion` *MSBuild. exe*için bir belirleme belirttiğinizde, çözümdeki her proje kendi kendine `ToolsVersion` belirtsebiletümprojelerveproje-projebağımlılıklarıbunagöreoluşturulur `ToolsVersion`. `ToolsVersion` Değeri proje başına olarak tanımlamak için bkz. [araçları sürüm ayarlarını geçersiz kılma](../msbuild/overriding-toolsversion-settings.md).

 Özniteliği `ToolsVersion` , proje geçişi için de kullanılır. Örneğin, Visual Studio 2010 ' de bir Visual Studio 2008 projesi açarsanız proje dosyası, araçları sürümü = "4.0" olarak güncelleştirilir. Daha sonra bu projeyi Visual Studio 2008 ' de açmaya çalışırsanız bu, yükseltilen `ToolsVersion` öğesini tanımaz ve bu nedenle projeyi özniteliği hala 3,5 olarak ayarlanmış gibi oluşturur.

 Visual Studio 2010 ve Visual Studio 2012, 4,0 için bir araçları sürümü kullanır. Visual Studio 2013, 12,0 'in bir araçları sürümünü kullanır. Visual Studio 2015, araçları sürüm 14,0 ' nı kullanır ve Visual Studio 2017, araçları sürüm 15,0 kullanır. Birçok durumda, Visual Studio 'nun birden çok sürümünde değişiklik yapmadan projeyi açabilirsiniz. Visual Studio daima doğru araç takımını kullanır, ancak kullanılan sürüm proje dosyasındaki sürümle eşleşmezse size bildirilir. Neredeyse her durumda, araç kümeleri çoğu durumda uyumlu olduğu için bu uyarı zararsız olur.

 Bu konunun ilerleyen kısımlarında açıklanan alt araç kümeleri, MSBuild 'in çalıştırıldığı bağlama göre kullanılacak araç kümesini otomatik olarak değiştirmesine izin verir. Örneğin, MSBuild, proje dosyasını açıkça değiştirmek zorunda kalmadan Visual Studio 2012 ' de çalıştırıl2010 masından daha yeni bir araç kümesi kullanır.

## <a name="toolset-implementation"></a>Araç takımı uygulama

 Araç takımını oluşturan çeşitli araçların, hedeflerin ve görevlerin yollarını seçerek bir araç takımı uygulayın. MSBuild 'in tanımladığı araç takımı içindeki Araçlar aşağıdaki kaynaklardan gelir:

- .NET Framework klasörü.

- Ek yönetilen araçlar.

  Yönetilen Araçlar *Resgen. exe* ve *Tlbimp. exe*' yi içerir.

MSBuild, araç seti 'ne erişmenin iki yolunu sağlar:

- Araç kümesi özelliklerini kullanarak

- Yöntemleri kullanarak <xref:Microsoft.Build.Utilities.ToolLocationHelper>

Araç kümesi özellikleri araçların yollarını belirtir. Visual Studio 2017 ' den başlayarak MSBuild artık sabit bir konuma sahip değildir. Varsayılan olarak, Visual Studio yükleme konumuna göre *Msbuild\15.0\Bin* klasöründe bulunur. Daha önceki sürümlerde MSBuild, karşılık gelen kayıt defteri anahtarını `ToolsVersion` bulmak için proje dosyasındaki özniteliğin değerini kullanır ve ardından araç kümesi özelliklerini ayarlamak için kayıt defteri anahtarındaki bilgileri kullanır. Örneğin, değeri `12.0`varsa `ToolsVersion` MSBuild, araç kümesi özelliklerini bu kayıt defteri anahtarına göre ayarlar: **Hklm\software\microsoft\msbuild\tools\versions\12.0**.

 Araç kümesi özellikleri şunlardır:

- `MSBuildToolsPath`MSBuild ikili dosyalarının yolunu belirtir.

- `SDK40ToolsPath`MSBuild 4. x için ek yönetilen araçların yolunu belirtir (4,0 veya 4,5 olabilir).

- `SDK35ToolsPath`MSBuild 3,5 için ek yönetilen araçların yolunu belirtir.

Alternatif olarak, <xref:Microsoft.Build.Utilities.ToolLocationHelper> sınıfının yöntemlerini çağırarak araç takımını programlı bir şekilde belirleyebilirsiniz. Sınıfı şu yöntemleri içerir:

- <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFramework%2A>.NET Framework klasörünün yolunu döndürür.

- <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFrameworkFile%2A>.NET Framework klasöründeki bir dosyanın yolunu döndürür.

- <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFrameworkSdk%2A>yönetilen araçlar klasörünün yolunu döndürür.

- <xref:Microsoft.Build.Utilities.ToolLocationHelper.GetPathToDotNetFrameworkSdkFile%2A>genellikle yönetilen Araçlar klasöründe bulunan bir dosyanın yolunu döndürür.

- [Getpathtobuildtools](/previous-versions/visualstudio/visual-studio-2013/dn251121(v=vs.121)) , derleme araçlarının yolunu döndürür.

### <a name="sub-toolsets"></a>Alt araç kümeleri

 MSBuild 15,0 ' den önceki sürümler için, temel araçların yolunu belirtmek üzere bir kayıt defteri anahtarı kullanır. Anahtarın bir alt anahtarı varsa, MSBuild bunu ek araçlar içeren bir alt araç takımının yolunu belirtmek için kullanır. Bu durumda, araç takımı her iki anahtar içinde tanımlanmış özellik tanımlarını birleştirerek tanımlanır.

> [!NOTE]
> Araç kümesi özellik adları çakışıyorsa, alt anahtar yolu için tanımlanan değer kök anahtar yolu için tanımlanan değeri geçersiz kılar.

 Alt araç kümeleri `VisualStudioVersion` Build özelliğinin varlığı içinde etkin hale gelir. Bu özellik şu değerlerden birini alabilir:

- "10,0" .NET Framework 4 alt araç takımını belirtir

- "11,0" .NET Framework 4,5 alt araç takımını belirtir

- "12,0" .NET Framework 4.5.1 alt araç takımını belirtir

10,0 ve 11,0 alt araç kümeleri, Araçlar sürüm 4,0 ile kullanılmalıdır. Sonraki sürümlerde alt araç takımı sürümü ve araçları sürümü eşleşmelidir.

Bir derleme sırasında, MSBuild, zaten tanımlanmamışsa `VisualStudioVersion` özellik için varsayılan değeri otomatik olarak belirler ve ayarlar.

MSBuild, `ToolLocationHelper` bir parametre olarak `VisualStudioVersion` Numaralandırılmış değer ekleyen yöntemler için aşırı yüklemeler sağlar

.NET Framework 4,5 ' de alt araç kümeleri tanıtılmıştı.

## <a name="see-also"></a>Ayrıca bkz.

- [Standart ve özel araç takımı yapılandırması](../msbuild/standard-and-custom-toolset-configurations.md)
- [Çoklu Sürüm Desteği](../msbuild/msbuild-multitargeting-overview.md)
