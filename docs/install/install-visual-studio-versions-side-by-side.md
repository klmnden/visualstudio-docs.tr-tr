---
title: Visual Studio sürümlerini yan yana yükleme
ms.date: 03/05/2019
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.topic: conceptual
helpviewer_keywords:
- side-by-side installations [Visual Studio]
- Help [Visual Studio], installing
- install multiple versions of Visual Studio
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.openlocfilehash: 123f01b2e4545545a380f5a37adcdaf883bc9e91
ms.sourcegitcommit: 509fc3a324b7748f96a072d0023572f8a645bffc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58856936"
---
# <a name="install-visual-studio-versions-side-by-side"></a>Visual Studio sürümlerini yan yana yükleme

Visual Studio'nun önceki veya sonraki bir sürümü Visual Studio'nun zaten yüklü olan bir bilgisayara yükleyebilirsiniz.

::: moniker range="vs-2017"

Sürümleri yan yana yüklemeden önce aşağıdaki koşulları gözden geçirin:

* Visual Studio 2015'te oluşturulmuş bir çözümü açmak için Visual Studio 2017 kullanırsanız, daha sonra açın ve Visual Studio 2017'ye özgü herhangi bir özellik uygulamadığınız sürece çözümü yeniden eski sürümü değiştirin.

* Visual Studio 2015 veya önceki bir sürümünde oluşturulmuş bir çözümü açmak için Visual Studio 2017'yi kullanmaya çalışırsanız, projelerinizi ve dosyalarınızı Visual Studio 2017 ile uyumlu olacak şekilde değiştirmek gerekebilir. Daha fazla bilgi için [bağlantı noktası, geçirme ve Visual Studio projelerini yükseltme](../porting/port-migrate-and-upgrade-visual-studio-projects.md?view=vs-2017) sayfası.

::: moniker-end

::: moniker range=">= vs-2019"

Sürümleri yan yana yüklemeden önce aşağıdaki koşulları gözden geçirin:

* Visual Studio 2017'de oluşturulmuş bir çözümü açmak için Visual Studio 2019 kullanırsanız, daha sonra açın ve Visual Studio 2019 için belirli herhangi bir özellik uygulamadığınız sürece çözümü yeniden eski sürümü değiştirme.

* Visual Studio 2017 veya önceki bir sürümünde oluşturulmuş bir çözümü açmak için Visual Studio 2019 kullanmaya çalışırsanız, projelerinizi ve dosyalarınızı Visual Studio 2019'ile uyumlu olacak şekilde değiştirmek gerekebilir. Daha fazla bilgi için [bağlantı noktası, geçirme ve Visual Studio projelerini yükseltme](../porting/port-migrate-and-upgrade-visual-studio-projects.md) sayfası.

::: moniker-end

* Birden fazla sürümün yüklü olduğu bir bilgisayarda Visual Studio'nun bir sürümünü kaldırırsanız tüm sürümler için Visual Studio dosya ilişkilendirmeleri kaldırılır.

* Tüm uzantıları uyumlu olmadığından visual Studio uzantıları otomatik olarak yükseltmez. Uzantılar'dan yeniden yüklemeniz gerekir [Visual Studio Market](http://go.microsoft.com/fwlink/?LinkId=178891) veya yazılım yayımcısından.

## <a name="net-framework-versions-and-side-by-side-installations"></a>.NET framework sürümleri ve yan yana yüklemeler

Visual Basic, Visual C#, görsel ve F# projelerde kullan **hedef Framework'ü** seçeneğini **Proje Tasarımcısı** kullanan bir proje .NET Framework'ün hangi sürümünün belirtmek için. Bir C++ projesi için .vcxproj dosyasını değiştirerek hedef Framework'ü el ile değiştirebilirsiniz. Daha fazla bilgi için [.NET Framework'te sürüm uyumluluğu](/dotnet/framework/migration-guide/version-compatibility) sayfası.

Bir proje oluşturduğunuzda, projenin hangi .NET Framework sürümünü hedefleyeceğini belirtebilirsiniz **.NET Framework** listesinde **yeni proje** iletişim kutusu.

Dile özgü bilgiler için aşağıdaki tabloda ilgili konuya bakın.

::: moniker range="vs-2017"

| Dil | Konu |
|--------------|-----------|
| Visual Basic | [Uygulama Sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md?view=vs-2017) |
| Visual C# | [Uygulama Sayfası, Proje Tasarımcısı (C#)](../ide/reference/application-page-project-designer-csharp.md?view=vs-2017) |
| Visual F# | [Görselle geliştirme F# Visual Studio'da](../ide/fsharp-visual-studio.md?view=vs-2017) |
|C++ | [Nasıl yapılır: Hedef framework ve platform araç kümesini değiştirme](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset/) |

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleme](install-visual-studio.md?view=vs-2017)
* [Taşıma, geçirme ve Visual Studio projelerini yükseltme](../porting/port-migrate-and-upgrade-visual-studio-projects.md?view=vs-2017)
* [C/C++ oluşturma yalıtılmış uygulamalar ve yan yana derlemeler](/cpp/build/building-c-cpp-isolated-applications-and-side-by-side-assemblies/)

::: moniker-end

::: moniker range=">= vs-2019"

| Dil | Konu |
|--------------|-----------|
| Visual Basic | [Uygulama Sayfası, Proje Tasarımcısı (Visual Basic)](../ide/reference/application-page-project-designer-visual-basic.md) |
| Visual C# | [Uygulama Sayfası, Proje Tasarımcısı (C#)](../ide/reference/application-page-project-designer-csharp.md) |
| Visual F# | [Görselle geliştirme F# Visual Studio'da](../ide/fsharp-visual-studio.md) |
| C++ | [Nasıl yapılır: Hedef framework ve platform araç kümesini değiştirme](/cpp/build/how-to-modify-the-target-framework-and-platform-toolset/) |

[!INCLUDE[install_get_support_md](includes/install_get_support_md.md)]

## <a name="see-also"></a>Ayrıca bkz.

* [Visual Studio'yu yükleme](install-visual-studio.md)
* [Taşıma, geçirme ve Visual Studio projelerini yükseltme](../porting/port-migrate-and-upgrade-visual-studio-projects.md)
* [C/C++ oluşturma yalıtılmış uygulamalar ve yan yana derlemeler](/cpp/build/building-c-cpp-isolated-applications-and-side-by-side-assemblies/)

::: moniker-end