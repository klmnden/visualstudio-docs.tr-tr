---
title: Renk, Çizgi Stili ve Diğer Şekil Özelliklerini Denetleme
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: d1783ecf3b30207838d93fdb9cda93e3ed7e232c
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55956239"
---
# <a name="controlling-color-line-style-and-other-shape-properties"></a>Renk, Çizgi Stili ve Diğer Şekil Özelliklerini Denetleme

Renk gibi bazı Şekil özelliklerini 'kullanıma sunulabilecek'. Diğer bir deyişle, özellikleri, şekle bir alan özelliğine bağlanabilir. Başkalarının doğrudan denetlenmesi gerekir.

## <a name="exposing-a-property"></a>Bir özelliği kullanıma sunma
 Renk gibi bazı Şekil özelliklerini değeri alan özelliği olarak bağlanabilir.

 DSL tanımındaki şekil, bağlayıcı veya diyagram sınıfı seçin. Kendi sağ tıklama menüsünde **ekleme kullanıma sunulan**, istediğiniz gibi dolgu rengi özelliği seçin.

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