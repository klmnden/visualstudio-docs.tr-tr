---
title: Renk, çizgi stili ve diğer Şekil özelliklerini denetleme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-modeling
ms.topic: conceptual
ms.assetid: c06d0066-24aa-4c65-b91c-c2089b81ec8d
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: jillfra
ms.openlocfilehash: cff60ca7fc76563db73c4fc839688e0fba4ab975
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54785993"
---
# <a name="controlling-color-line-style-and-other-shape-properties"></a>Renk, Çizgi Stili ve Diğer Şekil Özelliklerini Denetleme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Renk 'olarak sunulabilir gibi' – bazı Şekil özelliklerini, diğer bir deyişle, şekle bir alan özelliğine bağlı. Başkalarının doğrudan denetlenmesi gerekir.  
  
## <a name="exposing-a-property"></a>Bir özelliği kullanıma sunma  
 Renk gibi bazı Şekil özelliklerini değeri alan özelliği olarak bağlanabilir.  
  
 DSL tanımındaki şekil, bağlayıcı veya diyagram sınıfı seçin. Kendi bağlam menüsünde **ekleme kullanıma sunulan**, istediğiniz gibi dolgu rengi özelliği seçin.  
  
 Şekil, program kodu veya bir kullanıcı olarak ayarlanmış bir alan özelliği artık sahiptir.  
  
## <a name="dynamically-updating-an-exposed-property"></a>Dinamik olarak sunulan bir özellik güncelleştiriliyor  
 Genellikle sunulan özelliği başka bir özellikte bağlı olmanız gerekir. Örneğin, belirli bir etki alanı özelliği olduğunda kırmızıya şekle sıfırdan isteyebilirsiniz. Bu bağımlılık olmak için oluşturun bir [kural](../modeling/rules-propagate-changes-within-the-model.md). Örneğin:  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using Microsoft.VisualStudio.Modeling;  
using Microsoft.VisualStudio.Modeling.Diagrams;  
namespace ExampleNamespace  
{  
 // Attribute associates the rule with class:  
 [RuleOn(typeof(CarShape), FireTime = TimeToFire.TopLevelCommit)]  
 // The rule is a class derived from one of the abstract rules:  
 class CarShapeAddRule : AddRule  
 {  
 // Override the abstract method:  
 public override void ElementAdded(ElementAddedEventArgs e)  
 {  
 base.ElementAdded(e);  
 CarShape shape = e.ModelElement as CarShape;  
 Store store = shape.Store;  
 // Ignore this call if we're currently loading a model:  
 if (store.TransactionManager.CurrentTransaction.IsSerializing)   
  return;  
 Car car = shape.ModelElement as Car;  
 // Code here propagates change as required - for example:  
 shape.FillColor = car.Somebool ? System.Drawing.Color.Red : System.Drawing.Color.Green;   
 }  
}  
 // The rule must be registered:  
 public partial class ExampleDomainModel  
 {  
 protected override Type[] GetCustomDomainModelTypes()  
 {  
  List<Type> types = new List<Type>(base.GetCustomDomainModelTypes());  
  types.Add(typeof(CarShapeAddRule));  
  // If you add more rules, list them here.   
  return types.ToArray();  
 }  
 }  
}  
```
