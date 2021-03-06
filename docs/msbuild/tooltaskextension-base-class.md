---
title: ToolTaskExtension temel sınıfı | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
ms.assetid: 258ae433-f68a-49f1-b276-da20e3472e68
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7734f852da997836cf2f42fd3f6b96e9decdf8dd
ms.sourcegitcommit: 628eb202a1153ebfe69c668f966f821b98b34b34
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/02/2019
ms.locfileid: "71720564"
---
# <a name="tooltaskextension-base-class"></a>ToolTaskExtension temel sınıfı
Birçok görev, kendisini <xref:Microsoft.Build.Utilities.Task> sınıfından devralan <xref:Microsoft.Build.Utilities.ToolTask> sınıfından devralan <xref:Microsoft.Build.Tasks.ToolTaskExtension> sınıfından devralınır. Bu devralma zinciri, bunlardan türetilen görevlere birkaç parametre ekler. Bu parametreler bu belgede listelenmiştir.

## <a name="parameters"></a>Parametreler
 Aşağıdaki tabloda temel sınıfların parametreleri açıklanmaktadır.

| Parametre | Açıklama |
| - | - |
| <xref:Microsoft.Build.Utilities.Task.BuildEngine%2A> | İsteğe <xref:Microsoft.Build.Framework.IBuildEngine> bağlı parametre.<br /><br /> Görevler için kullanılabilen derleme altyapısı arabirimini belirtir. Yapı altyapısı bu parametreyi otomatik olarak ayarlar ve görevlere geri çağrı yapmasına izin verir. |
| <xref:Microsoft.Build.Utilities.Task.BuildEngine2%2A> | İsteğe <xref:Microsoft.Build.Framework.IBuildEngine2> bağlı parametre.<br /><br /> Görevler için kullanılabilen derleme altyapısı arabirimini belirtir. Yapı altyapısı bu parametreyi otomatik olarak ayarlar ve görevlere geri çağrı yapmasına izin verir.<br /><br /> Bu bir kullanışlı özelliktir. bu sınıftan devralan görev yazarlarının değeri `IBuildEngine` ' dan `IBuildEngine2` ' e dönüştürmek zorunda değildir. |
| <xref:Microsoft.Build.Utilities.Task.BuildEngine3%2A> | İsteğe <xref:Microsoft.Build.Framework.IBuildEngine3> bağlı parametre.<br /><br /> Konak tarafından belirtilen derleme altyapısı arabirimini belirtir. |
| <xref:Microsoft.Build.Utilities.ToolTask.EchoOff%2A> | İsteğe `bool` bağlı parametre.<br /><br /> @No__t-0 olarak ayarlandığında, bu görev **/q** komutunu komut satırı stdout 'a kopyalanmaması gibi *cmd. exe* komut satırına geçirir. |
| <xref:Microsoft.Build.Utilities.ToolTask.EnvironmentVariables%2A> | İsteğe bağlı `String` dizi parametresi.<br /><br /> Ortam değişkenlerinin çiftler dizisi, eşittir işaretleriyle ayrılmıştır. Bu değişkenler, normal ortam bloğunu seçerek veya seçmeli olarak geçersiz kılmanın yanı sıra oluşturulan yürütülebilir dosyaya geçirilir. |
| <xref:Microsoft.Build.Utilities.ToolTask.ExitCode%2A> | İsteğe bağlı `Int32` çıkış salt okunurdur parametresi.<br /><br /> Yürütülen komut tarafından belirtilen çıkış kodunu belirtir. Görev herhangi bir hata günlüğe açtıysa, ancak işlem 0 (başarılı) çıkış koduna sahipse bu,-1 ' e ayarlanır. |
| <xref:Microsoft.Build.Utilities.Task.HostObject%2A> | İsteğe <xref:Microsoft.Build.Framework.ITaskHost> bağlı parametre.<br /><br /> Ana bilgisayar nesne örneğini belirtir (null olabilir). Konak IDE, bu görevle bir ana bilgisayar nesnesi ilişkilendirirse, derleme altyapısı bu özelliği ayarlar. |
| <xref:Microsoft.Build.Tasks.ToolTaskExtension.Log%2A> | İsteğe bağlı <xref:Microsoft.Build.Utilities.TaskLoggingHelper> salt okunurdur parametresi.<br /><br /> Görev günlüğü yöntemlerini içeren <xref:Microsoft.Build.Tasks.TaskLoggingHelperExtension> sınıfının bir örneğini alır. |
| <xref:Microsoft.Build.Utilities.ToolTask.LogStandardErrorAsError%2A> | Seçenek `bool` parametresi.<br /><br /> @No__t-0 ise, standart hata akışında alınan tüm iletiler hata olarak günlüğe kaydedilir. |
| <xref:Microsoft.Build.Utilities.ToolTask.StandardErrorImportance%2A> | İsteğe `String` bağlı parametre.<br /><br /> Standart çıkış akışından metnin günlüğe kaydedileceği önem. |
| <xref:Microsoft.Build.Utilities.ToolTask.StandardOutputImportance%2A> | İsteğe `String` bağlı parametre.<br /><br /> Standart çıkış akışından metnin günlüğe kaydedileceği önem. |
| <xref:Microsoft.Build.Utilities.ToolTask.Timeout%2A> | Sanal isteğe bağlı `Int32` parametresi.<br /><br /> Görev yürütülebilir dosyasının sonlandırılacağı süre (milisaniye cinsinden) sayısını belirtir. Varsayılan değer `Int.MaxValue`, zaman aşımı süresi olmadığını gösterir. Zaman aşımı süresi milisaniyedir. |
| <xref:Microsoft.Build.Utilities.ToolTask.ToolExe%2A> | Sanal isteğe bağlı `string` parametresi.<br /><br /> Projeler, bir ToolName 'yi geçersiz kılmak için bunu uygulayabilir. Görevler, ToolName 'yi korumak için bunu geçersiz kılabilir. |
| <xref:Microsoft.Build.Utilities.ToolTask.ToolPath%2A> | İsteğe `string` bağlı parametre.<br /><br /> Görevin temel alınan yürütülebilir dosyayı yüklediği konumu belirtir. Bu parametre belirtilmezse, görev [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] çalıştıran Framework sürümüne karşılık gelen SDK yükleme yolunu kullanır. |
| <xref:Microsoft.Build.Utilities.ToolTask.UseCommandProcessor%2A> | İsteğe `bool` bağlı parametre.<br /><br /> @No__t-0 olarak ayarlandığında, bu görev komut satırı için bir toplu iş dosyası oluşturur ve komutu doğrudan yürütmek yerine komut işlemcisini kullanarak yürütür. |
| <xref:Microsoft.Build.Utilities.ToolTask.YieldDuringToolExecution%2A> | İsteğe `bool` bağlı parametre.<br /><br /> @No__t-0 olarak ayarlandığında, bu görev, görevi çalıştırıldığında düğümü verir. |

## <a name="see-also"></a>Ayrıca bkz.
- [Görev başvurusu](../msbuild/msbuild-task-reference.md)
- [Görevler](../msbuild/msbuild-tasks.md)