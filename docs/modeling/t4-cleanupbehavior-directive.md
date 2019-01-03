---
title: T4 CleanUpBehavior yönergesi
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: f99cece37b37cdbf4906e9af3939fe824aec0a93
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53912827"
---
# <a name="t4-cleanupbehavior-directive"></a>T4 CleanUpBehavior yönergesi

Bir metin şablonunu işledikten sonra appDomain öğesini silmek için aşağıdaki satırı ekleyin:

```
<#@ CleanupBehavior processor="T4VSHost" CleanupAfterProcessingtemplate="true" #>
```

Metin şablonları, ana bilgisayar işleminden ayrı bir appDomain içinde işlenir. Çoğu durumda, bir metin şablonu işlenirken, appdomain, bir sonraki şablonu işlemek için tekrar kullanılır. Ancak, CleanupBehavior belirtirseniz, appDomain silinir ve sonraki şablon yeni bir appDomain içinde işlenir.

Bu metin işlemeyi yavaşlatır, ancak kaynakların kaldırıldıklarından emin olmak için yararlı olabilir.

Bu yönerge yalnızca Visual Studio ana bilgisayarında çalışır.