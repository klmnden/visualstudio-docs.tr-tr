---
title: Modeli Yansıtacak Şekilleri ve Bağlayıcıları Güncelleştirme
ms.date: 11/04/2016
ms.topic: conceptual
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5b4c0c88e9e096836e32ce427ff78cc94f5d1f72
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62906995"
---
# <a name="update-shapes-and-connectors-to-reflect-the-model"></a>Şekilleri ve Bağlayıcıları Modeli Yansıtacak Şekilde Güncelleştirin

Visual Studio'da bir etki alanına özgü dil temel alınan modelin durumunu yansıtacak bir şekil görünümünü yapabilirsiniz.

Bu konudaki kod örnekleri eklenmesi gereken bir `.cs` dosyası, `Dsl` proje. Bu deyimler her dosyaya ihtiyacınız vardır:

```csharp
using Microsoft.VisualStudio.Modeling;
using Microsoft.VisualStudio.Modeling.Diagrams;
```

## <a name="set-shape-map-properties-to-control-the-visibility-of-a-decorator"></a>Bir dekoratörün görünürlüğünü denetleme için Şekil eşlemesi özelliklerini ayarlama

DSL tanımındaki şekil ile alan sınıfı arasındaki eşlemeyi yapılandırarak, program kodu yazmaya gerek kalmadan bir dekoratörün görünürlüğünü denetleyebilir. Daha fazla bilgi için [etki alanına özgü bir dili tanımlama nasıl](../modeling/how-to-define-a-domain-specific-language.md).

## <a name="expose-the-color-and-style-of-a-shape-as-properties"></a>Rengini ve stilini şeklinin özellik olarak kullanıma sunar.

DSL tanımındaki şekil sınıfı sağ tıklatın, **ekleme kullanıma sunulan**ve öğelerden birini gibi ardından **dolgu rengi**.

Şekil, program kodu veya bir kullanıcı olarak ayarlanmış bir alan özelliği artık sahiptir. Örneğin, bir komut veya kuralın program kodu içinde ayarlamak için şunu yazabilirsiniz:

`shape.FillColor = System.Drawing.Color.Red;`

Özellik değişkeni yalnızca, program denetimi altında ve kullanıcı tarafından hale getirmek isterseniz, yeni etki alanı özelliği gibi seçin **dolgu rengi** DSL tanım diyagramı içinde. Ardından, Özellikler penceresinde ayarlayın **olan gözatılabilir** için `false` veya **kullanıcı Arabirimi salt okunur olduğundan** için `true`.

## <a name="define-change-rules-to-make-color-style-or-location-depend-on-model-element-properties"></a>Değişiklik renk, stil veya model öğesi özelliklerine bağlıdır konumu yapmak üzere kurallar tanımlayın
 Görünüm modeli diğer kısımlarına bağımlı şekli güncelleştiren kurallar tanımlayabilirsiniz. Örneğin, şeklini model öğesinin özellikleri bağımlı rengini güncelleştiren bir model öğesi üzerinde değişiklik kural tanımlayabilirsiniz. Değişiklik kuralları hakkında daha fazla bilgi için bkz. [kuralları yaymak değişiklikleri içinde modeli](../modeling/rules-propagate-changes-within-the-model.md).

 Undo komutu gerçekleştirildiğinde kuralları çağrılmaz çünkü yalnızca Store içinde tutulan özelliklerini güncelleştirmek için kural kullanmanız gerekir. Bu şeklin görünürlüğünü ve boyutu gibi bazı grafik özellikleri içermez. Bir şeklin bu özellikleri güncelleştirmek için bkz. [olmayan Store grafik güncelleştirme özelliklerini](#OnAssociatedProperty).

 Aşağıdaki örnek, oluşturduğunuz varsayılır `FillColor` önceki bölümde açıklandığı gibi bir alan özelliği olarak.

```csharp
[RuleOn(typeof(ExampleElement))]
  class ExampleElementPropertyRule : ChangeRule
  {
    public override void ElementPropertyChanged(ElementPropertyChangedEventArgs e)
    {
      base.ElementPropertyChanged(e);
      ExampleElement element = e.ModelElement as ExampleElement;
      // The rule is called for every property that is updated.
      // Therefore, verify which property changed:
      if (e.DomainProperty.Id == ExampleElement.NameDomainPropertyId)
      {
        // There is usually only one shape:
        foreach (PresentationElement pel in PresentationViewsSubject.GetPresentation(element))
        {
          ExampleShape shape = pel as ExampleShape;
          // Replace this with a useful condition:
          shape.FillColor = element.Name.EndsWith("3")
                     ? System.Drawing.Color.Red : System.Drawing.Color.Green;
        }
      }
    }
  }
  // The rule must be registered:
  public partial class OnAssociatedPropertyExptDomainModel
  {
    protected override Type[] GetCustomDomainModelTypes()
    {
      List<Type> types = new List<Type>(base.GetCustomDomainModelTypes());
      types.Add(typeof(ExampleElementPropertyRule));
      // If you add more rules, list them here.
      return types.ToArray();
    }
  }
```

## <a name="use-onchildconfigured-to-initialize-a-shapes-properties"></a>Bir şeklin özellikleri başlatmak için OnChildConfigured kullanın

İlk çalıştırıldığında bir Şekil özelliklerini ayarlamak için oluşturulan, geçersiz kılma `OnChildConfigured()` diyagram sınıfınızın bir kısmi tanımı. Diyagram sınıfı, DSL tanımındaki belirtilir ve oluşturulan kodu **Dsl\Generated Code\Diagram.cs**. Örneğin:

```csharp
partial class MyLanguageDiagram
{
  protected override void OnChildConfigured(ShapeElement child, bool childWasPlaced, bool createdDuringViewFixup)
  {
    base.OnChildConfigured(child, childWasPlaced, createdDuringViewFixup);
    ExampleShape shape = child as ExampleShape;
    if (shape != null)
    {
      if (!createdDuringViewFixup) return; // Ignore load from file.
      ExampleElement element = shape.ModelElement as ExampleElement;
      // Replace with a useful condition:
      shape.FillColor = element.Name.EndsWith("3")
          ? System.Drawing.Color.Red : System.Drawing.Color.Green;
    }
    // else deal with other types of shapes and connectors.
  }
}
```

Bu yöntem, hem de etki alanı özellikleri ve şekli boyutu gibi mağaza içi özellikler için kullanılabilir.

## <a name="OnAssociatedProperty"></a> Diğer Şekil özelliklerini güncelleştirmek için AssociateValueWith() kullanın

Şeklin gölge ya da bir bağlayıcının Ok Stili sahip olup olmadığı gibi bazı özellikler için özellik bir alan özelliği olarak gösterme, yerleşik bir yöntem yoktur.  Değişiklikler gibi özellikler için hareket sistemi denetiminde değildir. Bu nedenle, bunları güncelleştirmek uygun değil Kullanıcı Geri Al komutu gerçekleştirdiğinde kuralları çağrılmaz çünkü kurallarını kullanarak.

Bunun yerine, kullanarak gibi özellikleri güncelleştirebilirsiniz <xref:Microsoft.VisualStudio.Modeling.Diagrams.ShapeElement.OnAssociatedPropertyChanged%2A>. Aşağıdaki örnekte, bir bağlayıcının Ok Stili bağlayıcı görüntüler ilişkisinde bir etki alanı özellik değeri tarafından denetlenir:

```csharp
public partial class ArrowConnector // My connector class.
{
    /// <summary>
    /// Called whenever a registered property changes in the associated model element.
    /// </summary>
    /// <param name="e"></param>
    protected override void OnAssociatedPropertyChanged(VisualStudio.Modeling.Diagrams.PropertyChangedEventArgs e)
    {
      base.OnAssociatedPropertyChanged(e);
      // Can be called for any property change. Therefore,
      // Verify that this is the property we're interested in:
      if ("IsDirected".Equals(e.PropertyName))
      {
        if (e.NewValue.Equals(true))
        { // Update the shape's built-in Decorator feature:
          this.DecoratorTo = LinkDecorator.DecoratorEmptyArrow;
        }
        else
        {
          this.DecoratorTo = null; // No arrowhead.
        }
      }
    }

    // OnAssociatedPropertyChanged is called only for properties
    // that have been registered using AssociateValueWith().
    // InitializeResources is a convenient place to call this.
    // This method is invoked only once per class, even though
    // it is an instance method.
    protected override void InitializeResources(StyleSet classStyleSet)
    {
      base.InitializeResources(classStyleSet);
      AssociateValueWith(this.Store, Wire.IsDirectedDomainPropertyId);
      // Add other properties here.
    }
}
```

`AssociateValueWith()` kaydetmek istediğiniz her bir etki alanı özellik için bir kez çağrılmalıdır. Bunu çağrıldıktan sonra belirtilen özellik değişiklikleri çağıracak `OnAssociatedPropertyChanged()` herhangi şekillerde özelliğin model öğesi sunar.

Bu çağrı gerekli değildir `AssociateValueWith()` her örneği için. InitializeResources bir örnek yöntemi olsa da, her şekil sınıf için yalnızca bir kez çağrılır.
