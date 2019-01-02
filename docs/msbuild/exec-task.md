---
title: Yürütme görevi | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- http://schemas.microsoft.com/developer/msbuild/2003#Exec
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- Exec task [MSBuild]
- MSBuild, Exec task
ms.assetid: c9b7525a-b1c9-40fc-8bce-77a5b8f960d8
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 6fd259f00fdb5af2e3125782bda28c17858eff80
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53959254"
---
# <a name="exec-task"></a>Yürütme görevi
Belirtilen program veya komut belirtilen bağımsız değişkenler kullanılarak çalıştırır.  
  
## <a name="parameters"></a>Parametreler  
 Parametreler için aşağıdaki tabloda açıklanmıştır `Exec` görev.  
  
|Parametre|Açıklama|  
|---------------|-----------------|  
|`Command`|Gerekli `String` parametresi.<br /><br /> Çalıştırılacak komut. Bunlar gibi attrib veya yürütülebilir bir dosya gibi sistem komutlarını olabilir *program.exe*, *runprogram.bat*, veya *setup.msi*.<br /><br /> Bu parametre, komutları birden fazla satır içerebilir. Alternatif olarak, bir toplu iş dosyasında birden çok komut yerleştirin ve bu parametre kullanarak çalıştırabilirsiniz.|  
|`ConsoleOutput`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Her öğesi çıktısı, aracı tarafından standart çıktı veya standart hata akışı'ndan bir satırdır. Bu, yalnızca yakalanır `ConsoleToMsBuild` ayarlanır `true`.|
|`ConsoleToMsBuild`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, görevin standart hatayı yakalar ve standart çıkış aracı ve bunları kullanılabilir duruma `ConsoleOutput` çıkış parametresi.<br /><br />Varsayılan: `false`.|  
|`CustomErrorRegularExpression`|İsteğe bağlı `String` parametresi.<br /><br /> Araç çıktısı nokta hatası satırlarda kullanılacak normal bir ifade belirtir. Bu, olağan dışı derecede biçimlendirilmiş çıktı oluşturmak için Araçlar kullanışlıdır.<br /><br />Varsayılan: `null` (hiçbir özel işlem).|  
|`CustomWarningRegularExpression`|İsteğe bağlı `String` parametresi.<br /><br /> Araç çıktısı nokta uyarı satırları için kullanılan normal bir ifade belirtir. Bu, olağan dışı derecede biçimlendirilmiş çıktı oluşturmak için Araçlar kullanışlıdır.<br /><br />Varsayılan: `null` (hiçbir özel işlem).|  
|`EchoOff`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, görev genişletilmiş biçiminin yayma değil `Command` MSBuild günlüğü.<br /><br />Varsayılan: `false`.|
|`ExitCode`|İsteğe bağlı `Int32` çıkış parametresi salt okunur.<br /><br /> Yürütülen komutun tarafından sağlanan çıkış kodu belirtir.|  
|`IgnoreExitCode`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `true`, görev tarafından yürütülen komutun sağlanan çıkış kodu yoksayar. Aksi halde, bir görev döndürür `false` Yürütülen komutun bir sıfır olmayan çıkış kodu döndürmesi durumunda.<br /><br />Varsayılan: `false`.|  
|`IgnoreStandardErrorWarningFormat`|İsteğe bağlı `Boolean` parametresi.<br /><br /> Varsa `false`, standart hata/uyarı biçim ile eşleşmesi çıktısında satırları seçer ve bunları hataları/uyarıları günlüğe kaydeder. Varsa `true`, bu davranışı devre dışı.<br /><br />Varsayılan: `false`.|  
|`Outputs`|İsteğe bağlı <xref:Microsoft.Build.Framework.ITaskItem> `[]` çıkış parametresi.<br /><br /> Görev çıktısı öğeleri içerir. `Exec` Görev bu kendisini ayarlamaz. Bunları ayarlamak gibi böylece daha sonra projede kullanılan bunun yerine, bunları sağlayabilirsiniz.|  
|`StdErrEncoding`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Yakalanan görev standart hata akışı kodlamasını belirtir. Geçerli varsayılandır konsol çıktı kodlaması.|  
|`StdOutEncoding`|İsteğe bağlı `String` çıkış parametresi.<br /><br /> Yakalanan görev standart çıkış akışına kodlamasını belirtir. Geçerli varsayılandır konsol çıktı kodlaması.|  
|`WorkingDirectory`|İsteğe bağlı `String` parametresi.<br /><br /> Komutun yürütüleceği dizini belirtir.<br /><br />Varsayılan: Projenin geçerli çalışma dizini.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu görevi, belirli bir zaman yararlı [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] gerçekleştirmek istediğiniz işlemi kullanılabilir değil görev. Ancak, `Exec` ek işleme veya aracı veya çalıştığı komut sonucuna göre koşullu işlemlerden daha belirli bir görevin farklı olarak görev yapamaz.
  
 `Exec` Görev çağrıları *cmd.exe* yerine doğrudan bir işlemi çağırma.  
  
 Bu belgede listelenen parametrelerin yanı sıra, bu görev parametreleri devralan <xref:Microsoft.Build.Tasks.ToolTaskExtension> kendisi sınıfının devraldığı <xref:Microsoft.Build.Utilities.ToolTask> sınıfı. Bu ek parametrelerin ve Tanımlamaların bir listesi için bkz. [ToolTaskExtension taban sınıfı](../msbuild/tooltaskextension-base-class.md).  
  
## <a name="example"></a>Örnek  
 Aşağıdaki örnekte `Exec` bir komutu çalıştırmak için görev.  
  
```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemGroup>  
        <Binaries Include="*.dll;*.exe"/>  
    </ItemGroup>  
  
    <Target Name="SetACL">  
        <!-- set security on binaries-->  
        <Exec Command="echo y| cacls %(Binaries.Identity) /G everyone:R"/>  
    </Target>  
</Project>  
```

## <a name="see-also"></a>Ayrıca bkz.  
 [Görevleri](../msbuild/msbuild-tasks.md)   
 [Görev başvurusu](../msbuild/msbuild-task-reference.md)
