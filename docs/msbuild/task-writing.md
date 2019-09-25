---
title: Görev yazma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, writing tasks
- tasks, creating for MSBuild
- MSBuild, creating tasks
ms.assetid: 3ebc5f87-8f00-46fc-82a1-228f35a6823b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 9cf7f82d628c0c093e0d807920b379263c20ff0b
ms.sourcegitcommit: 0c2523d975d48926dd2b35bcd2d32a8ae14c06d8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "71238190"
---
# <a name="task-writing"></a>Görev yazma
Görevler, derleme işlemi sırasında çalışan kodu sağlar. Görevler, hedefler ' de yer alır. Tipik görevlerin bir kitaplığı ile [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]birlikte dahildir ve ayrıca kendi görevlerinizi de oluşturabilirsiniz. İçinde yer [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]alan görevlerin Kitaplığı hakkında daha fazla bilgi için bkz. [görev başvurusu](../msbuild/msbuild-task-reference.md).

## <a name="tasks"></a>Görevler
 Görev örnekleri, bir veya daha fazla dosyayı kopyalayan, bir dizin oluşturan [MakeDir](../msbuild/makedir-task.md)ve kaynak kodu dosyalarını derleyen [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] [CSC](../msbuild/csc-task.md) ['yi içerir.](../msbuild/copy-task.md) Her görev, *Microsoft. Build. Framework. dll* derlemesinde <xref:Microsoft.Build.Framework.ITask> tanımlanan arabirimi uygulayan bir .NET sınıfı olarak uygulanır.

 Bir görevi uygularken kullanabileceğiniz iki yaklaşım vardır:

- <xref:Microsoft.Build.Framework.ITask> Arabirimi doğrudan uygulayın.

- *Microsoft. Build. Utilities. dll* derlemesinde <xref:Microsoft.Build.Utilities.Task>tanımlanan yardımcı sınıfından sınıfınızı türetirsiniz. Görev ITask 'ı uygular ve bazı ITask üyelerinin varsayılan uygulamalarını sağlar. Ayrıca günlüğe kaydetme daha kolay.

Her iki durumda da, görev çalıştırıldığında çağrılan yöntemi olan adlı `Execute`bir yöntemi sınıfınıza eklemeniz gerekir. Bu yöntem hiçbir parametre alır ve bir `Boolean` değer döndürür: `true` görev başarılı olursa veya `false` başarısız olursa. Aşağıdaki örnek, hiçbir eylem ve dönüş `true`gerçekleştirmeyen bir görevi gösterir.

```csharp
using System;
using Microsoft.Build.Framework;
using Microsoft.Build.Utilities;

namespace MyTasks
{
    public class SimpleTask : Task
    {
        public override bool Execute()
        {
            return true;
        }
    }
}
```

 Şu proje dosyası bu görevi çalıştırır:

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <Target Name="MyTarget">
        <SimpleTask />
    </Target>
</Project>
```

 Görevler çalıştırıldığında, görev sınıfında .NET özellikleri oluşturursanız proje dosyasından de giriş alabilir. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]görevin `Execute` metodunu çağırmadan önce bu özellikleri hemen ayarlar. Bir dize özelliği oluşturmak için, şöyle bir görev kodu kullanın:

```csharp
using System;
using Microsoft.Build.Framework;
using Microsoft.Build.Utilities;

namespace MyTasks
{
    public class SimpleTask : Task
    {
        public override bool Execute()
        {
            return true;
        }

        public string MyProperty { get; set; }
    }
}
```

 Aşağıdaki proje dosyası bu görevi çalıştırır ve belirtilen değere `MyProperty` ayarlar:

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
   <Target Name="MyTarget">
      <SimpleTask MyProperty="Value for MyProperty" />
   </Target>
</Project>
```

## <a name="register-tasks"></a>Görevleri Kaydet
 Bir proje bir görevi çalıştıracaksanız, [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] görev sınıfını içeren derlemeyi bulmayı bilmelidir. Görevler [UsingTask öğesi (MSBuild)](../msbuild/usingtask-element-msbuild.md)kullanılarak kaydedilir.

 Microsoft. *Common. Tasks* `UsingTask` [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]dosyası, ile sağlanan tüm görevleri kaydeden öğelerin listesini içeren bir proje dosyasıdır. [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Bu dosya, her proje oluşturulurken otomatik olarak eklenir. *Microsoft. Common. Tasks* ' de kayıtlı bir görev aynı zamanda geçerli proje dosyasında kayıtlıysa, geçerli proje dosyası önceliklidir; diğer bir deyişle, aynı ada sahip olan kendi görevinizdeki varsayılan görevi geçersiz kılabilirsiniz.

> [!TIP]
> [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] *Microsoft. Common. görevlerinin*içeriğini görüntüleyerek, ile sağlanan görevlerin bir listesini görebilirsiniz.

## <a name="raise-events-from-a-task"></a>Bir görevden olay oluştur
 Göreviniz <xref:Microsoft.Build.Utilities.Task> yardımcı sınıftan türetilirse, tüm kayıtlı Günlükçüler tarafından yakalanıp görüntülenecek olayları yükseltmek için <xref:Microsoft.Build.Utilities.Task> sınıfında aşağıdaki yardımcı yöntemlerden herhangi birini kullanabilirsiniz:

```csharp
public override bool Execute()
{
    Log.LogError("messageResource1", "1", "2", "3");
    Log.LogWarning("messageResource2");
    Log.LogMessage(MessageImportance.High, "messageResource3");
    ...
}
```

 Göreviniz doğrudan uygularsa <xref:Microsoft.Build.Framework.ITask> bu tür olayları yine de oluşturabilirsiniz, ancak IBuildEngine arabirimini kullanmanız gerekir. Aşağıdaki örnek, ITask uygulayan ve özel bir olay başlatan bir görevi gösterir:

```csharp
public class SimpleTask : ITask
{
    public IBuildEngine BuildEngine { get; set; }

    public override bool Execute()
    {
        TaskEventArgs taskEvent =
            new TaskEventArgs(BuildEventCategory.Custom,
            BuildEventImportance.High, "Important Message",
           "SimpleTask");
        BuildEngine.LogBuildEvent(taskEvent);
        return true;
    }
}
```

## <a name="require-task-parameters-to-be-set"></a>Görev parametrelerinin ayarlanması gerekiyor
 Belirli görev özelliklerini "gerekli" olarak işaretleyebilirsiniz. böylece, görevi çalıştıran herhangi bir proje dosyasının bu özelliklerin değerlerini ayarlaması gerekir, aksi durumda derleme başarısız olur. Aşağıdaki gibi `[Required]` , görev içindeki .net özelliğine özniteliğini uygulayın:

```csharp
[Required]
public string RequiredProperty { get; set; }
```

 Özniteliği, <xref:Microsoft.Build.Framework> ad alanında tarafından <xref:Microsoft.Build.Framework.RequiredAttribute> tanımlanır. `[Required]`

## <a name="how-includevstecmsbuildextensibilityinternalsincludesvstecmsbuild_mdmd-invokes-a-task"></a>Bir [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] görevi nasıl çağırır

Bir görevi [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] çağırırken, önce görev sınıfını örnekleyerek, sonra proje dosyasındaki görev öğesinde ayarlanan görev parametreleri için o nesnenin özellik ayarlayıcıları ' nı çağırır. Görev öğesi bir parametre belirtmezse veya öğede belirtilen ifade boş bir dize olarak değerlendirilirse, Özellik ayarlayıcısı çağrılmaz.

Örneğin, projede

```xml
<Project>
 <Target Name="InvokeCustomTask">
  <CustomTask Input1=""
              Input2="$(PropertyThatIsNotDefined)"
              Input3="value3" />
 </Target>
</Project>
```

yalnızca için `Input3` ayarlayıcı çağırılır.

Bir görev, parametre özelliği ayarlayıcısı çağrısının herhangi bir göreli sırasına bağlı olmamalıdır.

### <a name="task-parameter-types"></a>Görev parametresi türleri

`string` ,,`bool`Ve türündeki`ITaskItem[]`özellikleri [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)]yerelolarakişler `ITaskItem` . Bir görev farklı türde bir parametreyi kabul ediyorsa, [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] dönüştürme `string` için çağırır <xref:System.Convert.ChangeType%2A> (tüm özellik ve öğe başvuruları ile) hedef türüne. Herhangi bir giriş parametresi için dönüştürme başarısız olursa, [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] bir hata yayar ve `Execute()` görevin metodunu çağırmaz.

## <a name="example"></a>Örnek

### <a name="description"></a>Açıklama

Aşağıdaki [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] sınıf, <xref:Microsoft.Build.Utilities.Task> yardımcı sınıfından türetilen bir görevi gösterir. Bu görev, `true`başarılı olduğunu belirten döndürür.

### <a name="code"></a>Kod

```csharp
using System;
using Microsoft.Build.Utilities;

namespace SimpleTask1
{
    public class SimpleTask1: Task
    {
        public override bool Execute()
        {
            // This is where the task would presumably do its work.
            return true;
        }
    }
}
```

## <a name="example"></a>Örnek

### <a name="description"></a>Açıklama

Aşağıdaki [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] sınıf, <xref:Microsoft.Build.Framework.ITask> arabirimini uygulayan bir görevi gösterir. Bu görev, `true`başarılı olduğunu belirten döndürür.

### <a name="code"></a>Kod

```csharp
using System;
using Microsoft.Build.Framework;

namespace SimpleTask2
{
    public class SimpleTask2: ITask
    {
        //When implementing the ITask interface, it is necessary to
        //implement a BuildEngine property of type
        //Microsoft.Build.Framework.IBuildEngine. This is done for
        //you if you derive from the Task class.
        public IBuildEngine BuildEngine { get; set; }

        // When implementing the ITask interface, it is necessary to
        // implement a HostObject property of type object.
        // This is done for you if you derive from the Task class.
        public object HostObject { get; set; }

        public bool Execute()
        {
            // This is where the task would presumably do its work.
            return true;
        }
    }
}
```

## <a name="example"></a>Örnek

### <a name="description"></a>Açıklama

Bu [!INCLUDE[csprcs](../data-tools/includes/csprcs_md.md)] sınıf, <xref:Microsoft.Build.Utilities.Task> yardımcı sınıfından türetilen bir görevi gösterir. Gerekli bir dize özelliğine sahiptir ve tüm kayıtlı Günlükçüler tarafından görüntülenen bir olay oluşturur.

### <a name="code"></a>Kod

[!code-csharp[msbuild_SimpleTask3#1](../msbuild/codesnippet/CSharp/task-writing_1.cs)]

## <a name="example"></a>Örnek

### <a name="description"></a>Açıklama

Aşağıdaki örnek, SimpleTask3 önceki örnek görevi çağıran bir proje dosyası gösterir.

### <a name="code"></a>Kod

```xml
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
    <UsingTask TaskName="SimpleTask3.SimpleTask3"
        AssemblyFile="SimpleTask3\bin\debug\simpletask3.dll"/>

    <Target Name="MyTarget">
        <SimpleTask3 MyProperty="Hello!"/>
    </Target>
</Project>
```

## <a name="see-also"></a>Ayrıca bkz.

- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
