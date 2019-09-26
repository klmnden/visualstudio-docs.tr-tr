---
title: XAML Tasarımcısı genişletilebilirlik geçişi
ms.date: 07/09/2019
ms.topic: conceptual
author: lutzroeder
ms.author: lutzr
manager: jillfra
dev_langs:
- csharp
- vb
monikerRange: vs-2019
ms.openlocfilehash: 9f5085c7a655f186c3c8a4a6eecada8b440650cd
ms.sourcegitcommit: 528178a304e66c0cb7ab98b493fe3c409f87493a
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71273212"
---
# <a name="xaml-designer-extensibility-migration"></a>XAML Tasarımcısı genişletilebilirlik geçişi

Visual Studio 2019 ' de XAML Tasarımcısı iki farklı mimariyi destekler: tasarımcı yalıtım mimarisi ve daha yeni yüzey yalıtım mimarisi. Bu mimari geçişi, bir .NET Framework işleminde barındırılmayan hedef çalışma zamanlarını desteklemek için gereklidir. Yüzey yalıtım mimarisine geçiş, üçüncü taraf genişletilebilirlik modelinde önemli değişiklikler sunar. Bu makalede, Visual Studio 2019 sürüm 16,3 ' den başlayarak bulunan bu değişiklikler özetlenmektedir.

**Tasarımcı yalıtımı** , .NET Framework hedefleyen ve *. Design. dll* UZANTıLARıNı destekleyen projeler için WPF Tasarımcısı tarafından kullanılır. Kullanıcı kodu, denetim kitaplıkları ve üçüncü taraf uzantıları, gerçek tasarımcı kodu ve tasarımcı panelleriyle birlikte dış bir işleme (*Xdesproc. exe*) yüklenir.

**Surface yalıtım** , UWP Tasarımcısı tarafından kullanılır. Ayrıca, .NET Core ' u hedefleyen projeler için WPF Tasarımcısı tarafından da kullanılır. Yüzey yalıtımında, tasarımcı ve bölmeleri Visual Studio işleminde (*devenv. exe*) yüklenirken yalnızca Kullanıcı kodu ve denetim kitaplıkları ayrı bir işleme yüklenir. Kullanıcı kodu ve denetim kitaplıklarını yürütmek için kullanılan çalışma zamanı, gerçek tasarımcı ve üçüncü taraf genişletilebilirlik kodu için .NET Framework tarafından kullanılan bir farklıdır.

![genişletilebilirlik-geçiş mimarisi](media/xaml-designer-extensibility-migration-architecture.png)

Bu mimari geçişi nedeniyle, üçüncü taraf uzantıları artık üçüncü taraf denetim kitaplıklarıyla aynı işleme yüklenmez. Uzantılar artık denetim kitaplıklarında doğrudan bağımlılıklara sahip olamaz veya çalışma zamanı nesnelerine doğrudan erişemez. *Microsoft. Windows. Extensibility. dll* API 'si kullanılarak tasarımcı yalıtım mimarisi için daha önce yazılmış olan uzantılar, yüzey yalıtım mimarisiyle çalışmak için yeni bir yaklaşıma geçirilmelidir. Uygulamada, mevcut bir uzantının yeni genişletilebilirlik API Derlemeleriyle derlenmesi gerekir. Denetim kitaplıkları artık farklı bir işlemde yüklendiğinden, [typeof](/dotnet/csharp/language-reference/keywords/typeof) veya çalışma zamanı örnekleri aracılığıyla çalışma zamanı denetim türlerine erişim değiştirilmelidir veya kaldırılmalıdır.

## <a name="new-extensibility-api-assemblies"></a>Yeni genişletilebilirlik API derlemeleri

Yeni genişletilebilirlik API derlemeleri var olan genişletilebilirlik API derlemelerine benzerdir, ancak bunları ayırt etmek için farklı bir adlandırma şemasını izler. Benzer şekilde, ad alanı adları yeni derleme adlarını yansıtacak şekilde değiştirilmiştir.

| Tasarımcı yalıtım API derlemesi            | Surface yalıtım API derlemesi                       |
|:------------------------------------------ |:---------------------------------------------------- |
| Microsoft. Windows. Design. Extensibility. dll | Microsoft. VisualStudio. DesignTools. Extensibility. dll |
| Microsoft. Windows. Design. ınterbir. dll   | Microsoft. VisualStudio. DesignTools. ınterbir. dll   |

## <a name="new-file-extension-and-discovery"></a>Yeni dosya uzantısı ve bulma

*. Design. dll* dosya uzantısını kullanmak yerine, *. DesignTools. dll* dosya uzantısı kullanılarak yeni yüzey uzantıları keşfedilir. *. Design. dll* ve *. DesignTools. dll* uzantıları aynı *Tasarım* alt klasöründe bulunabilir.

Gerçek hedef çalışma zamanı (.NET Core veya UWP) için üçüncü taraf denetim kitaplıkları derlenirken, *. DesignTools. dll* uzantısının her zaman .NET Framework bir derleme olarak derlenmesi gerekir.

## <a name="decouple-attribute-tables-from-run-time-types"></a>Çalışma zamanı türlerindeki öznitelik tablolarını ayrıştı

Yüzey yalıtımı genişletilebilirlik modeli, uzantıların gerçek denetim kitaplıklarına bağlı olmasına izin vermez ve bu nedenle uzantılar denetim kitaplığından türlere başvuramaz. Örneğin, *MyLibrary. DesignTools. dll* *MyLibrary. dll*' de bir bağımlılığa sahip olmamalıdır.

Bu tür bağımlılıklar, öznitelik tabloları aracılığıyla türler için meta veriler kaydedilirken en yaygın olarak yapılmıştır. Doğrudan [typeof](/dotnet/csharp/language-reference/keywords/typeof) veya [GetType](/dotnet/visual-basic/language-reference/operators/gettype-operator) aracılığıyla denetim kitaplığı türlerine başvuran uzantı kodu, yeni API 'lerde dize tabanlı tür adları kullanılarak değiştirilir:

```csharp
using Microsoft.VisualStudio.DesignTools.Extensibility.Metadata;
using Microsoft.VisualStudio.DesignTools.Extensibility.Features;
using Microsoft.VisualStudio.DesignTools.Extensibility.Model;

[assembly: ProvideMetadata(typeof(AttributeTableProvider))]

public class AttributeTableProvider : IProvideAttributeTable
{
  public AttributeTable AttributeTable
  {
    get
    {
      var builder = new AttributeTableBuilder();
      builder.AddCustomAttributes("MyLibrary.MyControl", new DescriptionAttribute(Strings.MyControlDescription);
      builder.AddCustomAttributes("MyLibrary.MyControl", new FeatureAttribute(typeof(MyControlDefaultInitializer));
      return builder.CreateTable();
    }
  }
}
```

```vb
Imports Microsoft.VisualStudio.DesignTools.Extensibility.Metadata
Imports Microsoft.VisualStudio.DesignTools.Extensibility.Features
Imports Microsoft.VisualStudio.DesignTools.Extensibility.Model

<Assembly: ProvideMetadata(GetType(AttributeTableProvider))>

Public Class AttributeTableProvider
    Implements IProvideAttributeTable

    Public ReadOnly Property AttributeTable As AttributeTable Implements IProvideAttributeTable.AttributeTable
        Get
            Dim builder As New AttributeTableBuilder
            builder.AddCustomAttributes("MyLibrary.MyControl", New DescriptionAttribute(Strings.MyControlDescription))
            builder.AddCustomAttributes("MyLibrary.MyControl", New FeatureAttribute(GetType(MyControlDefaultInitializer)))
            Return builder.CreateTable()
        End Get
    End Property
End Class
```

## <a name="feature-providers-and-model-api"></a>Özellik sağlayıcıları ve model API 'SI

Özellik sağlayıcıları uzantı Derlemeleriyle uygulanır ve Visual Studio işleminde yüklenir. `FeatureAttribute`, doğrudan [typeof](/dotnet/csharp/language-reference/keywords/typeof)kullanarak özellik sağlayıcısı türlerine başvurmasına devam edecektir.

Şu anda aşağıdaki özellik sağlayıcıları desteklenmektedir:

* `DefaultInitializer`
* `AdornerProvider`
* `ContextMenuProvider`
* `ParentAdapter`
* `PlacementAdapter`
* `DesignModeValueProvider`, tasarımcıda değiştirilmekte olan `TranslatePropertyValue` `InvalidateProperty` veya içinde değiştirildiğinde çağrılacak kısıtlamalarla desteklenir. Çalışma zamanı kodunda değiştirildiğinde çağrılmayacak.

Özellik sağlayıcıları artık gerçek çalışma zamanı kodu ve denetim kitaplıklarından farklı bir işleme yüklendiğinden, artık çalışma zamanı nesnelerine doğrudan erişemeyecektir. Bunun yerine, ilgili model tabanlı API 'Leri kullanmak için tüm etkileşimlerin dönüştürülmesi gerekir. Model API <xref:System.Type> 'si güncelleştirilmiştir ve erişimi <xref:System.Object> artık yok ya da ile `TypeIdentifier` `TypeDefinition`değiştirilmiştir.

`TypeIdentifier`bir türü tanımlayan bütünleştirilmiş kod adı olmayan bir dizeyi temsil eder. , Türüyle ilgili ek bilgileri sorgulamak `TypeDefinition` için bir öğesine çözülebilir. `TypeIdenfifier` `TypeDefinition`örnekler uzantı kodunda önbelleğe alınamaz.

```csharp
TypeDefinition type = ModelFactory.ResolveType(
    item.Context, new TypeIdentifier("MyLibrary.MyControl"));
TypeDefinition buttonType = ModelFactory.ResolveType(
    item.Context, new TypeIdentifier("System.Windows.Controls.Button"));
if (type?.IsSubclassOf(buttonType) == true)
{
}
```

```vb
Dim type As TypeDefinition = ModelFactory.ResolveType(
    item.Context, New TypeIdentifier("MyLibrary.MyControl"))
Dim buttonType As TypeDefinition = ModelFactory.ResolveType(
    item.Context, New TypeIdentifier("System.Windows.Controls.Button"))
If type?.IsSubclassOf(buttonType) Then

End If
```

Surface yalıtım genişletilebilirlik API kümesinden kaldırılan API 'Ler:

* `ModelFactory.CreateItem(EditingContext context, object item)`
* `ViewItem.PlatformObject`
* `ModelProperty.DefaultValue`
* `AssemblyReferences.GetTypes(Type baseType)`

Yerine kullanan `TypeIdentifier` API 'ler: <xref:System.Type>

* `ModelFactory.CreateItem(EditingContext context, Type itemType, params object[] arguments)`
* `ModelFactory.CreateItem(EditingContext context, Type itemType, CreateOptions options, params object[] arguments)`
* `ModelFactory.CreateStaticMemberItem(EditingContext context, Type type, string memberName)`
* `ModelFactory.ResolveType(EditingContext context, Type)`değiştirme`MetadataFactory.ResolveType(EditingContext context, TypeIdentifier typeIdentifier)`
* `ModelService.ResolveType(TypeIdentifier typeIdentifier)`değiştirme`MetadataService.ResolveType(TypeIdentifier typeIdentifier)`
* `ViewItem.ItemType`
* `ModelEvent.EventType`
* `ModelEvent.IsEventOfType(Type type)`
* `ModeItem.IsItemOfType(Type type)`
* `ModelParent.CanParent(EditingContext context, ModelItem parent, Type childType)`
* `ModelParent.FindParent(EditingContext context, Type childType, ModelItem startingItem)`
* `ModelParent.FindParent(Type childType, GestureData gestureData)`
* `ModelProperty.IsPropertyOfType(Type type)`
* `ParentAdpater.CanParent(ModelItem parent, Type childType)`
* `ParentAdapter.RedirectParent(ModelItem parent, Type childType)`

Ve yerine kullanan `TypeIdentifier` API 'ler artık Oluşturucu bağımsız değişkenlerini desteklemez: <xref:System.Type>

* `ModelFactory.CreateItem(EditingContext context, TypeIdentifier typeIdentifier, params object[] arguments)`
* `ModelFactory.CreateItem(EditingContext context, TypeIdentifier typeIdentifier, CreateOptions options, params object[] arguments)`

Yerine kullanan `TypeDefinition` API 'ler: <xref:System.Type>

* `ValueTranslationService.GetProperties(Type itemType)`
* `ValueTranslationService.HasValueTranslation(Type itemType, PropertyIdentifier identifier)`
* `ValueTranslationService.TranslatePropertyValue(Type itemType, ModelItem item, PropertyIdentifier identifier, object value)`
* `ModelService.Find(ModelItem startingItem, Type type)`
* `ModelService.Find(ModelItem startingItem, Predicate<Type> match)`
* `ModelItem.ItemType`
* `ModelProperty.AttachedOwnerType`
* `ModelProperty.PropertyType`
* `FeatureManager.CreateFeatureProviders(Type featureProviderType, Type type)`
* `FeatureManager.CreateFeatureProviders(Type featureProviderType, Type type, Predicate<Type> match)`
* `FeatureManager.InitializeFeatures(Type type)`
* `FeatureManager.GetCustomAttributes(Type type, Type attributeType)`
* `AdapterService.GetAdapter<TAdapterType>(Type itemType)`
* `AdapterService.GetAdapter(Type adapterType, Type itemType)`
* `PropertyEntry.PropertyType`

Yerine kullanan `AssemblyIdentifier` API 'ler: `<xref:System.Reflection.AssemblyName?displayProperty=fullName>`

* `AssemblyReferences.ReferencedAssemblies`
* `AssemblyReferences.LocalAssemblyName`değiştirme`AssemblyReferences.LocalAssemblyIdentifier`

Ayrıca, `ModelItem` gibi `SetValue` API 'ler yalnızca, hedef çalışma zamanı için dönüştürülebilen temel türlerin veya yerleşik .NET Framework türlerinin örneklerini destekler. Şu anda bu türler desteklenir:

* İlkel .NET Framework türleri: `Boolean`, `Byte`, `Char` `DateTime`,, `Double`, ,`Enum` ,`Int16`, ,`Int64`,, `Int32` `Guid` `Nullable` `SByte` , `Single`, `String`, `Type`, `UInt16`, `UInt32`, `UInt64`,`Uri`
* Bilinen WPF .NET Framework türleri (ve türetilmiş türler): `Brush`, `Color`, `CompositeTransform` `CornerRadius`,, `Duration`, `EasingFunctionBase`, `EasingMode`, `EllipseGeometry`, `FontFamily`, `GeneralTransform` ,`Geometry` , `GradientStopCollection`, `GradientStop`, `GridLength`, `ImageSource`, `InlineCollection`, `Inline`, `KeySpline`, `Material`, `Matrix`, `PathFigureCollection`, `PathFigure`, `PathSegmentCollection`, `PathSegment`, `Path`, `PointCollection`, `Point`, `PropertyPath`, `Rect`, `RepeatBehavior`, `Setter`, `Size`, `StaticResource`, `TextAlignment`, `TextDecorationCollection`, `ThemeResourceExtension`, `Thickness`, `TimeSpan`, `Transform3D`,`TransformCollection`

Örneğin:

```csharp
using Microsoft.VisualStudio.DesignTools.Extensibility.Features;
using Microsoft.VisualStudio.DesignTools.Extensibility.Model;

public class MyControlDefaultInitializer : DefaultInitializer
{
  public override void InitializeDefaults(ModelItem item)
  {
    item.Properties["Width"].SetValue(800d);
    base.InitializeDefaults(item);
  }
}
```

```vb
Imports Microsoft.VisualStudio.DesignTools.Extensibility.Features
Imports Microsoft.VisualStudio.DesignTools.Extensibility.Model

Public Class MyControlDefaultInitializer
    Inherits DefaultInitializer

    Public Overrides Sub InitializeDefaults(item As ModelItem)
        item.Properties!Width.SetValue(800.0)
        MyBase.InitializeDefaults(item)
    End Sub
End Class
```

[XAML-Designer-Extensibility-Samples](https://github.com/microsoft/xaml-designer-extensibility-samples) deposunda daha fazla kod örneği bulunur.

## <a name="limited-support-for-designdll-extensions"></a>. Design. dll uzantıları için sınırlı destek

Bir denetim kitaplığı için herhangi bir *. DesignTools. dll* uzantısı bulunursa, önce yüklenir ve *. Design. dll* uzantıları için bulma atlanır.

Hayır *. DesignTools. dll* uzantıları mevcut ancak *. Design. dll* uzantısı bulunursa xaml dil hizmeti, temel düzenleyiciyi ve Özellik denetçisi senaryolarını desteklemek üzere öznitelik tablosu bilgilerini ayıklamak için bu derlemeyi yüklemeyi dener. Bu mekanizma kapsamında sınırlıdır. Özellik sağlayıcılarını yürütmek için tasarımcı yalıtım uzantılarının yüklenmesine izin vermez, ancak mevcut WPF denetim kitaplıkları için temel destek sağlayabilir.
