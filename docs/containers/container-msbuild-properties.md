---
title: Visual Studio kapsayıcı araçları derleme özellikleri
author: ghogen
description: Kapsayıcı Araçları yapı işlemine genel bakış
ms.author: ghogen
ms.date: 06/06/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: e3ce803f13b8dde82ffe71906e5f7a43a029dbb6
ms.sourcegitcommit: 0cd282a7584b9bfd4df7882f8fdf3ad8a270e219
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67467415"
---
# <a name="container-tools-build-properties"></a>Kapsayıcı Araçları derleme özellikleri

Visual Studio projenizi derlemek için MSBuild'ı kullanan özelliklerini ayarlayarak kapsayıcı projelerinizi nasıl derler özelleştirebilirsiniz. Dockerfile adını değiştirmek, etiketleri ve etiketler için kendi görüntülerinizi sağlayan ek bağımsız değişkenleri belirtin. Örneğin, Visual Studio dışında yapı gibi bazı performans iyileştirmelerini mu yoksa Docker komutlar ve Denetim başarılı kapsayıcı ortamı. Sağlamak için hata ayıklama başlatma ve komut satırı bağımsız değişkenleri yürütülebilir dosyaya adı gibi özellikleri de ayarlayabilirsiniz.

Bir özelliğin değerini ayarlamak için proje dosyasını düzenleyin. Örneğin, Dockerfile adlı varsayalım *MyDockerfile*. Ayarlayabileceğiniz `DockerfileFile` projesi özelliğinde dosya gibi.

```xml
<PropertyGroup>
   <DockerfileFile>MyDockerfile</DockerfileFile>
</PropertyGroup>
```

Varolan bir özellik ayarı ekleyebilirsiniz `PropertyGroup` öğesi veya yoksa, yeni bir oluşturma `PropertyGroup` öğesi.

Aşağıdaki tabloda kullanılabilir kapsayıcı projeleri için MSBuild özelliklerini gösterir.

| Özellik adı | Açıklama | Varsayılan değer  |
|---------------|-------------|----------------|
| DockerfileFile | Varsayılan derleme / proje için kapsayıcı çalıştırma için kullanılan Dockerfile açıklar. Bu işlem de bir yol olabilir. | Dockerfile |
| DockerfileTag | Docker görüntüsü oluşturulurken kullanılan etiketi. Hata ayıklama, bir ": geliştirme" etiketine eklenir. | Aşağıdaki kurallar ile alfasayısal olmayan karakterleri çıkarma sonra derleme adı: <br/> Ardından sonuç etiketi tüm sayısal ise, "image" (örneğin, image2314) önek olarak eklenir <br/> Ardından sonuç etiketi boş bir dize ise, "image" etiket kullanılır. |
| DockerContext | Docker görüntüsü oluşturulurken kullanılan varsayılan bağlamı. | Visual Studio tarafından ayarlayın. |
| ContainerDevelopmentMode | (Hata ayıklama "Hızlı mod") "derleme-üzerinde-host" iyileştirme etkin olup olmadığını denetler.  İzin verilen değerler **hızlı** ve **normal**. | Hızlı |
| DockerDefaultTargetOS | Varsayılan hedef Docker görüntüsü oluşturma sırasında kullanılan işletim sistemini. | Visual Studio tarafından ayarlayın. |
| DockerImageLabels | Docker görüntüsüne uygulanan etiketler varsayılan kümesi. | com.microsoft.Created-By=Visual-Studio;com.microsoft.Visual-Studio.Project-Name=$(MSBuildProjectName) |
| ContainerVsDbgPath | VSDBG hata ayıklayıcı yoludur. | `%USERPROFILE%\vsdbg\vs2017u5` |
| DockerfileBuildArguments | Ek bağımsız değişkenler Docker derleme komutuyla geçirildi. | Geçerli değildir. |
| DockerfileRunArguments | Docker için geçirilen ek bağımsız değişkenler komutu çalıştırın. | Geçerli değildir. |
| DockerfileRunEnvironmentFiles | Noktalı virgül ile ayrılmış Docker run sırasında uygulanan ortamı dosyaların listesi. | Geçerli değildir. |
| DockerfileFastModeStage | Hata ayıklama modunda görüntüsü oluşturulurken kullanılan Dockerfile aşama (yani, hedef). | Birinci aşama (Temel) Dockerfile içinde bulunamadı |
| DockerDebuggeeProgram | Hata ayıklarken hata ayıklayıcı bu yürütülebilir dosyayı başlatmak için talimat verilmiştir. | .NET Core projeleri için: dotnet, ASP.NET .NET Framework projeleri: Uygulanamaz (IIS her zaman kullanılır) |
| DockerDebuggeeArguments | Hata ayıklarken hata ayıklayıcı bu bağımsız değişkenler başlatılan çalıştırılabilire talimat verilmiştir. | ASP.NET .NET Framework projeleri için geçerli değildir |
| DockerDebuggeeWorkingDirectory | Hata ayıklarken hata ayıklayıcı bu yolu çalışma dizini olarak kullanması talimat verilmiştir. | C:\app (Windows) veya /app (Linux) |
| DockerDebuggeeKillProgram | Bu komut, bir kapsayıcıda çalışan işlemi sonlandırmak için kullanılır. | ASP.NET .NET Framework projeleri için geçerli değildir |

## <a name="next-steps"></a>Sonraki adımlar

MSBuild hakkında bilgi için özellikleri genellikle görmek [MSBuild özellikleri](../msbuild/msbuild-properties.md).

## <a name="see-also"></a>Ayrıca bkz.

[MSBuild ayrılmış ve tanınmış özellikleri](../msbuild/msbuild-reserved-and-well-known-properties.md).
