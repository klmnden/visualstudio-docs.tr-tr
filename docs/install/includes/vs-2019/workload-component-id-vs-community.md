---
title: Visual Studio Community 2019 iş yükü ve bileşen kimlikleri
titleSuffix: ''
description: İş yükü ve Bileşen kimlikleri komut satırını kullanarak Visual Studio'yu yükleyin veya bağımlılık VSIX bildirimi olarak belirtmek için kullanın.
keywords: ''
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.date: 07/24/2019
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.topic: include
ms.openlocfilehash: ffaaeaa619b4cf0ef35d0b4effa3d628cd47b772
ms.sourcegitcommit: 0f5f7955076238742f2071d286ad8e896f3a6cad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68484846"
---
## <a name="visual-studio-core-editor-included-with-visual-studio-community-2019"></a>Visual Studio çekirdek Düzenleyicisi (Visual Studio Community 2019 ile birlikte)

**NUMARASINI** Microsoft. VisualStudio. Workload. CoreEditor

**Açıklama:** Sözdizimi kullanan kod düzenlemesi, kaynak kodu denetimi ve iş öğesi yönetimi de dahil olmak üzere Visual Studio Core kabuğu deneyimi.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.CoreEditor | Visual Studio temel Düzenleyicisi | 16.1.28811.260 | Gerekli
Microsoft.VisualStudio.Component.StartPageExperiment.Cpp | Visual Studio başlangıç sayfasını C++ kullanıcılar | 16.0.28315.86 | İsteğe Bağlı

## <a name="azure-development"></a>Azure geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. Azure

**Açıklama:** Bulut uygulamaları geliştirmeye, kaynak oluşturmaya ve Docker desteği dahil kapsayıcılar oluşturmaya yönelik Azure SDK 'Ları, araçları ve projeleri.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | Gerekli
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure Web Işleri araçları | 16.0.28714.129 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.1.28810.153 | Gerekli
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.FSharp.WebTemplates | F#web projeleri için dil desteği | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Gerekli
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Azure.Prerequisites | Azure geliştirme önkoşulları | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure Web Işleri araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake ve Stream Analytics araçları | 16.2.28915.88 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.VisualStudio.Component.AspNet45 | Gelişmiş ASP.NET özellikleri | 16.0.28315.86 | Önerilen
Microsoft. VisualStudio. Component. Azure. Kubernetes. Tools | Kubernetes için Visual Studio Araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ResourceManager.Tools | Azure Resource Manager temel araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Azure.ServiceFabric.Tools | Service Fabric Araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton | Azure Cloud Services temel araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure Cloud Services derleme araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Azure.CloudServices | Azure Cloud Services araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Azure.ResourceManager.Tools | Azure Resource Manager araçları | 16.0.28528.71 | Önerilen
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.SDK | .NET framework 4.7.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net. ComponentGroup. 4.6.1. DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. net. Core. Component. SDK. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. DevelopmentTools. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. Web. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Storage.AzCopy | Azure depolama AzCopy | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | İsteğe Bağlı

## <a name="data-storage-and-processing"></a>Veri depolama ve işleme

**NUMARASINI** Microsoft. VisualStudio. Workload. Data

**Açıklama:** SQL Server, Azure Data Lake veya Hadoop ile veri çözümlerini bağlayın, geliştirin ve test edin.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | Önerilen
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Önerilen
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake ve Stream Analytics araçları | 16.2.28915.88 | Önerilen
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.1.28810.153 | Önerilen
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton | Azure Cloud Services temel araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure Cloud Services derleme araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Önerilen
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Önerilen
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Önerilen
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | Önerilen
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Önerilen
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | Önerilen
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Önerilen
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Önerilen
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.FSharp.Desktop | F#Masaüstü dil desteği | 16.0.28315.86 | İsteğe Bağlı

## <a name="data-science-and-analytical-applications"></a>Veri bilimi ve analitik uygulamalar

**NUMARASINI** Microsoft. VisualStudio. Workload. DataScience

**Açıklama:** Python ve F#dahil olmak üzere veri bilimi uygulamaları oluşturmak için Diller ve araçlar.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.PythonTools | Python dil desteği | 16.0.28625.61 | Önerilen
Microsoft. Component. PythonTools. Minicondax64 | Python miniconda | 16.2.29003.222 | Önerilen
Microsoft.Component.PythonTools.Web | Python web desteği | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.FSharp.Desktop | F#Masaüstü dil desteği | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Önerilen
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Önerilen
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Python yerel geliştirme araçları | 16.2.29020.229 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | İsteğe Bağlı
Microsoft. VisualStudio. Component. Windows10SDK. 18362 | Windows 10 SDK (10.0.18362.0) | 16.1.28829.92 | İsteğe Bağlı

## <a name="net-desktop-development"></a>.NET masaüstü geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. ManagedDesktop

**Açıklama:** , Visual Basic ve C# F#kullanarak WPF, Windows Forms ve konsol uygulamaları oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | .NET masaüstü geliştirme araçları | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Component. Microsoft. VisualStudio. Livespaylaşımı | Live Share | 1.0.473 | Önerilen
Microsoft.ComponentGroup.Blend | Visual Studio için Blend | 16.0.28315.86 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.VisualStudio.Component.Debugger.JustInTime | Just-In-Time hata ayıklayıcı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 araçları | 16.0.28315.86 | Önerilen
Component.Dotfuscator | PreEmptive koruma - Dotfuscator | 16.0.28528.71 | İsteğe Bağlı
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | İsteğe Bağlı
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.SDK | .NET framework 4.7.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net. ComponentGroup. 4.6.1. DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. net. Core. Component. SDK. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. DevelopmentTools. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.FSharp.Desktop | F#Masaüstü dil desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | İsteğe Bağlı
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | İsteğe Bağlı
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | İsteğe Bağlı
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.PortableLibrary | .NET taşınabilir kitaplık targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | İsteğe Bağlı
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | İsteğe Bağlı

## <a name="game-development-with-unity"></a>Unity ile oyun geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. ManagedGame

**Açıklama:** Güçlü platformlar arası bir geliştirme ortamı olan Unity ile 2B ve 3B Oyunlar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Net.Component.3.5.DeveloperTools | .NET framework 3.5 geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Unity | Unity için Visual Studio Araçları | 16.0.28315.86 | Gerekli
Component.UnityEngine.x64 | Unity 2018,3 64-bit düzenleyici | 16.1.28810.153 | Önerilen
Component.UnityEngine.x86 | Unity 5.6 32 bit Düzenleyici | 16.1.28811.260 | Önerilen

## <a name="linux-development-with-c"></a>C++ ile Linux geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NativeCrossPlat

**Açıklama:** Oluşturun ve bir Linux ortamında çalışan uygulamalarda hata ayıklayın.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.MDD.Linux | C++Linux geliştirme için | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | Gerekli
Component.Linux.CMake | C++Linux için CMake araçları | 16.2.29003.222 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Component.MDD.Linux.GCC.arm | Katıştırılmış ve IoT geliştirme araçları | 16.2.28915.88 | İsteğe Bağlı

## <a name="desktop-development-with-c"></a>C++ ile masaüstü geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NativeDesktop

**Açıklama:** Microsoft C++ araç TAKıMı, ATL veya MFC kullanarak Windows Masaüstü uygulamaları oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++2019 yeniden dağıtılabilir güncelleştirme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | C++Çekirdek masaüstü özellikleri | 16.2.29012.281 | Gerekli
Component. Microsoft. VisualStudio. Livespaylaşımı | Live Share | 1.0.473 | Önerilen
Microsoft.VisualStudio.Component.Debugger.JustInTime | Just-In-Time hata ayıklayıcı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | Önerilen
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Önerilen
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Önerilen
Microsoft.VisualStudio.Component.VC.ATL | C++V142 için ATL derleme araçları (x86 & x64) | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.CMake.Project | C++Windows için CMake araçları | 16.2.29003.222 | Önerilen
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.TestAdapterForBoostTest | Boost.Test için test bağdaştırıcısı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.VC.TestAdapterForGoogleTest | Google Test için test bağdaştırıcısı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | Önerilen
Microsoft. VisualStudio. Component. Windows10SDK. 18362 | Windows 10 SDK (10.0.18362.0) | 16.1.28829.92 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Component.Incredibuild | IncrediBuild - derleme hızlandırma | 16.0.28528.71 | İsteğe Bağlı
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.10 | İsteğe Bağlı
Microsoft.Component.VC.Runtime.UCRTSDK | Windows Evrensel CRT SDK | 16.0.28625.61 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.140 | MSVC v140-VS 2015 C++ derleme araçları (v 14.00) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.ATLMFC | C++V142 derleme araçları için MFC (x86 & x64) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CLI.Support | C++V142 derleme araçları için/CLı desteği (14,22) | 16.2.29003.222 | İsteğe Bağlı
Microsoft. VisualStudio. Component. VC. LLVM. Clang | Windows için C++ Clang derleyicisi (8.0.0) | 16.2.29019.55 | İsteğe Bağlı
Microsoft. VisualStudio. Component. VC. LLVM. Clangaraç takımı | C++V142 derleme araçları için Clang-CL (x64/x86) | 16.2.29109.103 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | C++V142 derleme araçları için modüller (x64/x86 – deneysel) | 16.0.28625.61 | İsteğe Bağlı
Microsoft. VisualStudio. Component. VC. v141. x86. x64 | MSVC v141-VS 2017 C++ x64/x86 derleme araçları (v 14.16) | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft. VisualStudio. ComponentGroup. NativeDesktop. LLVM. Clang | C++Windows için Clang araçları (8.0.0-x64/x86) | 16.2.29019.55 | İsteğe Bağlı

## <a name="game-development-with-c"></a>C++ ile oyun geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NativeGame

**Açıklama:** DirectX, Unreal veya C++ Cocos2d tarafından desteklenen profesyonel oyunlar oluşturmak için tam gücünü kullanın.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++2019 yeniden dağıtılabilir güncelleştirme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | Önerilen
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Önerilen
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft. VisualStudio. Component. Windows10SDK. 18362 | Windows 10 SDK (10.0.18362.0) | 16.1.28829.92 | Önerilen
Component. Android. NDK. R16B | Android NDK (R16B) | 16.2.29116.78 | İsteğe Bağlı
Component.Android.SDK25.Private | Android SDK kurulumu (API düzeyi 25) (ile C++mobil geliştirme için yerel yükleme) | 16.0.28625.61 | İsteğe Bağlı
Component.Ant | Apache Ant (1.9.3) | 1.9.3.8 | İsteğe Bağlı
Component.Cocos | Cocos | 16.0.28315.86 | İsteğe Bağlı
Component.Incredibuild | IncrediBuild - derleme hızlandırma | 16.0.28528.71 | İsteğe Bağlı
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.10 | İsteğe Bağlı
Component.MDD.Android | C++ Android geliştirici araçları | 16.0.28517.75 | İsteğe Bağlı
Component.OpenJDK | OpenJDK (Microsoft dağıtımı) | 16.1.28811.260 | İsteğe Bağlı
Component.Unreal | Unreal Engine yükleyicisi | 16.1.28810.153 | İsteğe Bağlı
Component.Unreal.Android | Unreal Engine için Android IDE desteği | 16.1.28810.153 | İsteğe Bağlı
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.VisualStudio.Component.NuGet.BuildTools | NuGet hedefleri ve derleme görevleri | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | İsteğe Bağlı

## <a name="mobile-development-with-c"></a>C++ ile Mobil Geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NativeMobile

**Açıklama:** Kullanarak C++IOS, Android veya Windows için platformlar arası uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Android.SDK25.Private | Android SDK kurulumu (API düzeyi 25) (ile C++mobil geliştirme için yerel yükleme) | 16.0.28625.61 | Gerekli
Component.OpenJDK | OpenJDK (Microsoft dağıtımı) | 16.1.28811.260 | Gerekli
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | Gerekli
Component. Android. NDK. R16B | Android NDK (R16B) | 16.2.29116.78 | Önerilen
Component.Ant | Apache Ant (1.9.3) | 1.9.3.8 | Önerilen
Component.MDD.Android | C++ Android geliştirici araçları | 16.0.28517.75 | Önerilen
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Önerilen
Component. Android. NDK. R16B_3264 | Android NDK (R16B) (32 bit) | 16.2.29116.78 | İsteğe Bağlı
Component. Google. Android. öykünücü. API25. Private | Google Android Emulator (API düzeyi 25) (yerel yüklemesi) | 16.1.28810.153 | İsteğe Bağlı
Component.HAXM.Private | Intel donanım hızlandırılmış yürütme Yöneticisi (HAXM) (yerel kurulum) | 16.0.28528.71 | İsteğe Bağlı
Component.Incredibuild | IncrediBuild - derleme hızlandırma | 16.0.28528.71 | İsteğe Bağlı
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.10 | İsteğe Bağlı
Component.MDD.IOS | C++ iOS geliştirici araçları | 16.0.28517.75 | İsteğe Bağlı

## <a name="net-core-cross-platform-development"></a>.NET core platformlar arası geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NetCoreTools

**Açıklama:** .NET Core, ASP.NET Core, HTML/JavaScript ve Docker desteği dahil kapsayıcılar kullanarak platformlar arası uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.FSharp.WebTemplates | F#web projeleri için dil desteği | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Component. Microsoft. VisualStudio. Livespaylaşımı | Live Share | 1.0.473 | Önerilen
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure Web Işleri araçları | 16.0.28714.129 | Önerilen
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.2.28917.182 | Önerilen
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.1.28810.153 | Önerilen
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure Web Işleri araçları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Web.CloudTools | Web geliştirme için bulut araçları | 16.2.29003.222 | Önerilen
Microsoft. net. Core. Component. SDK. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. DevelopmentTools. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. Web. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Geliştirme zamanı IIS desteği | 16.0.28315.86 | İsteğe Bağlı

## <a name="mobile-development-with-net"></a>.NET ile Mobil Geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NETbir Splat

**Açıklama:** Xamarin kullanarak iOS, Android veya Windows için platformlar arası uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.OpenJDK | OpenJDK (Microsoft dağıtımı) | 16.1.28811.260 | Gerekli
Component.Xamarin | Xamarin | 16.1.28810.153 | Gerekli
Component.Xamarin.RemotedSimulator | Xamarin uzak simülatör | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.Merq | Ortak Xamarin iç araçları | 16.2.29012.281 | Gerekli
Microsoft.VisualStudio.Component.MonoDebugger | Mono hata ayıklayıcısı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions.TemplateEngine | ASP.NET şablon oluşturma altyapısı | 16.0.28315.86 | Gerekli
Component. Android. SDK28 | Android SDK kurulumu (API düzeyi 28) | 16.2.29003.222 | Önerilen

## <a name="aspnet-and-web-development"></a>ASP.NET ve web geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. NetWeb

**Açıklama:** ASP.NET, ASP.NET Core, HTML/JavaScript ve Docker desteği dahil kapsayıcılar kullanarak Web uygulamaları oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.FSharp.WebTemplates | F#web projeleri için dil desteği | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Gerekli
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Component. Microsoft. VisualStudio. Livespaylaşımı | Live Share | 1.0.473 | Önerilen
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure Web Işleri araçları | 16.0.28714.129 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.2.28917.182 | Önerilen
Microsoft.VisualStudio.Component.AspNet45 | Gelişmiş ASP.NET özellikleri | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.1.28810.153 | Önerilen
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure Web Işleri araçları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Web.CloudTools | Web geliştirme için bulut araçları | 16.2.29003.222 | Önerilen
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.SDK | .NET framework 4.7.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net. ComponentGroup. 4.6.1. DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. net. Core. Component. SDK. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. DevelopmentTools. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. NetCore. ComponentGroup. Web. 2.2 | .NET Core 2,2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | İsteğe Bağlı
Microsoft. VisualStudio. ComponentGroup. Addiwebprojecttemplates | Ek proje şablonları (önceki sürümler) | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Geliştirme zamanı IIS desteği | 16.0.28315.86 | İsteğe Bağlı

## <a name="nodejs-development"></a>Node.js geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. Node

**Açıklama:** Zaman uyumsuz olay temelli bir JavaScript çalışma zamanı olan Node. js kullanarak ölçeklenebilir ağ uygulamaları oluşturun. 

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.Node.Tools | Node. js geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Component. Microsoft. VisualStudio. Livespaylaşımı | Live Share | 1.0.473 | Önerilen
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.2.28917.182 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı

## <a name="officesharepoint-development"></a>Office/SharePoint geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. Office

**Açıklama:** , Vb ve JavaScript kullanarak C#Office ve SharePoint eklentileri, SharePoint ÇÖZÜMLERI ve VSTO eklentileri oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.2.28917.182 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | .NET masaüstü geliştirme araçları | 16.2.29003.222 | Gerekli
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Sharepoint.Tools | Visual Studio için Office Geliştirici Araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Gerekli
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.Workflow | Windows Workflow Foundation | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.TeamOffice | (VSTO) Office için Visual Studio Araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.SDK | .NET framework 4.7.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net. ComponentGroup. 4.6.1. DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft. VisualStudio. ComponentGroup. SharePoint. WıF | Windows Identity Foundation 3,5 | 16.0.28621.142 | İsteğe Bağlı

## <a name="python-development"></a>Python geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. Python

**Açıklama:** Python için düzen, hata ayıklama, etkileşimli geliştirme ve kaynak denetimi.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.PythonTools | Python dil desteği | 16.0.28625.61 | Gerekli
Component.CPython3.x64 | Python 3 64-bit (3.7.3) | 3.7.3 | Önerilen
Component. Microsoft. VisualStudio. Livespaylaşımı | Live Share | 1.0.473 | Önerilen
Microsoft. Component. PythonTools. Minicondax64 | Python miniconda | 16.2.29003.222 | Önerilen
Microsoft.Component.PythonTools.Web | Python web desteği | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.2.29003.222 | Önerilen
Microsoft. VisualStudio. Component. TypeScript. 3.5 | TypeScript 3,5 SDK | 16.0.29012.281 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Component.CPython2.x64 | Python 2 64-bit (2.7.16) | 2.7.16 | İsteğe Bağlı
Component.CPython2.x86 | Python 2 32-bit (2.7.16) | 2.7.16 | İsteğe Bağlı
Component.CPython3.x86 | Python 3 32-bit (3.7.3) | 3.7.3 | İsteğe Bağlı
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28714.129 | İsteğe Bağlı
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | İsteğe Bağlı
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | İsteğe Bağlı
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Python yerel geliştirme araçları | 16.2.29020.229 | İsteğe Bağlı
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | İsteğe Bağlı
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.1.28810.153 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Waverton | Azure Cloud Services temel araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure Cloud Services derleme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | İsteğe Bağlı
Microsoft. VisualStudio. Component. MSODBC. SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | İsteğe Bağlı
Microsoft. VisualStudio. Component. MSSQL. CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28707.177 | İsteğe Bağlı
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.1.28811.260 | İsteğe Bağlı
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | İsteğe Bağlı
Microsoft. VisualStudio. Component. Windows10SDK. 18362 | Windows 10 SDK (10.0.18362.0) | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.1.28812.146 | İsteğe Bağlı

## <a name="universal-windows-platform-development"></a>Evrensel Windows platformu geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. Universal

**Açıklama:** C#, Vb veya isteğe bağlı olarak C++Evrensel Windows platformu uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.NetFX.Native | .NET Yerel | 16.0.28315.86 | Gerekli
Microsoft.ComponentGroup.Blend | Visual Studio için Blend | 16.0.28315.86 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.2.28917.182 | Gerekli
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Graphics | Görüntü ve 3B model düzenleyicileri | 16.0.28517.75 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft. VisualStudio. Component. Windows10SDK. 18362 | Windows 10 SDK (10.0.18362.0) | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.ComponentGroup.UWP.NetCoreAndStandard | .NET native ve .NET Standard | 16.0.28516.191 | Gerekli
Microsoft. VisualStudio. ComponentGroup. UWP. support | Evrensel Windows platformu araçları | 16.2.29003.222 | Gerekli
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | Xamarin için evrensel Windows platformu araçları | 16.2.29020.229 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.UWP.VC.ARM64 | C++V142 derleme araçları için Evrensel Windows Platformu desteği (ARM64) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++2019 yeniden dağıtılabilir güncelleştirme | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.ARM | MSVC v142-VS 2019 C++ ARM derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | MSVC v142-VS 2019 C++ ARM64 derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı
Microsoft. VisualStudio. Component. VC. v141. ARM | MSVC v141-VS 2017 C++ ARM derleme araçları (v 14.16) | 16.2.29003.222 | İsteğe Bağlı
Microsoft. VisualStudio. Component. VC. v141. ARM64 | MSVC v141-VS 2017 C++ ARM64 derleme araçları (v 14.16) | 16.1.28829.92 | İsteğe Bağlı
Microsoft. VisualStudio. Component. VC. v141. x86. x64 | MSVC v141-VS 2017 C++ x64/x86 derleme araçları (v 14.16) | 16.1.28829.92 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.IpOverUsb | USB cihaz bağlantısı | 16.2.29020.229 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | C++Çekirdek masaüstü özellikleri | 16.2.29012.281 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.UWP.VC | C++(v142) Evrensel Windows Platformu araçları | 16.2.29020.229 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.UWP.VC.v141 | C++v141 Evrensel Windows Platformu araçları | 16.1.28810.153 | İsteğe Bağlı

## <a name="visual-studio-extension-development"></a>Visual Studio uzantısı geliştirme

**NUMARASINI** Microsoft. VisualStudio. Workload. VisualStudioExtension

**Açıklama:** Visual Studio için yeni komutlar, kod Çözümleyicileri ve araç pencereleri dahil eklentiler ve uzantılar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.1.28811.260 | Gerekli
Microsoft. VisualStudio. Component. ıntellicode | IntelliCode | 0.1 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28714.129 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.1.28829.92 | Gerekli
Microsoft.VisualStudio.Component.VSSDK | Visual Studio SDK | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.ComponentGroup.VisualStudioExtension.Prerequisites | Visual Studio uzantı geliştirme önkoşulları | 16.2.29012.281 | Gerekli
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Önerilen
Component.Dotfuscator | PreEmptive koruma - Dotfuscator | 16.0.28528.71 | İsteğe Bağlı
Microsoft.Component.CodeAnalysis.SDK | .NET Compiler Platform SDK’sı | 16.2.29003.222 | İsteğe Bağlı
Microsoft.Component.VC.Runtime.OSSupport | C++V142 derleme araçları için Evrensel Windows Platformu çalışma zamanı | 16.1.28811.260 | İsteğe Bağlı
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.2.28917.182 | İsteğe Bağlı
Microsoft.VisualStudio.Component.ClassDesigner | Sınıf Tasarımcısı | 16.0.28528.71 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DslTools | Modelleme SDK'sı | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.ATL | C++V142 için ATL derleme araçları (x86 & x64) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.ATLMFC | C++V142 derleme araçları için MFC (x86 & x64) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++Temel Özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.22) | 16.2.29003.222 | İsteğe Bağlı

## <a name="unaffiliated-components"></a>Kullanıcıyla bağlantılı olmayan bileşenleri

Bu, her türlü iş yükü ile dahil edilmez, ancak tek bir bileşeni olarak seçilebilir bileşenlerdir.

Bileşen kimliği | Ad | Sürüm
--- | --- | ---
Component.GitHub.VisualStudio | Visual Studio için GitHub uzantısı | 2.5.9.5485
Component.Xamarin.Inspector | Xamarin Inspector | 16.0.28315.86
Component.Xamarin.Profiler | Xamarin Profiler | 16.0.28315.86
Component. Xamarin. kitaplarında | Xamarin Workbooks | 16.0.28315.86
Microsoft.Component.ClickOnce | ClickOnce yayımlama | 16.0.28707.177
Microsoft.Component.HelpViewer | Yardım Görüntüleyicisi | 16.0.28625.61
Microsoft.NetCore.1x.ComponentGroup.Web | Web için .NET core 1.0-1.1 geliştirme araçları | 16.0.28621.142
Microsoft. VisualStudio. Component. AzureDevOps. Officetümleştirmesi | Azure DevOps Office tümleştirmesi | 16.0.28625.61
Microsoft.VisualStudio.Component.DependencyValidation.Community | Bağımlılık doğrulama | 16.0.28517.75
Microsoft.VisualStudio.Component.Git | Windows için Git | 16.0.28625.61
Microsoft.VisualStudio.Component.GraphDocument | DGML Düzenleyici | 16.0.28625.61
Microsoft.VisualStudio.Component.LinqToSql | LINQ to SQL araçları | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. 14.20. ARM | MSVC v142-VS 2019 C++ ARM derleme araçları (v 14.20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ARM. Spectre | MSVC v142-VS 2019 C++ ARM Spectre-azaltılan LIBS (v 14.20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ARM64 | MSVC v142-VS 2019 C++ ARM64 derleme araçları (v 14.20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ARM64. Spectre | MSVC v142-VS 2019 C++ ARM64 Spectre-azaltılan LIBS (v 14.20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ATL | C++v142 derleme araçları için v 14.20 ATL (x86 & x64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ATL. ARM | C++v142 derleme araçları için v 14.20 ATL (ARM) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ATL. ARM. Spectre | C++Spectre azaltmaları (ARM) ile v142 derleme araçları için v 14.20 ATL | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ATL. ARM64 | C++v142 derleme araçları için v 14.20 ATL (ARM64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ATL. ARM64. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.20 ATL (ARM64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. ATL. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.20 ATL (x86 & x64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. CLı. support | C++V142 derleme araçları için/CLı desteği (14,20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. MFC | C++v142 derleme araçları için v 14.20 MFC (x86 & x64) | 16.2.29003.222
Microsoft. VisualStudio. Component. VC. 14.20. MFC. ARM | C++v142 derleme araçları için v 14.20 MFC (ARM) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. MFC. ARM. Spectre | C++Spectre azaltmaları (ARM) ile v142 derleme araçları için v 14.20 MFC | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. MFC. ARM64 | C++v142 derleme araçları için v 14.20 MFC (ARM64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. MFC. ARM64. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.20 MFC (ARM64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. MFC. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.20 MFC (x86 & x64) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. x86. x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.20. x86. x64. Spectre | MSVC v142-VS 2019 C++ x64/x86 Spectre-azaltılan LIBS (v 14.20) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. 14.21. ARM | MSVC v142-VS 2019 C++ ARM derleme araçları (v 14.21) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ARM. Spectre | MSVC v142-VS 2019 C++ ARM Spectre-azaltılan LIBS (v 14.21) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ARM64 | MSVC v142-VS 2019 C++ ARM64 derleme araçları (v 14.21) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ARM64. Spectre | MSVC v142-VS 2019 C++ ARM64 Spectre-azaltılan LIBS (v 14.21) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ATL | C++v142 derleme araçları için v 14.21 ATL (x86 & x64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ATL. ARM | C++v142 derleme araçları için v 14.21 ATL (ARM) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ATL. ARM. Spectre | C++Spectre azaltmaları (ARM) ile v142 derleme araçları için v 14.21 ATL | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ATL. ARM64 | C++v142 derleme araçları için v 14.21 ATL (ARM64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ATL. ARM64. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.21 ATL (ARM64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. ATL. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.21 ATL (x86 & x64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. CLı. support | C++V142 derleme araçları için/CLı desteği (14,21) | 16.2.29012.281
Microsoft. VisualStudio. Component. VC. 14.21. MFC | C++v142 derleme araçları için v 14.21 MFC (x86 & x64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. MFC. ARM | C++v142 derleme araçları için v 14.21 MFC (ARM) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. MFC. ARM. Spectre | C++Spectre azaltmaları (ARM) ile v142 derleme araçları için v 14.21 MFC | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. MFC. ARM64 | C++v142 derleme araçları için v 14.21 MFC (ARM64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. MFC. ARM64. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.21 MFC (ARM64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. MFC. Spectre | C++Spectre azaltmaları ile v142 derleme araçları için v 14.21 MFC (x86 & x64) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. x86. x64 | MSVC v142-VS 2019 C++ x64/x86 derleme araçları (v 14.21) | 16.2.29019.55
Microsoft. VisualStudio. Component. VC. 14.21. x86. x64. Spectre | MSVC v142-VS 2019 C++ x64/x86 Spectre-azaltılan LIBS (v 14.21) | 16.2.29019.55
Microsoft.VisualStudio.Component.VC.ATL.ARM | C++V142 için ATL derleme araçları (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM.Spectre | C++Spectre azaltmaları ile v142 derleme araçları için ATL (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM64 | C++V142 derleme araçları için ATL (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM64.Spectre | C++Spectre azaltmaları ile v142 derleme araçları için ATL (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.Spectre | C++Spectre azaltmaları ile v142 derleme araçları için ATL (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATLMFC.Spectre | C++Spectre azaltmaları ile v142 derleme araçları için MFC (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM | C++V142 derleme araçları (ARM) için MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM.Spectre | C++Spectre azaltmaları ile v142 derleme araçları için MFC (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM64 | C++V142 derleme araçları için MFC (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM64.Spectre | C++Spectre azaltmaları ile v142 derleme araçları için MFC (ARM64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. Redist. MSM | C++2019 yeniden dağıtılabilir MSMs | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.ARM.Spectre | MSVC v142-VS 2019 C++ ARM Spectre-azaltılan LIBS (v 14.22) | 16.2.29003.222
Microsoft.VisualStudio.Component.VC.Runtimes.ARM64.Spectre | MSVC v142-VS 2019 C++ ARM64 Spectre-azaltılan LIBS (v 14.22) | 16.2.29003.222
Microsoft.VisualStudio.Component.VC.Runtimes.x86.x64.Spectre | MSVC v142-VS 2019 C++ x64/x86 Spectre-azaltılan LIBS (v 14.22)  | 16.2.29003.222
Microsoft. VisualStudio. Component. VC. v141. ARM. Spectre | MSVC v141-VS 2017 C++ ARM Spectre-azaltılan LIBS (v 14.16) | 16.1.28829.92
Microsoft. VisualStudio. Component. VC. v141. ARM64. Spectre | MSVC v141-VS 2017 C++ ARM64 Spectre-azaltılan LIBS (v 14.16) | 16.1.28829.92
Microsoft.VisualStudio.Component.VC.v141.ATL | C++V141 için ATL derleme araçları (x86 & x64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. ATL. ARM | C++V141 için ATL derleme araçları (ARM) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. ATL. ARM. Spectre | C++Spectre azaltmaları ile v141 derleme araçları için ATL (ARM) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. ATL. ARM64 | C++V141 derleme araçları için ATL (ARM64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. ATL. ARM64. Spectre | C++Spectre azaltmaları ile v141 derleme araçları için ATL (ARM64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. ATL. Spectre | C++Spectre azaltmaları ile v141 derleme araçları için ATL (x86 & x64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. CLı. support | C++V141 derleme araçları için/CLı desteği (14,16) | 16.1.28829.92
Microsoft.VisualStudio.Component.VC.v141.MFC | C++V141 derleme araçları için MFC (x86 & x64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM | C++V141 derleme araçları (ARM) için MFC | 16.2.28915.88
Microsoft. VisualStudio. Component. VC. v141. MFC. ARM. Spectre | C++Spectre azaltmaları ile v141 derleme araçları için MFC (ARM) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM64 | C++V141 derleme araçları için MFC (ARM64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. MFC. ARM64. Spectre | C++Spectre azaltmaları ile v141 derleme araçları için MFC (ARM64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. MFC. Spectre | C++Spectre azaltmaları ile v141 derleme araçları için MFC (x86 & x64) | 16.0.28625.61
Microsoft. VisualStudio. Component. VC. v141. x86. x64. Spectre | MSVC v141-VS 2017 C++ x64/x86 Spectre-azaltılan LIBS (v 14.16) | 16.1.28829.92
Microsoft.VisualStudio.Component.VisualStudioData | Veri kaynakları ve hizmet başvuruları | 16.0.28707.177
Microsoft.VisualStudio.Component.WinXP | C++VS 2017 (v141) araçları için Windows XP desteği [kullanım dışı] | 16.1.28811.260
Microsoft.VisualStudio.Web.Mvc4.ComponentGroup | ASP.NET MVC 4 | 16.1.28810.153
