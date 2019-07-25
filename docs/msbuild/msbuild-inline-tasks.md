---
title: MSBuild satır Içi görevleri | Microsoft Docs
ms.date: 09/21/2017
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, tasks
ms.assetid: e72e6506-4a11-4edf-ae8d-cfb5a3b9d8a0
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 37597d1e1f4fde2b2e81e7aa7868c0aaff935337
ms.sourcegitcommit: 59e5758036223ee866f3de5e3c0ab2b6dbae97b6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "68416858"
---
# <a name="msbuild-inline-tasks"></a>MSBuild satır içi görevleri
MSBuild görevleri genellikle <xref:Microsoft.Build.Framework.ITask> arabirimini uygulayan bir sınıf derlenerek oluşturulur. Daha fazla bilgi için bkz. [Görevler](../msbuild/msbuild-tasks.md).

 .NET Framework sürüm 4 ' te başlayarak, proje dosyasında görevleri satır içinde oluşturabilirsiniz. Görevi barındırmak için ayrı bir derleme oluşturmanız gerekmez. Bu, kaynak kodu izlemeyi daha kolay hale getirir ve görevi dağıtmayı kolaylaştırır. Kaynak kodu betiğe tümleştirilir.

 MSBuild 15,8 ' de [Roslyncodetaskfactory](../msbuild/msbuild-roslyncodetaskfactory.md) , .NET Standard platformlar arası satır içi görevler oluşturabilecek şekilde eklenmiştir.  .NET Core 'da satır içi görevler kullanmanız gerekiyorsa, RoslynCodeTaskFactory ' yi kullanmanız gerekir.
## <a name="the-structure-of-an-inline-task"></a>Satır içi görevin yapısı
 Bir Inline görevi [UsingTask](../msbuild/usingtask-element-msbuild.md) öğesi tarafından içerilir. Satır içi görev ve `UsingTask` bu öğeyi içeren öğe, genellikle bir *. targets* dosyasına dahil edilir ve gereken şekilde diğer proje dosyalarına aktarılır. Temel bir satır içi görev aşağıda verilmiştir. Hiçbir şey yapmediğine dikkat edin.

```xml
<Project ToolsVersion="15.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <!-- This simple inline task does nothing. -->
  <UsingTask
    TaskName="DoNothing"
    TaskFactory="CodeTaskFactory"
    AssemblyFile="$(MSBuildToolsPath)\Microsoft.Build.Tasks.Core.dll" >
    <ParameterGroup />
    <Task>
      <Reference Include="" />
      <Using Namespace="" />
      <Code Type="Fragment" Language="cs">
      </Code>
    </Task>
  </UsingTask>
</Project>
```

 Örnekteki `UsingTask` öğesinde, görevi tanımlayan üç öznitelik ve onu derleyen satır içi görev fabrikası vardır.

- Özniteliği, bu `DoNothing`durumda görevi adlandırır. `TaskName`

- `TaskFactory` Özniteliği, satır içi görev fabrikasını uygulayan sınıfı adlandırır.

- `AssemblyFile` Özniteliği, satır içi görev fabrikasının konumunu verir. Alternatif olarak, genellikle genel derleme `AssemblyName` önbelleğinde (GAC) bulunan satır içi görev fabrikası sınıfının tam adını belirtmek için özniteliğini kullanabilirsiniz.

`DoNothing` Görevin kalan öğeleri boştur ve bir satır içi görevin sırasını ve yapısını göstermek için verilmiştir. Daha sonra bu konunun ilerleyen kısımlarında daha sağlam bir örnek sunulmaktadır.

- `ParameterGroup` Öğesi isteğe bağlıdır. Belirtildiğinde, görevin parametrelerini bildirir. Giriş ve çıkış parametreleri hakkında daha fazla bilgi için bu konunun ilerleyen kısımlarında [giriş ve çıkış parametreleri](#input-and-output-parameters) bölümüne bakın.

- `Task` Öğesi, görev kaynak kodunu tanımlar ve içerir.

- Öğesi `Reference` , kodunuzda kullanmakta olduğunuz .NET derlemelerine başvuruları belirtir. Bu, Visual Studio 'da bir projeye başvuru ekleme ile eşdeğerdir. `Include` Öznitelik, başvurulan derlemenin yolunu belirtir.

- `Using` Öğesi, erişmek istediğiniz ad alanlarını listeler. Bu, `Using` Visual C#'teki ifadeye benzer. `Namespace` Öznitelik, dahil edilecek ad alanını belirtir.

`Reference`ve `Using` öğeleri dilden bağımsız değildir. Satır içi görevler desteklenen .NET CodeDom dillerinin herhangi birine (örneğin, Visual Basic veya görsel C#) yazılabilir.

> [!NOTE]
> `Task` Öğesi tarafından içerilen öğeler, bu durumda kod görev fabrikası olan görev fabrikasına özeldir.

### <a name="code-element"></a>Kod öğesi
 `Task` Öğesi`Code` içinde görünecek Son alt öğe öğesi. Öğesi `Code` , bir görevde derlenmek istediğiniz kodu içerir veya konumlandırır. `Code` Öğesine yerleştirdiğiniz öğe, görevi nasıl yazmak istediğinize bağlıdır.

 `Language` Özniteliği, kodunuzun yazıldığı dili belirtir. Visual Basic `vb` için kabul `cs` edilebilir C#değerler içindir.

 Özniteliği, `Code` öğesinde bulunan kodun türünü belirtir. `Type`

- Değeri `Type` ise `Class`, <xref:Microsoft.Build.Framework.ITask> öğesi arabirimindentüretilenbirsınıfiçinkodiçerir.`Code`

- Değeri `Type` ise `Method`, kod, <xref:Microsoft.Build.Framework.ITask> arabirimin `Execute` yöntemini geçersiz kılmayı tanımlar.

- Değeri `Type` ise `Fragment`, `Execute` kod`return` yöntemin içeriğini tanımlar, ancak imza veya deyimin değil.

Kod genellikle bir `<![CDATA[` işaret `]]>` ve işaret arasında görünür. Kod cdata bölümünde olduğundan, kaçış ayrılmış karakterleri (örneğin, "\<" veya ">") konusunda endişelenmeniz gerekmez.

Alternatif olarak, görevin kodunu içeren `Source` bir dosyanın konumunu `Code` belirtmek için öğesinin özniteliğini kullanabilirsiniz. Kaynak dosyadaki kod, `Type` özniteliği tarafından belirtilen türde olmalıdır. Özniteliği varsa, varsayılan `Type` değeri olur `Class`. `Source` Yoksa, varsayılan değer olur `Fragment`. `Source`

> [!NOTE]
> Kaynak dosyada görev sınıfını tanımlarken, sınıf adı karşılık gelen `TaskName` [UsingTask](../msbuild/usingtask-element-msbuild.md) öğesinin özniteliğiyle kabul etmelidir.

## <a name="helloworld"></a>HelloWorld
 Daha sağlam bir satır içi görev aşağıda verilmiştir. HelloWorld görevinde "Hello, World!" görüntülenir Varsayılan hata günlüğü cihazında, genellikle sistem konsolu veya Visual Studio **çıktı** penceresidir. Örnekteki `Reference` öğesi yalnızca çizim için dahil edilmiştir.

```xml
<Project ToolsVersion="15.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <!-- This simple inline task displays "Hello, world!" -->
  <UsingTask
    TaskName="HelloWorld"
    TaskFactory="CodeTaskFactory"
    AssemblyFile="$(MSBuildToolsPath)\Microsoft.Build.Tasks.Core.dll" >
    <ParameterGroup />
    <Task>
      <Reference Include="System.Xml"/>
      <Using Namespace="System"/>
      <Using Namespace="System.IO"/>
      <Code Type="Fragment" Language="cs">
<![CDATA[
// Display "Hello, world!"
Log.LogError("Hello, world!");
]]>
      </Code>
    </Task>
  </UsingTask>
</Project>
```

 HelloWorld *. targets*adlı bir dosyaya HelloWorld görevini kaydedebilir ve ardından bunu bir projeden aşağıdaki şekilde çağırabilirsiniz.

```xml
<Project ToolsVersion="15.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <Import Project="HelloWorld.targets" />
  <Target Name="Hello">
    <HelloWorld />
  </Target>
</Project>
```

## <a name="input-and-output-parameters"></a>Giriş ve çıkış parametreleri
 Satır içi görev parametreleri bir `ParameterGroup` öğenin alt öğeleridir. Her parametre, kendisini tanımlayan öğenin adını alır. Aşağıdaki kod parametresini `Text`tanımlar.

```xml
<ParameterGroup>
  <Text />
</ParameterGroup>
```

 Parametrelerde bu özniteliklerin bir veya daha fazlası olabilir:

- `Required`, varsayılan `false` olarak bir isteğe bağlı özniteliktir. `true`Daha sonra parametresi zorunludur ve görev çağrılmadan önce bir değer verilmelidir.

- `ParameterType`, varsayılan `System.String` olarak bir isteğe bağlı özniteliktir. System. Convert. ChangeType kullanarak bir öğe ya da bir dizeden dönüştürülebilen bir değer olan herhangi bir tamamen nitelenmiş türe ayarlanabilir. (Başka bir deyişle, bir dış görevden ve bu bilgisayardan geçirilebilecek herhangi bir tür.)

- `Output`, varsayılan `false` olarak bir isteğe bağlı özniteliktir. İse `true`, Execute yönteminden dönmeden önce parametreye bir değer verilmelidir.

Örneğin,

```xml
<ParameterGroup>
  <Expression Required="true" />
  <Files ParameterType="Microsoft.Build.Framework.ITaskItem[]" Required="true" />
  <Tally ParameterType="System.Int32" Output="true" />
</ParameterGroup>
```

Şu üç parametreyi tanımlar:

- `Expression`, System. String türünde gerekli bir giriş parametresidir.

- `Files`gerekli bir öğe listesi giriş parametresidir.

- `Tally`, System. Int32 türünde bir çıkış parametresidir.

`Code` Öğesinde `Type` veya özniteliği`Method`varsa, özellikler her parametre için otomatik olarak oluşturulur. `Fragment` Aksi halde, özellikler, görev kaynak kodunda açıkça bildirilmelidir ve parametre tanımlarıyla tam olarak eşleşmesi gerekir.

## <a name="example"></a>Örnek
 Aşağıdaki satır içi görev, verilen dosyadaki bir belirtecin her oluşumunu verilen değerle değiştirir.

```xml
<Project xmlns='http://schemas.microsoft.com/developer/msbuild/2003' ToolsVersion="15.0">

  <UsingTask TaskName="TokenReplace" TaskFactory="CodeTaskFactory" AssemblyFile="$(MSBuildToolsPath)\Microsoft.Build.Tasks.Core.dll">
    <ParameterGroup>
      <Path ParameterType="System.String" Required="true" />
      <Token ParameterType="System.String" Required="true" />
      <Replacement ParameterType="System.String" Required="true" />
    </ParameterGroup>
    <Task>
      <Code Type="Fragment" Language="cs"><![CDATA[
string content = File.ReadAllText(Path);
content = content.Replace(Token, Replacement);
File.WriteAllText(Path, content);

]]></Code>
    </Task>
  </UsingTask>

  <Target Name='Demo' >
    <TokenReplace Path="C:\Project\Target.config" Token="$MyToken$" Replacement="MyValue"/>
  </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.
- [Görevler](../msbuild/msbuild-tasks.md)
- [İzlenecek yol: Satır içi görev oluşturma](../msbuild/walkthrough-creating-an-inline-task.md)
