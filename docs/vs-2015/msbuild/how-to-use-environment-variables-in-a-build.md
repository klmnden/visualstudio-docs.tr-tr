---
title: 'Nasıl yapılır: Derlemede ortam değişkenlerini kullanma | Microsoft Docs'
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
ms.topic: conceptual
helpviewer_keywords:
- environment variables, referencing
- projects [.NET Framework], environment variables
- MSBuild, environment variables
ms.assetid: 7f9e4469-8865-4b59-aab3-3ff26bd36e77
caps.latest.revision: 21
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 72d810f998b111aa2ec08a5874498ed8ee23a3be
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63437886"
---
# <a name="how-to-use-environment-variables-in-a-build"></a>Nasıl yapılır: Derlemede Ortam Değişkenlerini Kullanma
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Projeler derlerken genellikle proje dosyası veya proje oluşturan dosyaların değil bilgileri kullanarak yapı seçeneklerini ayarlamak gereklidir. Bu bilgiler genellikle ortam değişkenleri olarak depolanır.  
  
## <a name="referencing-environment-variables"></a>Başvuruda bulunan ortam değişkenleri  
 Tüm ortam değişkenleri kullanılabilir [!INCLUDE[vstecmsbuildengine](../includes/vstecmsbuildengine-md.md)] ([!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)]) özellikleri olarak proje dosyası.  
  
> [!NOTE]
> Proje dosyası açık bir ortam değişkeni ile aynı ada sahip bir özellik tanımı içeriyorsa, proje dosyasındaki özellik ortam değişkeninin değerini geçersiz kılar.  
  
#### <a name="to-use-an-environment-variable-in-an-msbuild-project"></a>İçinde bir MSBuild Projesi bir ortam değişkenini kullanmak için  
  
- Ortam değişkeni, proje dosyasında bildirilen bir değişken olduğu gibi başvuru. Örneğin, aşağıdaki kodu BIN_PATH ortam değişkeni başvuruyor:  
  
   `<FinalOutput>$(BIN_PATH)\MyAssembly.dll</FinalOutput>`  
  
  Kullanabileceğiniz bir `Condition` ortam değişkeni ayarlanmamış olması halinde bir özellik için varsayılan bir değer sağlamak için özniteliği.  
  
#### <a name="to-provide-a-default-value-for-a-property"></a>Bir özellik için varsayılan bir değer sağlamak için  
  
- Kullanım bir `Condition` özellik değeri yalnızca şu durumlarda ayarlamak için bir özellik özniteliğini değere sahip değil. Örneğin, aşağıdaki ayarlar kod `ToolsPath` c:\tools yalnızca şu durumlarda özelliğini `ToolsPath` ortam değişkeninin ayarlı değil:  
  
     `<ToolsPath Condition="'$(TOOLSPATH)' == ''">c:\tools</ToolsPath>`  
  
    > [!NOTE]
    > Özellik adlarını büyük küçük harfe duyarlı olmayan şekilde hem `$(ToolsPath)` ve `$(TOOLSPATH)` aynı özellik veya ortam değişkeni başvurusu.  
  
## <a name="example"></a>Örnek  
 Aşağıdaki proje dosyası, dizin konumunu belirtmek için ortam değişkenlerini kullanır.  
  
```  
<Project DefaultTargets="FakeBuild">  
    <PropertyGroup>  
        <FinalOutput>$(BIN_PATH)\myassembly.dll</FinalOutput>  
        <ToolsPath Condition=" '$(ToolsPath)' == '' ">  
            C:\Tools  
        </ToolsPath>  
    </PropertyGroup>  
    <Target Name="FakeBuild">  
        <Message Text="Building $(FinalOutput) using the tools at $(ToolsPath)..."/>  
    </Target>  
</Project>  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  

[MSBuild](msbuild.md)

[MSBuild Özellikleri](../msbuild/msbuild-properties1.md)

[Nasıl yapılır: Aynı Kaynak Dosyalarını Farklı Seçeneklerle Derleme](../msbuild/how-to-build-the-same-source-files-with-different-options.md)
