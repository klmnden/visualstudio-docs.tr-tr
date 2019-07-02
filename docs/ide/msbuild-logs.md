---
title: Sorun giderme ve MSBuild sorunlar için günlükleri oluşturma
ms.date: 06/27/2019
ms.topic: conceptual
helpviewer_keywords:
- msbuild logs"
author: mikeblome
ms.author: mblome
manager: jillfra
dev_langs:
- CSharp
- VB
- CPP
ms.workload:
- multiple
ms.description: Generate build logs for msbuild projects to collect helpful information when troubleshooting issues.
ms.openlocfilehash: c3db56ac7ea60ce88beae6698c974ac91373ed00
ms.sourcegitcommit: 6f7a740750b2cd17ea2275c3d046caebc9782917
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67518240"
---
# <a name="troubleshoot-and-create-logs-for-msbuild-problems"></a>Sorun giderme ve MSBuild sorunlar için günlükleri oluşturma

Aşağıdaki yordamlar Visual Studio projenize yapı sorunlarını tanılama ve gerekirse, araştırma için Microsoft'a göndermek için bir günlük oluşturmanıza yardımcı olabilir.

## <a name="a-property-value-is-ignored"></a>Bir özellik değeri yok sayıldı

Proje özelliği için belirli bir değere ayarlanması gibi görünüyor, ancak derleme üzerinde hiçbir etkisi, şu adımları izleyin:

1. Visual Studio Geliştirici komut Visual Studio sürümünüze karşılık gelen istemi açın.
1. Çözüm yolu, yapılandırma ve proje adı için değerleri değiştirerek sonra aşağıdaki komutu çalıştırın:

    ```cmd
    msbuild /p:SolutionDir="c:\MySolutionDir\";Configuration="MyConfiguration";Platform="Win32" /pp:out.xml MyProject.vcxproj
    ```

    Bu komut, "önceden işlenmiş" msbuild proje dosyası (out.xml) üretir. Bu dosya tanımlandığı görmek belirli bir özellik için arama yapabilirsiniz.

Son bir özelliğin hangi derleme tüketir tanımıdır. İki kez özelliği ayarlanmışsa, ikinci değer ilk üzerine yazar. Ayrıca, çeşitli geçiş projede MSBuild değerlendirir:

- PropertyGroups ve içeri aktarmalar
- ItemDefinitionGroups
- Itemgroups'un
- Hedefler

Bu nedenle, aşağıdaki sırayla verilen:

```xml
<PropertyGroup>
   <MyProperty>A</MyProperty>
</PropertyGroup>
<ItemGroup>
   <MyItems Include="MyFile.txt"/>
</ItemGroup>
<ItemDefinitionGroup>
  <MyItems>
      <MyMetadata>$(MyProperty)</MyMetadata>
  </MyItems>
</ItemDefinitionGroup>
<PropertyGroup>
   <MyProperty>B</MyProperty>
</PropertyGroup>
```

"MyMetadata" değerini "Dosya.txt" öğesi için derleme sırasında "B" olarak değerlendirilir (değil "A" ve boş olmayan)

## <a name="incremental-build-is-building-more-than-it-should"></a>Artımlı derleme, gerekenden daha fazla oluşturuyor

MSBuild gereksiz bir proje veya proje öğesini yeniden ayrıntılı ya da ikili derleme günlüğü oluşturun. Yerleşik veya gereksiz yere derlenmiş olan dosya için günlük arama yapabilirsiniz. Çıktı aşağıdakine benzer olacaktır:

```output
  Task "CL"

  Using cached input dependency table built from:

  F:\test\Project1\Project1\Debug\Project1.tlog\CL.read.1.tlog

  Outputs for F:\TEST\PROJECT1\PROJECT1\PROJECT1.CPP:
  F:\TEST\PROJECT1\PROJECT1\DEBUG\PROJECT1.OBJ
  Project1.cpp will be compiled because F:\TEST\PROJECT1\PROJECT1\PROJECT1.H was modified at 6/5/2019 12:37:09 PM.

  Outputs for F:\TEST\PROJECT1\PROJECT1\PROJECT1.CPP:
  F:\TEST\PROJECT1\PROJECT1\DEBUG\PROJECT1.OBJ

  Write Tracking Logs:
  Debug\Project1.tlog\CL.write.1.tlog
```

(İle ayrıntılı çıkış pencere ayrıntı), Visual Studio IDE içinde oluşturuyorsanız **çıkış penceresine** neden her proje güncel değil neden görüntüler:

```output
1>------ Up-To-Date check: Project: Project1, Configuration: Debug Win32 ------

1>Project is not up-to-date: build input 'f:\test\project1\project1\project1.h' was modified after the last build finished.
```

## <a name="create-a-binary-msbuild-log"></a>İkili msbuild günlük oluşturmak

1. Visual Studio sürümünüz için geliştirici komut istemi açın
1. Komut isteminde aşağıdaki komutlardan birini çalıştırın. (Proje ve yapılandırma değerleri kullanmayı unutmayın.):

    ```cmd
    Msbuild /p:Configuration="MyConfiguration";Platform="x86" /bl MySolution.sln
    ```

    veya

    ```cmd
    Msbuild /p:/p:SolutionDir="c:\MySolutionDir\";Configuration="MyConfiguration";Platform="Win32" /bl MyProject.vcxproj
    ```

Msbuild.binlog dosya, MSBuild'den çalıştırdığınız dizinde oluşturulur. Görüntüleyebilir ve kullanarak arama [Msbuild yapılandırılmış Günlük Görüntüleyici](http://www.msbuildlog.com/).

## <a name="create-a-detailed-log"></a>Ayrıntılı günlük oluşturma

1. Visual Studio ana menüden Git **Araçları** > **seçenekleri** > **projeler ve çözümler** >**oluşturun çalıştırıp**.
1. Ayarlama **Msbuild proje derlemesi ayrıntı** için **ayrıntılı** hem birleşik giriş kutularında. Ayrıntı düzeyi bir üst denetimlerin yapı içinde **çıkış penceresine** ve ikincisi denetimleri içinde derleme ayrıntısı \<projectname\>Ara dizindeki, her projenin sırasında oluşturulan .log dosyası oluşturun.
1. Visual Studio Geliştirici komut isteminden yolu ve yapılandırma değerleri değiştirerek, bu komutlardan birini girin:

    ```cmd
    Msbuild /p:Configuration="MyConfiguration";Platform="x86" /fl MySolution.sln 
    ```

    veya

    ```cmd
    Msbuild /p:/p:SolutionDir="c:\MySolutionDir\";Configuration="MyConfiguration";Platform="Win32" /fl MyProject.vcxproj
    ```

    Bir Msbuild.log dosya MSBuild'den çalıştırdığınız dizinde oluşturulur.
