---
title: T4 CleanUpBehavior yönergesi | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: 9e5a211f-a3bf-4229-bff0-7d2e45b71c64
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: f964f37b347d588b1f7e590d918018c50e9f41c0
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68199827"
---
# <a name="t4-cleanupbehavior-directive"></a>T4 CleanUpBehavior yönergesi
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir metin şablonunu işledikten sonra appDomain öğesini silmek için aşağıdaki satırı ekleyin:  
  
```  
<#@ CleanupBehavior processor="T4VSHost" CleanupAfterProcessingtemplate="true" #>  
```  
  
 Metin şablonları, ana bilgisayar işleminden ayrı bir appDomain içinde işlenir. Çoğu durumda, bir metin şablonu işlenirken, appdomain, bir sonraki şablonu işlemek için tekrar kullanılır. Ancak, CleanupBehavior belirtirseniz, appDomain silinir ve sonraki şablon yeni bir appDomain içinde işlenir.  
  
 Bu metin işlemeyi yavaşlatır, ancak kaynakların kaldırıldıklarından emin olmak için yararlı olabilir.  
  
 Bu yönerge yalnızca Visual Studio ana bilgisayarında çalışır.
