---
title: Ayarlar şelalesi | Microsoft Intellitest Geliştirici Test aracı
ms.date: 05/02/2017
ms.prod: visual-studio-dev15
ms.topic: conceptual
helpviewer_keywords:
- IntelliTest, Settings waterfall
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
author: gewarren
ms.openlocfilehash: 5371900ec439a0d8c736d5437316705b6bfb98cb
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54934523"
---
# <a name="settings-waterfall"></a>Ayarlar şelalesi

Kullanıcı ayarlarını belirtebilir ayarlar şelalesi kavramını anlamına gelir **derleme**, **düzeni**, ve **araştırma** düzeyi:

* Derleme - [PexAssemblySettings](attribute-glossary.md#pexassemblysettings)
* Düzeni - [PexClass](attribute-glossary.md#pexclass)
* Araştırma - [PexExplorationAttributeBase](attribute-glossary.md#pexexplorationattributebase)

Belirtilen ayarlar **derleme** tüm armatürleri ve araştırma altında bu derleme düzeyi etkiler. Belirtilen ayarlar **düzeni** düzeyi bu düzeni altındaki tüm araştırmaları etkiler. Alt ayarları win&mdash;konumundaki bir ayarı tanımlanmışsa **derleme** ve **düzeni** düzeylerini **düzeni** ayarları kullanılır.

Bazı ayarlar özel olduğunu unutmayın **derleme** düzeyi veya **düzeni** düzeyi.

**Örnek**

```csharp
using Microsoft.Pex.Framework;

[assembly: PexAssemblySettings(MaxBranches = 1000)] // we override the default value of maxbranches

namespace MyTests
{
    [PexClass(MaxBranches = 500)] // we override the 1000 value and set maxbranches to 500
    public partial class MyTests
    {
        [PexMethod(MaxBranches = 100)] // we override again, maxbranches = 100
        public void MyTest(...) { ... }
    }
}
```

## <a name="got-feedback"></a>Geri bildirim var mı?

Fikirlerinizi gönderin ve özellik istekleri [Geliştirici topluluğu](https://developercommunity.visualstudio.com/content/idea/post.html?space=8).