---
title: Bir metin şablonundan Visual Studio 2015 veya diğer Konaklara erişme | Microsoft Docs
titleSuffix: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: a68886da-7416-4785-8145-3796bb382cba
caps.latest.revision: 7
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: 053e8b09fd2b52683238f1ffe008e5e7d38b3962
ms.sourcegitcommit: 2da366ba9ad124366f6502927ecc720985fc2f9e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68872015"
---
# <a name="accessing-visual-studio-or-other-hosts-from-a-text-template"></a>Metin Şablonundan Visual Studio'ya veya diğer Konaklara Erişme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Metin şablonunda, yöntemleri ve şablon gibi yürüten bir ana bilgisayar tarafından kullanıma sunulan özellikler kullanabilirsiniz [!INCLUDE[vsprvs](../includes/vsprvs-md.md)].

 Bu değil önceden işlenmiş metin şablonlarını normal metin şablonları için geçerlidir.

## <a name="obtaining-access-to-the-host"></a>Konağa erişim elde etme

Ayarlama `hostspecific="true"` içinde `template` yönergesi. Bu, [ITextTemplatingEngineHost](/previous-versions/visualstudio/visual-studio-2012/bb126505(v=vs.110))türünde `this.Host`bir kullanmanıza olanak sağlar. Bu tür, örneğin, dosya adlarını çözümleme ve hataları günlüğe kaydetmek için kullanabileceğiniz üyeleri var.

### <a name="resolving-file-names"></a>Dosya adları çözme
 Metin şablonu göreli bir dosyanın tam yolunu bulmak için bunu kullanın. Host.ResolvePath().

```csharp
<#@ template hostspecific="true" language="C#" #>
<#@ output extension=".txt" #>
<#@ import namespace="System.IO" #>
<#
 // Find a path within the same project as the text template:
 string myFile = File.ReadAllText(this.Host.ResolvePath("MyFile.txt"));
#>
Content of myFile is:
<#= myFile #>

```

### <a name="displaying-error-messages"></a>Hata iletilerini görüntüleme
 Bu örnekte, şablon dönüştürdüğünüzde iletileri günlüğe kaydeder. Ana bilgisayar ise [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], hata penceresine eklenir.

```csharp
<#@ template hostspecific="true" language="C#" #>
<#@ output extension=".txt" #>
<#@ import namespace="System.CodeDom.Compiler" #>
<#
  string message = "test message";
  this.Host.LogErrors(new CompilerErrorCollection()
    { new CompilerError(
       this.Host.TemplateFile, // Identify the source of the error.
       0, 0, "0",   // Line, column, error ID.
       message) }); // Message displayed in error window.
#>

```

## <a name="using-the-visual-studio-api"></a>Visual Studio API kullanma
 Metin şablonunda çalıştırıldığında [!INCLUDE[vsprvs](../includes/vsprvs-md.md)], kullanabileceğiniz `this.Host` Erişim Hizmetleri tarafından sağlanan [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] ve paketleri veya yüklenen uzantıları.

 Ayarlama hostspecific = "true" ve dönüştürme `this.Host` için <xref:System.IServiceProvider>.

 Bu örnekte [!INCLUDE[vsprvs](../includes/vsprvs-md.md)] API <xref:EnvDTE.DTE>, hizmet olarak:

```csharp
<#@ template hostspecific="true" language="C#" #>
<#@ output extension=".txt" #>
<#@ assembly name="EnvDTE" #>
<#@ import namespace="EnvDTE" #>
<#
 IServiceProvider serviceProvider = (IServiceProvider)this.Host;
 DTE dte = serviceProvider.GetService(typeof(DTE)) as DTE;
#>
Number of projects in this solution: <#=  dte.Solution.Projects.Count #>

```

## <a name="using-hostspecific-with-template-inheritance"></a>Şablon kalıtım hostSpecific kullanma
 Belirtin `hostspecific="trueFromBase"` da kullanıyorsanız `inherits` özniteliği ve belirten bir şablondan devralıyorsanız `hostspecific="true"`. Bu bir derleyici uyarısı etkisine önler, özellik `Host` iki kez bildirilmiş.
