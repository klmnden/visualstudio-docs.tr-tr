---
title: Visual Studio Enterprise 2019 iş yükü ve Bileşen kimlikleri
titleSuffix: ''
description: İş yükü ve Bileşen kimlikleri komut satırını kullanarak Visual Studio'yu yükleyin veya bağımlılık VSIX bildirimi olarak belirtmek için kullanın.
keywords: ''
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.date: 02/29/2019
ms.prod: visual-studio-windows
ms.technology: vs-installation
ms.topic: include
ms.openlocfilehash: 9334472f3886559a60a64911ea137c6994fb3b0c
ms.sourcegitcommit: 11337745c1aaef450fd33e150664656d45fe5bc5
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2019
ms.locfileid: "57326939"
---
## <a name="visual-studio-core-editor-included-with-visual-studio-enterprise-2019"></a>Visual Studio çekirdek Düzenleyicisi (ile Visual Studio Enterprise 2019'da dahildir)

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.CoreEditor

**Açıklama:** Visual Studio söz dizimine duyarlı kod düzenleme, kaynak kodu denetimi de dahil olmak üzere, temel Kabuk deneyimi ve iş öğesi yönetimi.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.CoreEditor | Visual Studio temel Düzenleyicisi | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.StartPageExperiment.Cpp | Visual Studio başlangıç sayfasını C++ kullanıcılar | 16.0.28315.86 | İsteğe Bağlı

## <a name="azure-development"></a>Azure geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.Azure

**Açıklama:** Azure SDK'ları, araçları ve projeleri bulut uygulamaları geliştirmek için kaynakları oluşturmak ve Docker dahil kapsayıcılar oluşturmak destekler.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | Gerekli
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure Web işleri araçları | 16.0.28625.61 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.FSharp.WebTemplates | F#web projeleri için dil desteği | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Azure.Prerequisites | Azure geliştirme önkoşulları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure Web işleri araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake ve Stream Analytics araçları | 16.0.28625.61 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.VisualStudio.Component.AspNet45 | Gelişmiş ASP.NET özellikleri | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Kubernetes.Tools | Kubernetes için Visual Studio Araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ResourceManager.Tools | Azure Resource Manager temel araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Azure.ServiceFabric.Tools | Service Fabric Araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton | Azure Cloud Services temel araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure Cloud Services derleme araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Debugger.Snapshot | Anlık görüntü hata ayıklayıcısı | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Debugger.TimeTravel | Hata ayıklama yardımcı programları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
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
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.Core.Component.SDK.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.Web.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Storage.AzCopy | Azure depolama AzCopy | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | İsteğe Bağlı

## <a name="data-storage-and-processing"></a>Veri depolama ve işleme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.Data

**Açıklama:** Bağlayın, geliştirin ve SQL Server, Azure Data Lake veya Hadoop veri çözümleriyle test.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | Önerilen
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Önerilen
Microsoft.Component.Azure.DataLake.Tools | Azure Data Lake ve Stream Analytics araçları | 16.0.28625.61 | Önerilen
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton | Azure Cloud Services temel araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure Cloud Services derleme araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.FSharp.Desktop | F#Masaüstü dil desteği | 16.0.28315.86 | İsteğe Bağlı

## <a name="data-science-and-analytical-applications"></a>Veri bilimi ve analitik uygulamalar

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.DataScience

**Açıklama:** Diller ve Python dahil olmak üzere veri bilimi uygulamaları oluşturmaya yönelik araçlar ve F#.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.PythonTools | Python dil desteği | 16.0.28625.61 | Önerilen
Microsoft.Component.PythonTools.Minicondax64 | Python, miniconda | 16.0.28625.61 | Önerilen
Microsoft.Component.PythonTools.Web | Python web desteği | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.FSharp.Desktop | F#Masaüstü dil desteği | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Önerilen
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Microsoft.Component.VC.Runtime.UCRTSDK | Windows Evrensel CRT SDK | 16.0.28625.61 | İsteğe Bağlı
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Python yerel geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.140 | MSVC v140 - VS 2015 C++ derleme Araçları (v14.00) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | İsteğe Bağlı

## <a name="net-desktop-development"></a>.NET masaüstü geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.ManagedDesktop

**Açıklama:** WPF, Windows Forms ve konsol uygulamaları kullanarak yapı C#, Visual Basic ve F#.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | .NET masaüstü geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Component.Microsoft.VisualStudio.LiveShare | Canlı Paylaşım - Önizleme | 0.3.1225.0 | Önerilen
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
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.LiveUnitTesting | Live Unit Testing | 16.0.28315.86 | Önerilen
Component.Dotfuscator | PreEmptive koruma - Dotfuscator | 16.0.28528.71 | İsteğe Bağlı
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | İsteğe Bağlı
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.SDK | .NET framework 4.7.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.Core.Component.SDK.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeClone | Kod kopyası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeMap | Kod Haritası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Canlı bağımlılık doğrulama | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.FSharp.Desktop | F#Masaüstü dil desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.GraphDocument | DGML Düzenleyici | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.PortableLibrary | .NET taşınabilir kitaplık targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Mimari ve analiz araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | İsteğe Bağlı

## <a name="game-development-with-unity"></a>Unity ile oyun geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.ManagedGame

**Açıklama:** Güçlü bir platformlar arası geliştirme ortamı olan Unity ile 2B ve 3B oyunlar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Net.Component.3.5.DeveloperTools | .NET framework 3.5 geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Unity | Unity için Visual Studio Araçları | 16.0.28315.86 | Gerekli
Component.UnityEngine.x64 | Unity 2018.3 64 bit Düzenleyici | 16.0.28528.71 | Önerilen
Component.UnityEngine.x86 | Unity 5.6 32 bit Düzenleyici | 16.0.28315.86 | Önerilen

## <a name="linux-development-with-c"></a>C++ ile Linux geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NativeCrossPlat

**Açıklama:** Oluşturun ve bir Linux ortamında çalışan uygulamalarda hata ayıklayın.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.MDD.Linux | C++ Linux geliştirme için | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | Gerekli
Component.Linux.CMake | Linux için C++ CMake araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Component.MDD.Linux.GCC.arm | Katıştırılmış ve IOT geliştirme araçları | 16.0.28625.61 | İsteğe Bağlı

## <a name="desktop-development-with-c"></a>C++ ile masaüstü geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NativeDesktop

**Açıklama:** Microsoft C++ araç takımı, ATL veya MFC kullanarak Windows Masaüstü uygulamaları oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.ClassDesigner | Sınıf Tasarımcısı | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.CodeMap | Kod Haritası | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.GraphDocument | DGML Düzenleyici | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++ 2019 yeniden dağıtılabilir güncelleştirme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Native | C++ için Mimari Araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | Visual C++ temel masaüstü özellikleri | 16.0.28315.86 | Gerekli
Component.Microsoft.VisualStudio.LiveShare | Canlı Paylaşım - Önizleme | 0.3.1225.0 | Önerilen
Microsoft.VisualStudio.Component.Debugger.JustInTime | Just-In-Time hata ayıklayıcı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.ATL | V142 derleme Araçları (x86 & x64) için C++ ATL | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.CMake.Project | Windows için C++ CMake araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.VC.TestAdapterForBoostTest | Boost.Test için test bağdaştırıcısı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.VC.TestAdapterForGoogleTest | Google Test için test bağdaştırıcısı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Component.Incredibuild | IncrediBuild - derleme hızlandırma | 16.0.28528.71 | İsteğe Bağlı
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.2 | İsteğe Bağlı
Microsoft.Component.VC.Runtime.UCRTSDK | Windows Evrensel CRT SDK | 16.0.28625.61 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.140 | MSVC v140 - VS 2015 C++ derleme Araçları (v14.00) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.ATLMFC | V142 derleme Araçları (x86 & x64) için C++ MFC | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CLI.Support | C + +/ CLI desteği v142 için derleme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | C++ modülleri v142 için derleme Araçları (x64/x86 – Deneysel) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.v141.x86.x64 | MSVC v141 – VS 2017 C++ x64/x86 derleme Araçları (v14.16) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | İsteğe Bağlı

## <a name="game-development-with-c"></a>C++ ile oyun geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NativeGame

**Açıklama:** DirectX, Unreal veya Cocos2d tarafından desteklenen profesyonel oyunlar oluşturmak için C++'ın gücünü kullanın.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++ 2019 yeniden dağıtılabilir güncelleştirme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | Önerilen
Component.Android.NDK.R16B | Android NDK (R16B) | 16.0.28625.61 | İsteğe Bağlı
Component.Android.SDK25.Private | Android SDK kurulumu (API düzeyi 25) (C++ ile Mobil Geliştirme için yerel yükleme) | 16.0.28625.61 | İsteğe Bağlı
Component.Ant | Apache Ant (1.9.3) | 1.9.3.8 | İsteğe Bağlı
Component.Cocos | Cocos | 16.0.28315.86 | İsteğe Bağlı
Component.Incredibuild | IncrediBuild - derleme hızlandırma | 16.0.28528.71 | İsteğe Bağlı
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.2 | İsteğe Bağlı
Component.MDD.Android | C++ Android geliştirici araçları | 16.0.28517.75 | İsteğe Bağlı
Component.OpenJDK | OpenJDK (Microsoft Dağıtım) | 16.0.28625.61 | İsteğe Bağlı
Component.Unreal | Unreal Engine yükleyicisi | 16.0.28625.61 | İsteğe Bağlı
Component.Unreal.Android | Unreal engine için Android IDE desteği | 16.0.28625.61 | İsteğe Bağlı
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.VisualStudio.Component.NuGet.BuildTools | NuGet hedefleri ve derleme görevleri | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | İsteğe Bağlı

## <a name="mobile-development-with-c"></a>C++ ile Mobil Geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NativeMobile

**Açıklama:** İOS, Android veya C++ kullanarak Windows için platformlar arası uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Android.SDK25.Private | Android SDK kurulumu (API düzeyi 25) (C++ ile Mobil Geliştirme için yerel yükleme) | 16.0.28625.61 | Gerekli
Component.OpenJDK | OpenJDK (Microsoft Dağıtım) | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | Gerekli
Component.Android.NDK.R16B | Android NDK (R16B) | 16.0.28625.61 | Önerilen
Component.Ant | Apache Ant (1.9.3) | 1.9.3.8 | Önerilen
Component.MDD.Android | C++ Android geliştirici araçları | 16.0.28517.75 | Önerilen
Component.Android.NDK.R16B_3264 | Android NDK (R16B) (32 bit) | 16.0.28625.61 | İsteğe Bağlı
Component.Google.Android.Emulator.API25.Private | Google Android Emulator (API düzeyi 25) (yerel kurulum) | 16.0.28625.61 | İsteğe Bağlı
Component.HAXM.Private | Intel donanım hızlandırılmış yürütme Yöneticisi (HAXM) (yerel kurulum) | 16.0.28528.71 | İsteğe Bağlı
Component.Incredibuild | IncrediBuild - derleme hızlandırma | 16.0.28528.71 | İsteğe Bağlı
Component.IncredibuildMenu | IncrediBuildMenu | 1.5.0.2 | İsteğe Bağlı
Component.MDD.IOS | C++ iOS geliştirici araçları | 16.0.28517.75 | İsteğe Bağlı

## <a name="net-core-cross-platform-development"></a>.NET core platformlar arası geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NetCoreTools

**Açıklama:** .NET Core, ASP.NET Core, HTML/JavaScript ve Docker desteği içeren kapsayıcıları kullanarak platformlar arası uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.FSharp.WebTemplates | F#web projeleri için dil desteği | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Component.Microsoft.VisualStudio.LiveShare | Canlı Paylaşım - Önizleme | 0.3.1225.0 | Önerilen
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure Web işleri araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Debugger.Snapshot | Anlık görüntü hata ayıklayıcısı | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Debugger.TimeTravel | Hata ayıklama yardımcı programları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.LiveUnitTesting | Live Unit Testing | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure Web işleri araçları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Web.CloudTools | Web geliştirme için bulut araçları | 16.0.28621.142 | Önerilen
Microsoft.Net.Core.Component.SDK.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.Web.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Geliştirme zamanı IIS desteği | 16.0.28315.86 | İsteğe Bağlı

## <a name="mobile-development-with-net"></a>.NET ile Mobil Geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NetCrossPlat

**Açıklama:** İOS, Android veya Xamarin kullanarak Windows için platformlar arası uygulamalar oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Xamarin | Xamarin | 16.0.28625.61 | Gerekli
Component.Xamarin.RemotedSimulator | Xamarin uzak simülatör | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.Merq | Ortak Xamarin iç araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.MonoDebugger | Mono hata ayıklayıcısı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions.TemplateEngine | ASP.NET şablon oluşturma altyapısı | 16.0.28315.86 | Gerekli
Component.Android.SDK27 | Android SDK kurulumu (API düzeyi 27) | 16.0.28517.75 | Önerilen
Component.OpenJDK | OpenJDK (Microsoft Dağıtım) | 16.0.28625.61 | Önerilen

## <a name="aspnet-and-web-development"></a>ASP.NET ve web geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.NetWeb

**Açıklama:** ASP.NET, ASP.NET Core, HTML/JavaScript ve Docker desteği içeren kapsayıcıları kullanarak web uygulamaları oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.NetCore.ComponentGroup.Web.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.FSharp | F#dil desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.FSharp.WebTemplates | F#web projeleri için dil desteği | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Component.Microsoft.VisualStudio.LiveShare | Canlı Paylaşım - Önizleme | 0.3.1225.0 | Önerilen
Component.Microsoft.VisualStudio.Web.AzureFunctions | Azure Web işleri araçları | 16.0.28625.61 | Önerilen
Microsoft.Net.Component.4.5.1.TargetingPack | .NET framework 4.5.1 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Önerilen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | .NET framework 4-4.6 geliştirme araçları | 16.0.28516.191 | Önerilen
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.AspNet45 | Gelişmiş ASP.NET özellikleri | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.CloudExplorer | Cloud Explorer | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Debugger.Snapshot | Anlık görüntü hata ayıklayıcısı | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.Debugger.TimeTravel | Hata ayıklama yardımcı programları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.EntityFramework | Entity Framework 6 araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.LiveUnitTesting | Live Unit Testing | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.AzureFunctions | Azure Web işleri araçları | 16.0.28621.142 | Önerilen
Microsoft.VisualStudio.ComponentGroup.Web.CloudTools | Web geliştirme için bulut araçları | 16.0.28621.142 | Önerilen
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.SDK | .NET framework 4.6.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.6.2.TargetingPack | .NET framework 4.6.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.SDK | .NET framework 4.7.1 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.1.TargetingPack | .NET framework 4.7.1 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.SDK | .NET framework 4.7 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.TargetingPack | .NET framework 4.7 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.Core.Component.SDK.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.DevelopmentTools.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.NetCore.ComponentGroup.Web.2.2 | .NET core 2.2 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeClone | Kod kopyası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeMap | Kod Haritası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Canlı bağımlılık doğrulama | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.GraphDocument | DGML Düzenleyici | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.TestTools.WebLoadTest | Web performansı ve yük testi araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.AdditionalWebProjectTemplates | Ek proje şablonları (önceki sürümler) | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Mimari ve analiz araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.IISDevelopment | Geliştirme zamanı IIS desteği | 16.0.28315.86 | İsteğe Bağlı

## <a name="nodejs-development"></a>Node.js geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.Node

**Açıklama:** Zaman uyumsuz olay temelli JavaScript çalışma zamanı olan node.js kullanarak Ölçeklenebilir Ağ uygulamaları oluşturun. 

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Node.Tools | Node.js geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Component.Microsoft.VisualStudio.LiveShare | Canlı Paylaşım - Önizleme | 0.3.1225.0 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | İsteğe Bağlı

## <a name="officesharepoint-development"></a>Office/SharePoint geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.Office

**Açıklama:** Office ve SharePoint eklentileri, SharePoint çözümleri ve kullanarak VSTO eklentileri oluşturma C#, VB ve JavaScript.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | Gerekli
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | Gerekli
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.TargetingPack | .NET framework 4.6.1 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.TargetingPack | .NET framework 4 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.ManagedDesktop.Prerequisites | .NET masaüstü geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Sharepoint.Tools | Visual Studio için Office Geliştirici Araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Wcf.Tooling | Windows Communication Foundation | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.Workflow | Windows Workflow Foundation | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | Gerekli
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
Microsoft.Net.ComponentGroup.4.6.1.DeveloperTools | .NET framework 4.6.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET framework 4.6.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET framework 4.7.1 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET framework 4.7 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.Sharepoint.WIF | Windows Identity Foundation 3.5 | 16.0.28621.142 | İsteğe Bağlı

## <a name="python-development"></a>Python geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.Python

**Açıklama:** Düzenleme, hata ayıklama, etkileşimli geliştirme ve Python için kaynak denetimi.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.PythonTools | Python dil desteği | 16.0.28625.61 | Gerekli
Component.CPython3.x64 | Python 3 64 bit (3.7.2) | 3.7.2 | Önerilen
Component.Microsoft.VisualStudio.LiveShare | Canlı Paylaşım - Önizleme | 0.3.1225.0 | Önerilen
Microsoft.Component.PythonTools.Minicondax64 | Python, miniconda | 16.0.28625.61 | Önerilen
Microsoft.Component.PythonTools.Web | Python web desteği | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.Component.Common.Azure.Tools | Bağlantı ve yayımlama araçları | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.WebDeploy | Web Dağıtımı | 16.0.28517.75 | Önerilen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Önerilen
Component.CPython2.x64 | Python 2 64-bit (2.7.15) | 2.7.15 | İsteğe Bağlı
Component.CPython2.x86 | Python 2 32 bit (2.7.15) | 2.7.15 | İsteğe Bağlı
Component.CPython3.x86 | Python 3 32 bit (3.7.2) | 3.7.2 | İsteğe Bağlı
Component.Microsoft.VisualStudio.RazorExtension | Razor dil Hizmetleri | 16.0.28315.86 | İsteğe Bağlı
Component.Microsoft.Web.LibraryManager | Kitaplık Yöneticisi | 16.0.28315.86 | İsteğe Bağlı
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Component.VC.Runtime.UCRTSDK | Windows Evrensel CRT SDK | 16.0.28625.61 | İsteğe Bağlı
Microsoft.ComponentGroup.PythonTools.NativeDevelopment | Python yerel geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.Net.Component.4.5.2.TargetingPack | .NET framework 4.5.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | İsteğe Bağlı
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.AuthoringTools | Azure yazma araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.ClientLibs | .NET için Azure kitaplıkları | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Compute.Emulator | Azure işlem öykünücüsü | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Storage.Emulator | Azure depolama öykünücüsü | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Waverton | Azure Cloud Services temel araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Azure.Waverton.BuildTools | Azure Cloud Services derleme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DockerTools | Kapsayıcı geliştirme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.IISExpress | IIS Express  | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.ManagedDesktop.Core | Yönetilen masaüstü iş yükü Çekirdeği | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.Component.MSODBC.SQL | SQL Server ODBC sürücüsü | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.MSSQL.CMDLnUtils | SQL Server komut satırı yardımcı programları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.ADAL | SQL ADAL çalışma zamanı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.DataSources | Veri kaynakları için SQL Server desteği | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.SSDT | SQL Server Veri Araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.140 | MSVC v140 - VS 2015 C++ derleme Araçları (v14.00) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.DiagnosticTools | C++ profil oluşturma araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Web | ASP.NET ve web geliştirme araçları | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK | Windows Evrensel C çalışma zamanı | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.Web | ASP.NET ve web geliştirme araçları önkoşulları | 16.0.28621.142 | İsteğe Bağlı

## <a name="universal-windows-platform-development"></a>Evrensel Windows platformu geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.Universal

**Açıklama:** Evrensel Windows platformu uygulamaları oluşturmak C#, VB veya isteğe bağlı olarak C++.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.NetFX.Native | .NET Yerel | 16.0.28315.86 | Gerekli
Microsoft.ComponentGroup.Blend | Visual Studio için Blend | 16.0.28315.86 | Gerekli
Microsoft.Net.Component.4.5.TargetingPack | .NET framework 4.5 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.1.SDK | .NET framework 4.6.1 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Core.Component.SDK.2.1 | .NET core 2.1 geliştirme araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Graphics | Görüntü ve 3B model düzenleyicileri | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.Diagnostics | JavaScript tanılamaları | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.Component.JavaScript.TypeScript | JavaScript ve TypeScript dil desteği | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.SQL.CLR | SQL Server için CLR veri türleri | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.Component.TypeScript.3.3 | 3.3 TypeScript SDK'sı | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Windows10SDK.17763 | Windows 10 SDK (10.0.17763.0) | 16.0.28517.75 | Gerekli
Microsoft.VisualStudio.ComponentGroup.UWP.NetCoreAndStandard | .NET native ve .NET Standard | 16.0.28516.191 | Gerekli
Microsoft.VisualStudio.ComponentGroup.UWP.Support | Evrensel Windows platformu araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.UWP.Xamarin | Xamarin için evrensel Windows platformu araçları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET ve web geliştirme | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | İsteğe Bağlı
Microsoft.Component.VC.Runtime.OSSupport | C++ Evrensel Windows platformu çalışma zamanı için v142 derleme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.ClassDesigner | Sınıf Tasarımcısı | 16.0.28528.71 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeClone | Kod kopyası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeMap | Kod Haritası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Canlı bağımlılık doğrulama | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.GraphDocument | DGML Düzenleyici | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Graphics.Tools | DirectX için grafik hata ayıklayıcı ve GPU | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.UWP.VC.ARM64 | C++ Evrensel Windows platformu v142 derleme Araçları (ARM64) desteği | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | C++ 2019 yeniden dağıtılabilir güncelleştirme | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.ARM | MSVC v142 – VS 2019 C++ ARM derleme araçlarını (v14.20) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | MSVC v142 – VS 2019 C++ ARM64 derleme araçlarını (v14.20) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.v141.ARM | MSVC v141 – VS 2017 C++ ARM derleme araçlarını (v14.16) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.v141.ARM64 | MSVC v141 – VS 2017 C++ ARM64 derleme araçlarını (v14.16) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.v141.x86.x64 | MSVC v141 – VS 2017 C++ x64/x86 derleme Araçları (v14.16) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.16299 | Windows 10 SDK (10.0.16299.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.17134 | Windows 10 SDK (10.0.17134.0) | 16.0.28517.75 | İsteğe Bağlı
Microsoft.VisualStudio.Component.Windows10SDK.IpOverUsb | USB cihaz bağlantısı | 16.0.28320.51 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Mimari ve analiz araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Native | C++ için Mimari Araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Core | Visual C++ temel masaüstü özellikleri | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.UWP.VC | (V142) C++ Evrensel Windows platformu araçları | 16.0.28621.142 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.UWP.VC.v141 | (V141) C++ Evrensel Windows platformu araçları | 16.0.28621.142 | İsteğe Bağlı

## <a name="visual-studio-extension-development"></a>Visual Studio uzantısı geliştirme

**KİMLİĞİ:** Microsoft.VisualStudio.Workload.VisualStudioExtension

**Açıklama:** Visual Studio için yeni komutlar, kod Çözümleyicileri ve araç pencerelerini de dahil olmak üzere, eklentileri ve uzantıları oluşturun.

### <a name="components-included-by-this-workload"></a>Bu iş yükü tarafından bulunan bileşenler

Bileşen kimliği | Ad | Sürüm | Bağımlılık türü
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.6.TargetingPack | .NET framework 4.6 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.SDK | .NET framework 4.7.2 SDK'sı | 16.0.28517.75 | Gerekli
Microsoft.Net.Component.4.7.2.TargetingPack | .NET framework 4.7.2 targeting pack | 16.0.28517.75 | Gerekli
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET framework 4.7.2 geliştirme araçları | 16.0.28516.191 | Gerekli
Microsoft.VisualStudio.Component.NuGet | NuGet Paket Yöneticisi | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.Compiler | C# ve Visual Basic Roslyn derleyicileri | 16.0.28528.71 | Gerekli
Microsoft.VisualStudio.Component.Roslyn.LanguageServices | C# ve Visual Basic | 16.0.28625.61 | Gerekli
Microsoft.VisualStudio.Component.VSSDK | Visual Studio SDK | 16.0.28315.86 | Gerekli
Microsoft.VisualStudio.ComponentGroup.VisualStudioExtension.Prerequisites | Visual Studio uzantı geliştirme önkoşulları | 16.0.28621.142 | Gerekli
Microsoft.VisualStudio.Component.DiagnosticTools | .NET profil oluşturma araçları | 16.0.28625.61 | Önerilen
Microsoft.VisualStudio.Component.IntelliTrace.FrontEnd | IntelliTrace | 16.0.28315.86 | Önerilen
Microsoft.VisualStudio.Component.TextTemplating | Metin şablonu dönüştürme | 16.0.28625.61 | Önerilen
Component.Dotfuscator | PreEmptive koruma - Dotfuscator | 16.0.28528.71 | İsteğe Bağlı
Microsoft.Component.CodeAnalysis.SDK | .NET Compiler Platform SDK’sı | 16.0.28625.61 | İsteğe Bağlı
Microsoft.Component.VC.Runtime.OSSupport | C++ Evrensel Windows platformu çalışma zamanı için v142 derleme araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.AppInsights.Tools | Geliştirici analiz araçları | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.ClassDesigner | Sınıf Tasarımcısı | 16.0.28528.71 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeClone | Kod kopyası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.CodeMap | Kod Haritası | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DependencyValidation.Enterprise | Canlı bağımlılık doğrulama | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.DslTools | Modelleme SDK'sı | 16.0.28315.86 | İsteğe Bağlı
Microsoft.VisualStudio.Component.GraphDocument | DGML Düzenleyici | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.SQL.LocalDB.Runtime | SQL Server Express 2016 LocalDB | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.ATL | V142 derleme Araçları (x86 & x64) için C++ ATL | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.ATLMFC | V142 derleme Araçları (x86 & x64) için C++ MFC | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.CoreIde | C++ temel özellikler | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | MSVC v142 – VS 2019 C++ x64/x86 derleme Araçları (v14.20) | 16.0.28625.61 | İsteğe Bağlı
Microsoft.VisualStudio.ComponentGroup.ArchitectureTools.Managed | Mimari ve analiz araçları | 16.0.28621.142 | İsteğe Bağlı

## <a name="unaffiliated-components"></a>Kullanıcıyla bağlantılı olmayan bileşenleri

Bu, her türlü iş yükü ile dahil edilmez, ancak tek bir bileşeni olarak seçilebilir bileşenlerdir.

Bileşen kimliği | Ad | Sürüm
--- | --- | ---
Component.GitHub.VisualStudio | Visual Studio için GitHub uzantısı | 2.5.9.5485
Component.Xamarin.Inspector | Xamarin Inspector | 16.0.28315.86
Component.Xamarin.Profiler | Xamarin Profiler | 16.0.28315.86
Component.Xamarin.Workbooks | Xamarin Workbooks | 16.0.28315.86
Microsoft.Component.HelpViewer | Yardım Görüntüleyicisi | 16.0.28625.61
Microsoft.NetCore.1x.ComponentGroup.Web | Web için .NET core 1.0-1.1 geliştirme araçları | 16.0.28621.142
Microsoft.VisualStudio.Component.AzureDevOps.OfficeIntegration | Azure DevOps Office tümleştirmesi | 16.0.28625.61
Microsoft.VisualStudio.Component.Git | Windows için Git | 16.0.28625.61
Microsoft.VisualStudio.Component.LinqToSql | LINQ to SQL araçları | 16.0.28625.61
Microsoft.VisualStudio.Component.TestTools.CodedUITest | Kodlanmış UI testi | 16.0.28327.66
Microsoft.VisualStudio.Component.VC.ATL.ARM | V142 derleme Araçları (ARM) için C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM.Spectre | V142 derleme araçları için Spectre azaltmaları (ARM) ile C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM64 | V142 derleme Araçları (ARM64) için C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.ARM64.Spectre | C++ ATL v142 için derleme araçlarını Spectre azaltmalarının bulunduğu (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATL.Spectre | Spectre azaltmaları (x86 & x64) ile C++ ATL v142 derleme araçları | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.ATLMFC.Spectre | Spectre azaltmaları (x86 & x64) ile v142 derleme araçları için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM | V142 derleme Araçları (ARM) için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM.Spectre | V142 derleme araçları için Spectre azaltmaları (ARM) ile C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM64 | V142 derleme Araçları (ARM64) için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.MFC.ARM64.Spectre | C++ MFC v142 için derleme araçlarını Spectre azaltmalarının bulunduğu (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Redist.MSM | Yeniden dağıtılabilir C++ 2019 MSMs | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.ARM.Spectre | MSVC v142 – VS 2019 C++ ARM Spectre azaltılabilir kitaplıklar (v14.20) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.ARM64.Spectre | MSVC v142 – VS 2019 C++ ARM64 Spectre azaltılabilir kitaplıklar (v14.20) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.Runtimes.x86.x64.Spectre | MSVC v142 – VS 2019 C++ x64/x86 Spectre azaltılabilir kitaplıklar (v14.20)  | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ARM.Spectre | MSVC v141 – VS 2017 C++ ARM Spectre azaltılabilir kitaplıklar (v14.16) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ARM64.Spectre | MSVC v141 – VS 2017 C++ ARM64 Spectre azaltılabilir kitaplıklar (v14.16) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL | V141 derleme Araçları (x86 & x64) için C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM | V141 derleme Araçları (ARM) için C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM.Spectre | V141 derleme araçları için Spectre azaltmaları (ARM) ile C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM64 | V141 derleme Araçları (ARM64) için C++ ATL | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.ARM64.Spectre | C++ ATL v141 için derleme araçlarını Spectre azaltmalarının bulunduğu (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.ATL.Spectre | Spectre azaltmaları (x86 & x64) ile C++ ATL v141 derleme araçları | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.CLI.Support | C + +/ CLI desteği v141 için derleme araçları | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC | V141 derleme Araçları (x86 & x64) için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM | V141 derleme Araçları (ARM) için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM.Spectre | V141 derleme araçları için Spectre azaltmaları (ARM) ile C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM64 | V141 derleme Araçları (ARM64) için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.ARM64.Spectre | C++ MFC v141 için derleme araçlarını Spectre azaltmalarının bulunduğu (ARM64) | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.MFC.Spectre | Spectre azaltmaları (x86 & x64) ile v141 derleme araçları için C++ MFC | 16.0.28625.61
Microsoft.VisualStudio.Component.VC.v141.x86.x64.Spectre | MSVC v141 – VS 2017 C++ x64/x86 Spectre azaltılabilir kitaplıklar (v14.16) | 16.0.28625.61
Microsoft.VisualStudio.Component.WinXP | VS 2017 (v141) araçları [kullanım dışı] için C++ Windows XP desteği | 16.0.28625.61
Microsoft.VisualStudio.Web.Mvc4.ComponentGroup | ASP.NET MVC 4 | 16.0.28621.142