---
title: T4 CleanUpBehavior yönergesi
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.prod: visual-studio-dev15
ms.openlocfilehash: 55558216efcdf17615996d767614743d12b1880f
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54967884"
---
# <a name="t4-cleanupbehavior-directive"></a>T4 CleanUpBehavior yönergesi

Bir metin şablonunu işledikten sonra appDomain öğesini silmek için aşağıdaki satırı ekleyin:

```
<#@ CleanupBehavior processor="T4VSHost" CleanupAfterProcessingtemplate="true" #>
```

Metin şablonları, ana bilgisayar işleminden ayrı bir appDomain içinde işlenir. Çoğu durumda, bir metin şablonu işlenirken, appdomain, bir sonraki şablonu işlemek için tekrar kullanılır. Ancak, CleanupBehavior belirtirseniz, appDomain silinir ve sonraki şablon yeni bir appDomain içinde işlenir.

Bu metin işlemeyi yavaşlatır, ancak kaynakların kaldırıldıklarından emin olmak için yararlı olabilir.

Bu yönerge yalnızca Visual Studio ana bilgisayarında çalışır.