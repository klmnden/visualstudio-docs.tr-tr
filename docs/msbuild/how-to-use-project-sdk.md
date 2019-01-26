---
title: 'Nasıl yapılır: Bir MSBuild proje SDK başvurusu | Microsoft Docs'
ms.date: 01/25/2018
ms.topic: conceptual
helpviewer_keywords:
- MSBuild, SDKs, SDK
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 361b64191d10056d80ab89dd6d4254ca128dcc96
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55020600"
---
# <a name="how-to-use-msbuild-project-sdks"></a>Nasıl yapılır: MSBuild proje SDK'ları kullanın

[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] 15.0 "projesinde SDK" kavramını kullanıma sunulan özellikler ve içeri aktarılacak hedefler gerektiren bir yazılım geliştirme setleri kullanarak basitleştirir.

```xml
<Project Sdk="Microsoft.NET.Sdk">
    <PropertyGroup>
        <TargetFramework>net46</TargetFramework>
    </PropertyGroup>
</Project>
```

Projenin değerlendirme sırasında [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] örtük içeri aktarmalar üst ve alt projenizin ekler:

```xml
<Project>
    <!-- Implicit top import -->
    <Import Project="Sdk.props" Sdk="Microsoft.NET.Sdk" />

    <PropertyGroup>
        <TargetFramework>net46</TargetFramework>
    </PropertyGroup>

    <!-- Implicit bottom import -->
    <Import Project="Sdk.targets" Sdk="Microsoft.NET.Sdk" />
</Project>
```

## <a name="reference-a-project-sdk"></a>Bir proje SDK başvurusu

 SDK bir proje başvurusu için üç yol vardır:

1. Kullanım `Sdk` özniteliği `<Project/>` öğesi:

    ```xml
    <Project Sdk="My.Custom.Sdk">
        ...
    </Project>
    ```

    Üst ve alt yukarıda açıklandığı gibi bir projenin bir örtük içeri aktarması eklenir.  Biçimi `Sdk` özniteliği `Name[/Version]` sürüm olduğu isteğe bağlı.  Örneğin, belirtebilirsiniz `My.Custom.Sdk/1.2.3`.

    > [!NOTE]
    > Şu anda Mac için Visual Studio SDK proje başvurmak için desteklenen tek yol budur

2. Üst düzey kullanın `<Sdk/>` öğesi:

    ```xml
    <Project>
        <Sdk Name="My.Custom.Sdk" Version="1.2.3" />
        ...
    </Project>
   ```

   Üst ve alt yukarıda açıklandığı gibi bir projenin bir örtük içeri aktarması eklenir.  `Version` Öznitelik gerekli değildir.

3. Kullanım `<Import/>` , projenizdeki herhangi bir öğe:

    ```xml
    <Project>
        <PropertyGroup>
            <MyProperty>Value</MyProperty>
        </PropertyGroup>
        <Import Project="Sdk.props" Sdk="My.Custom.Sdk" />
        ...
        <Import Project="Sdk.targets" Sdk="My.Custom.Sdk" />
    </Project>
   ```

   Açıkça içeri aktarımlar projenizde dahil sırasını üzerinde tam denetim sağlar.

   Kullanırken `<Import/>` öğesi, isteğe bağlı belirtebilirsiniz `Version` de özniteliği.  Örneğin, belirtebilirsiniz `<Import Project="Sdk.props" Sdk="My.Custom.Sdk" Version="1.2.3" />`.

## <a name="how-project-sdks-are-resolved"></a>Proje SDK'ları nasıl çözümlenir

İçeri aktarma değerlendirirken [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] SDK alan adı ve sürümü, belirtilen proje yolu dinamik olarak çözümlenir.  [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] Ayrıca hangi makinenizde SDK projesi bulun eklentiler kayıtlı SDK Çözümleyicileri bir listesi bulunur.  Bu eklentilerin dahil et:

1. Yapılandırılmış paketinizi sorgular NuGet tabanlı bir çözümleyici kimliği ve belirttiğiniz SDK sürümü eşleştirmek için NuGet paketlerini akışları.<br/>
   Bu Çözümleyici, yalnızca belirttiğiniz isteğe bağlı bir sürüm ve tüm özel Proje SDK'sı kullanılabilir etkindir.  
2. .NET CLI'de yüklü SDK'ları çözümler .NET CLI çözümleyici.<br/>
   Bu çözümleyici proje SDK'ları gibi bulur `Microsoft.NET.Sdk` ve `Microsoft.NET.Sdk.Web` ürünün bir parçası olduğu.
3. MSBuild ile yüklenmiş SDK'ları çözümler varsayılan çözümleyici.

SDK'sı NuGet tabanlı çözümleyici destekleyen bir sürüm belirtme, [global.json](https://docs.microsoft.com/dotnet/core/tools/global-json) proje SDK sürümü tek bir yerde yerine her bir proje denetlemesine olanak sağlar:

```json
{
    "msbuild-sdks": {
        "My.Custom.Sdk": "5.0.0",
        "My.Other.Sdk": "1.0.0-beta"
    }
}
```

Bir yapı sırasında her proje SDK yalnızca bir sürümü kullanılabilir.  MSBuild, iki farklı sürümünü aynı projede SDK başvurduğunuz, bir uyarı yayar.  Önerilir **değil** içinde bir sürüm belirtilmezse, projelerinizde bir sürüm belirtin, *global.json*.  

## <a name="see-also"></a>Ayrıca bkz.

 [MSBuild kavramları](../msbuild/msbuild-concepts.md)   
 [Derlemenizi özelleştirme](../msbuild/customize-your-build.md)   
 [Paketler, meta verileri ve çerçeveler](/dotnet/core/packages)   
 [.NET Core csproj biçimine eklemeler](/dotnet/core/tools/csproj)
