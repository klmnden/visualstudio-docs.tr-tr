---
title: Yerelleştirme İçin Bağımsız Kaynak Dilleri
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- localization [Visual Studio], resources
- NeutralResourcesLanguageAttribute class
- globalization [Visual Studio], resources
- resources [Visual Studio], fallback system
- culture, locating resources
- neutral resources
ms.assetid: ef064995-3b84-4698-a708-9689b7723533
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c1a671eefae23fb369cd7398efb7589764ebb46f
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55912878"
---
# <a name="neutral-resources-languages-for-localization"></a>Yerelleştirme İçin Bağımsız Kaynak Dilleri

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

## <a name="see-also"></a>Ayrıca bkz.

- <xref:System.Resources.ResourceManager>
- [.NET Framework Tabanlı Uluslararası Uygulamalara Giriş](../ide/introduction-to-international-applications-based-on-the-dotnet-framework.md)
- [Yerelleştirme için Kaynakların Hiyerarşik Organizasyonu](../ide/hierarchical-organization-of-resources-for-localization.md)
- [Uygulamaları Yerelleştirme](../ide/localizing-applications.md)
- [Uygulamaları Genelleştirme ve Yerelleştirme](../ide/globalizing-and-localizing-applications.md)