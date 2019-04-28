---
title: MSBuild ile paralel olarak birden çok proje oluşturma | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- parallel project builds
- building multiple projects in parallel
- msbuild, building projects in parallel
ms.assetid: c8c9aadc-33ad-4aa1-b07d-b879e9eabda0
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 4de5eebdf9c1f4f66d26b29d194b57172e9af3be
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63426990"
---
# <a name="building-multiple-projects-in-parallel-with-msbuild"></a>MSBuild ile Paralel Olarak Birden Çok Proje Derleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Paralel çalıştırarak daha hızlı olan birden çok projeleri derlemek için MSBuild'ı kullanabilirsiniz. Derlemeleri paralel olarak çalıştırmak için çok çekirdekli veya birden çok işlemci bilgisayarda aşağıdaki ayarları kullanın:  
  
- `/maxcpucount` Geçiş komut isteminde.  
  
- <xref:Microsoft.Build.Tasks.MSBuild.BuildInParallel%2A> Bir MSBuild görevi görev parametresi.  
  
> [!NOTE]
> **/Verbosity** (**/v**) bir komut satırı anahtarı da yapı performansını etkiler. Derleme günlüğü bilgilerinizin ayrıntı ayrıntılı kümesi veya sorun giderme için kullanılan tanılama ise, derleme performansı düşebilir. Daha fazla bilgi için [derleme günlükleri alma](../msbuild/obtaining-build-logs-with-msbuild.md) ve [komut satırı başvurusu](../msbuild/msbuild-command-line-reference.md).  
  
## <a name="maxcpucount-switch"></a>/maxcpucount Anahtarı  
 Kullanırsanız `/maxcpucount` geçiş, veya `/m` kısa için paralel olarak çalıştırılabilecek MSBuild.exe sayısı belirtilen MSBuild oluşturabilirsiniz. Bu işlemler "çalışan işlemleri" olarak da bilinen olan Diğer kullanılabilir işlemci diğer projeler oluşturmak olarak aynı anda bir proje oluşturmak kullanılabilir olduğunda her çalışan işlemi ayrı bir çekirdek veya işlemci kullanır. Örneğin, "4" değeri için bu anahtarı ayarı, projeyi derlemek için dört çalışan işlemler oluşturmak MSBuild neden olur.  
  
 Eklerseniz `/maxcpucount` MSBuild bir değer belirtmeden anahtar için kullanacağı bilgisayarın işlemci sayısı.  
  
 MSBuild 3. 5'kullanıma sunulan bu anahtar hakkında daha fazla bilgi için bkz. [komut satırı başvurusu](../msbuild/msbuild-command-line-reference.md).  
  
 Aşağıdaki örnek, üç alt işlemlerin kullanılacak MSBuild bildirir. Bu yapılandırmayı kullanıyorsanız, MSBuild aynı anda üç projeleri oluşturabilirsiniz.  
  
```  
msbuild.exe myproj.proj /maxcpucount:3  
```  
  
## <a name="buildinparallel-task-parameter"></a>BuildInParallel Görev Parametresi  
 `BuildInParallel` İsteğe bağlı bir boolean parametre açıktır bir [!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] görev. Zaman `BuildInParallel` ayarlanır `true` (varsayılan değeri) aynı anda mümkün olduğunca çok projeleri derlemek için birden çok çalışan işlemi oluşturulur. Bunun düzgün çalışması `/maxcpucount` anahtar ayarlanmalıdır bir değer 1'den büyük ve sistemin en az çift çekirdekli veya iki veya daha fazla işlemciye sahip olmanız gerekir.  
  
 Aşağıdaki örnek, Microsoft.common.targets'ı, nasıl ayarlanacağı konusunda alınan olan `BuildInParallel` parametresi.  
  
```  
<PropertyGroup>  
    <BuildInParallel Condition="'$(BuildInParallel)' ==   
        ''">true</BuildInParallel>  
</PropertyGroup>  
<MSBuild  
    Projects="@(_MSBuildProjectReferenceExistent)"  
    Targets="GetTargetPath"  
    BuildInParallel="$(BuildInParallel)"  
    Properties="%(_MSBuildProjectReferenceExistent.SetConfiguration);   
        %(_MSBuildProjectReferenceExistent.SetPlatform)"  
    Condition="'@(NonVCProjectReference)'!='' and   
        ('$(BuildingSolutionFile)' == 'true' or   
        '$(BuildingInsideVisualStudio)' == 'true' or   
        '$(BuildProjectReferences)' != 'true') and     
        '@(_MSBuildProjectReferenceExistent)' != ''"  
    ContinueOnError="!$(BuildingProject)">  
    <Output TaskParameter="TargetOutputs"   
        ItemName="_ResolvedProjectReferencePaths"/>  
</MSBuild>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Projeleri derlemek için birden çok işlemci kullanma](../msbuild/using-multiple-processors-to-build-projects.md)   
 [Birden çok işlemciye duyarlı Günlükçüler yazılıyor](../msbuild/writing-multi-processor-aware-loggers.md)   
 [C++ yapı paralellik blog ayarlama](http://go.microsoft.com/fwlink/?LinkId=251457)
