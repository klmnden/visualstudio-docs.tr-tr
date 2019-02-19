---
title: Yerelleştirme için bağımsız kaynak dilleri | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
- localization [Visual Studio], resources
- NeutralResourcesLanguageAttribute class
- globalization [Visual Studio], resources
- resources [Visual Studio], fallback system
- culture, locating resources
- neutral resources
ms.assetid: ef064995-3b84-4698-a708-9689b7723533
caps.latest.revision: 9
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: da39ed9373daaa1dbef21ad36931ce97ea1f1e1b
ms.sourcegitcommit: a83c60bb00bf95e6bea037f0e1b9696c64deda3c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "54764779"
---
# <a name="neutral-resources-languages-for-localization"></a>Yerelleştirme İçin Bağımsız Kaynak Dilleri
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

<xref:System.Resources.NeutralResourcesLanguageAttribute> Sınıfı ana derlemede bulunan kaynakların kültürü belirtir. Bu öznitelik bir performans geliştirmesi kullanılır. böylece <xref:System.Resources.ResourceManager> nesne ana derlemede bulunan kaynaklar için arama yapmaz.  
  
 Aşağıdaki kod bağımsız kaynaklar dilinin nasıl ayarlanacağını gösterir. Kod, derleme betiğindeki veya AssemblyInfo.vb veya AssemblyInfo.cs dosyasında yerleştirilebilir.  
  
```vb  
' Set neutral resources language for assembly.  
<Assembly: NeutralResourcesLanguageAttribute("en")>  
  
```  
  
```csharp  
// Set neutral resources language for assembly.  
[assembly: NeutralResourcesLanguageAttribute("en")]  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 <xref:System.Resources.ResourceManager>   
 [.NET Framework tabanlı Uluslararası uygulamalara giriş](../ide/introduction-to-international-applications-based-on-the-dotnet-framework.md)   
 [Yerelleştirme için kaynakların hiyerarşik organizasyonu](../ide/hierarchical-organization-of-resources-for-localization.md)   
 [Uygulamaları yerelleştirme](../ide/localizing-applications.md)   
 [Uygulamaları Genelleştirme ve Yerelleştirme](../ide/globalizing-and-localizing-applications.md)
