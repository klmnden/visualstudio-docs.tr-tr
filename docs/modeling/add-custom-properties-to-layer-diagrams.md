---
title: Bağımlılık diyagramlarına özel özellikler ekleme
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- dependency diagrams, adding custom properties
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 0c4639b5e2edcfebd05dcc6511102c0369b4b3e1
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60066097"
---
# <a name="add-custom-properties-to-dependency-diagrams"></a>Bağımlılık diyagramlarına özel özellikler ekleme

Bağımlılık diyagramları için uzantı kodu yazdığınızda, herhangi bir öğeyle değerleri bir bağımlılık diyagramında saklayabilirsiniz. Diyagram kaydedildiğinde ve yeniden açıldığında, değerler kalır. Bu özellikler görünür bulundurabilirsiniz **özellikleri** penceresi böylece kullanıcıların görebilmesi ve düzenleyebilmesi. Örneğin, kullanıcıların her katman için normal bir ifade belirtin ve her katmanda sınıfların adlarını, kullanıcı tarafından belirtilen düzene uyan doğrulamak için doğrulama kodu yazmasına izin verebilirsiniz.

## <a name="non-visible-properties"></a>Görünür olmayan özellikleri

Yalnızca kodunuzun değerleri bağımlılık diyagramında herhangi bir öğe eklemeye istiyorsanız, bir MEF Bileşeni tanımlamanız gerekmez. Adlı bir sözlük var. `Properties` içinde <xref:Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer.ILayerElement>. Herhangi bir katman öğenin sözlüğe sıralanabilecek değerler eklemeniz yeterlidir. Bağımlılık diyagramın bir parçası olarak kaydedilir.

## <a name="editable-properties"></a>Düzenlenebilir özellikler

**İlk Hazırlık**

> [!IMPORTANT]
> Özellikleri görünür yapmak için katman özellikleri görünür olmasını istediğiniz her bilgisayarda aşağıdaki değişikliği yapın:
>
> 1. Kullanarak Not Defteri'ni çalıştırma **yönetici olarak çalıştır**. Açık *%ProgramFiles%\Microsoft Visual Studio [sürüm] \Common7\IDE\Extensions\Microsoft\Architecture Tools\ExtensibilityRuntime\extension.vsixmanifest*.
> 2. İçinde **içerik** öğesini ekleyin:
>
>     ```xml
>     <MefComponent>Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer.Provider.dll</MefComponent>
>     ```
>
> 3. Altında **Visual Studio Araçları** Visual Studio uygulama başlangıç menüsünde, açık bir bölümünü **Geliştirici komut istemi**. Girin:
>
>      `devenv /rootSuffix /updateConfiguration`
>
>      `devenv /rootSuffix Exp /updateConfiguration`
> 4. Visual Studio'yu yeniden başlatın.

**Kodunuzun bir VSIX projesinde olduğundan emin olun**

Özelliğiniz komutun, hareket ya da doğrulama projesi parçasıysa, hiçbir şey eklemenize gerek yoktur. Özel özelliğinizin kodu, bir MEF Bileşeni olarak tanımlanmış bir Visual Studio genişletilebilirlik projesinde tanımlanmalıdır. Daha fazla bilgi için [bağımlılık diyagramlarına komut ve hareket ekleme](../modeling/add-commands-and-gestures-to-layer-diagrams.md) veya [bağımlılık diyagramlarına özel mimari doğrulaması ekleme](../modeling/add-custom-architecture-validation-to-layer-diagrams.md).

**Özel özelliği tanımla**

Özel bir özellik oluşturmak için şunun gibi bir sınıf tanımlayın:

```csharp
[Export(typeof(IPropertyExtension))]
public class MyProperty : PropertyExtension<ILayerElement>
{
  // Implement the interface.
}
```

Özellikleri tanımlayabilirsiniz <xref:Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer.ILayerElement> veya içeren, ondan türetilen sınıflardan biri:

- `ILayerModel` -model

- `ILayer` -her katman

- `ILayerDependencyLink` -Katmanlar arasında bağlantılar

- `ILayerComment`

- `ILayerCommentLink`

## <a name="example"></a>Örnek

Aşağıdaki kod tipik bir özel özellik tanımlayıcısıdır. Katman modelinde bir Boolean özelliği tanımlar (`ILayerModel`) olanak tanıyan kullanıcının özel doğrulama yöntemi için değerler sağlayın.

```csharp
using System;
using System.ComponentModel.Composition;
using Microsoft.VisualStudio.ArchitectureTools.Extensibility.Layer;

namespace MyNamespace
{
  /// <summary>
  /// Custom properties are added to the Layer Designer via a custom
  /// Property Descriptor. We have to export this Property Descriptor
  /// using MEF to make it available in the Layer Designer.
  /// </summary>
  [Export(typeof(IPropertyExtension))]
  public class AllTypesMustBeReferencedProperty
      : PropertyExtension<ILayerModel>
  {
    /// <summary>
    /// Each custom property must have a unique name.
    /// Usually we use the full name of this class.
    /// </summary>
    public static readonly string FullName =
      typeof(AllTypesMustBeReferencedProperty).FullName;

    /// <summary>
    /// Construct the property. Notice the use of FullName.
    /// </summary>
    public AllTypesMustBeReferencedProperty()
            : base(FullName)
    {  }

    /// <summary>
    /// The display name is shown in the Properties window.
    /// We therefore use a localizable resource.
    /// </summary>
    public override string DisplayName
    {
      get { return Strings.AllTypesMustBeReferencedDisplayName; }
    }

    /// <summary>
    /// Description shown at the bottom of the Properties window.
    /// We use a resource string for easier localization.
    /// </summary>
    public override string Description
    {
      get { return Strings.AllTypesMustBeReferencedDescription; }
    }

    /// <summary>
    /// This is called to set a new value for this property. We must
    /// throw an exception if the value is invalid.
    /// </summary>
    /// <param name="component">The target ILayerElement</param>
    /// <param name="value">The new value</param>
    public override void SetValue(object component, object value)
    {
      ValidateValue(value);
      base.SetValue(component, value);
    }
    /// <summary>
    /// Helper to validate the value.
    /// </summary>
    /// <param name="value">The value to validate</param>
    private static void ValidateValue(object value)
    {  }

    public override Type PropertyType
    { get { return typeof(bool); } }

    /// <summary>
    /// The segment label of the properties window.
    /// </summary>
    public override string Category
    {
      get
      {
        return Strings.AllTypesMustBeReferencedCategory;
      }
    }
  }
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Bağımlılık diyagramlarını genişletme](../modeling/extend-layer-diagrams.md)
