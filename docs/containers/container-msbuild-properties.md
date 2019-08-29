---
title: Visual Studio kapsayıcı araçları derleme özellikleri
author: ghogen
description: Kapsayıcı araçları derleme işlemine genel bakış
ms.author: ghogen
ms.date: 06/06/2019
ms.technology: vs-azure
ms.topic: conceptual
ms.openlocfilehash: 4bc6cb4221d85bd43b98b2ac36c34c919937960b
ms.sourcegitcommit: 3cda0d58c5cf1985122b8977b33a171c7359f324
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/29/2019
ms.locfileid: "70152531"
---
# <a name="container-tools-build-properties"></a>Kapsayıcı araçları derleme özellikleri

MSBuild 'in projenizi oluşturmak için kullandığı özellikleri ayarlayarak, Visual Studio 'Nun kapsayıcı projelerinizi nasıl derlemediğini özelleştirebilirsiniz. Örneğin, Dockerfile adını değiştirebilir, görüntüleriniz için Etiketler ve Etiketler belirtebilir, Docker komutlarına geçirilen ek bağımsız değişkenleri sağlayabilir ve Visual Studio 'nun kapsayıcı ortamı. Ayrıca, başlatılacak yürütülebilir dosyanın adı ve sağlanacak komut satırı bağımsız değişkenleri gibi hata ayıklama özelliklerini de ayarlayabilirsiniz.

Bir özelliğin değerini ayarlamak için proje dosyasını düzenleyin. Örneğin, Dockerfile adlı dosyanın *Mydockerfile*olduğunu varsayalım. Proje dosyasındaki `DockerfileFile` özelliğini aşağıdaki gibi ayarlayabilirsiniz.

```xml
<PropertyGroup>
   <DockerfileFile>MyDockerfile</DockerfileFile>
</PropertyGroup>
```

Özellik ayarını varolan `PropertyGroup` bir öğeye ekleyebilirsiniz, yoksa yeni `PropertyGroup` bir öğe oluşturun.

Aşağıdaki tabloda kapsayıcı projeleri için kullanılabilen MSBuild özellikleri gösterilmektedir.

| Özellik adı | Açıklama | Varsayılan değer  |
|---------------|-------------|----------------|
| DockerfileFile | Projenin kapsayıcısını derlemek/çalıştırmak için kullanılacak varsayılan Dockerfile öğesini açıklar. Bu bir yol da olabilir. | Dockerfile |
| DockerfileTag | Docker görüntüsü oluşturulurken kullanılacak etiket. Hata ayıklama sırasında, etikete bir ":d ev" eklenir. | Aşağıdaki kurallarla alfasayısal olmayan karakterleri gerçekleştirdikten sonra bütünleştirilmiş kod adı: <br/> Sonuç etiketi tümü sayısal ise, "görüntü" bir ön ek olarak eklenir (örneğin, image2314) <br/> Sonuç etiketi boş bir dizeyse, etiket olarak "görüntü" kullanılır. |
| DockerContext | Docker görüntüsü oluşturulurken kullanılan varsayılan bağlam. | Visual Studio tarafından ayarlanır. |
| ContainerDevelopmentMode | "Konak oluşturma" iyileştirmesi ("hızlı mod" hata ayıklama) etkin olup olmadığını denetler.  İzin verilen değerler **hızlı** ve **normal**. | Hızlı |
| DockerDefaultTargetOS | Docker görüntüsü oluşturulurken kullanılan varsayılan hedef işletim sistemi. | Visual Studio tarafından ayarlanır. |
| Dockerımagelabels | Docker görüntüsüne uygulanan varsayılan etiket kümesi. | com. Microsoft. Created-By = Visual-Studio; com. Microsoft. Visual-Studio. Project-Name = $ (MSBuildProjectName) |
| ContainerVsDbgPath | VSDBG hata ayıklayıcısı için yol. | `%USERPROFILE%\vsdbg\vs2017u5` |
| DockerfileBuildArguments | Docker Build komutuna ek bağımsız değişkenler geçirildi. | Geçerli değildir. |
| DockerfileRunArguments | Docker Run komutuna ek bağımsız değişkenler geçirildi. | Geçerli değildir. |
| DockerfileRunEnvironmentFiles | Docker çalıştırması sırasında uygulanan ortam dosyalarının noktalı virgülle ayrılmış listesi. | Geçerli değildir. |
| DockerfileFastModeStage | Görüntü hata ayıklama modunda oluşturulurken kullanılacak Dockerfile aşaması (yani, hedef). | Dockerfile 'da bulunan ilk aşama (temel) |
| DockerDebuggeeProgram | Hata ayıklarken, hata ayıklayıcıda bu çalıştırılabiliri başlatması istendi. | .NET Core projeleri için: DotNet, ASP.NET .NET Framework projeleri: Uygulanamaz (IIS her zaman kullanılır) |
| DockerDebuggeeArguments | Hata ayıklarken, hata ayıklayıcı, bu bağımsız değişkenleri başlatılan yürütülebilir dosyaya iletmektir. | ASP.NET .NET Framework projelerine uygulanamaz |
| Dockerdebuggeeworkingdizini | Hata ayıklarken, hata ayıklayıcının bu yolu çalışma dizini olarak kullanması talimatı verilir. | C:\app (Windows) veya/App (Linux) |
| DockerDebuggeeKillProgram | Bu komut, bir kapsayıcıda çalışan işlemi sonlandırmak için kullanılır. | ASP.NET .NET Framework projelerine uygulanamaz |

## <a name="next-steps"></a>Sonraki adımlar

MSBuild özellikleri hakkında genel bilgi için bkz. [MSBuild özellikleri](../msbuild/msbuild-properties.md).

## <a name="see-also"></a>Ayrıca bkz.

[Docker Compose derleme özellikleri](docker-compose-properties.md)

[Kapsayıcı araçları başlatma ayarları](container-launch-settings.md)

[MSBuild ayrılmış ve iyi bilinen Özellikler](../msbuild/msbuild-reserved-and-well-known-properties.md)
