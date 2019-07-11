---
title: XAML Tasarımcısı genişletilebilirlik geçiş
ms.date: 07/09/2019
ms.topic: conceptual
author: lutzroeder
ms.author: lutzr
manager: jillfra
dev_langs:
- csharp
- vb
monikerRange: vs-2019
ms.openlocfilehash: 52bc8a6a0097d255891f4b6111a27bff85091bec
ms.sourcegitcommit: 208395bc122f8d3dae3f5e5960c42981cc368310
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/10/2019
ms.locfileid: "67784484"
---
# <a name="xaml-designer-extensibility-migration"></a>XAML Tasarımcısı genişletilebilirlik geçiş

Visual Studio 2019 genel Önizleme sürümü 16.1 başlayan, XAML Tasarımcısı'nı iki farklı mimari destekler: Tasarımcısı yalıtım mimarisi ve daha yeni surface yalıtım mimarisi. Bu mimari geçiş, bir .NET Framework işlemde barındırılamaz hedef çalışma zamanları desteklemek için gereklidir. Yüzey yalıtım mimariye taşıma önemli değişiklikler için üçüncü taraf genişletilebilirlik modeli sunar. Bu makalede değişiklikler özetlenmektedir.

**Tasarımcı yalıtım** destekler ve .NET Framework'ü hedefleyen projeler için WPF tasarımcısı tarafından kullanılan *. design.dll* uzantıları. Kullanıcı kodu, Denetim kitaplıklarını ve üçüncü taraf uzantıları dış işlemde yüklenir (*XDesProc.exe*) yanı sıra gerçek tasarımcı kod ve tasarımcı bölmelerini.

**Yüzey yalıtım** UWP tasarımcısı tarafından kullanılır. .NET Core hedefleyen projeler için WPF tasarımcısı tarafından da kullanılır. Visual Studio işlemin tasarımcı ve panellerini yüklenirken yüzey yalıtılmış olarak ayrı bir işlemde yalnızca kullanıcı kodunu ve denetimi kitaplıkları yüklenir (*DevEnv.exe*). Kullanıcı kodu ve denetimi kitaplıkları yürütmek için kullanılan çalışma zamanı gerçek tasarımcı ve üçüncü taraf genişletilebilirlik kod için .NET Framework tarafından kullanılan farklıdır.

![Genişletilebilirlik geçiş mimarisi](media/xaml-designer-extensibility-migration-architecture.png)

Bu mimari geçiş nedeniyle, üçüncü taraf uzantıları artık üçüncü taraf denetim kitaplıklarını aynı işlemde içine yüklenir. Uzantıları artık denetimi kitaplıkları'nı doğrudan bağımlılıkları olan veya çalışma zamanı nesneleri doğrudan erişebilirsiniz. Tasarımcı yalıtım mimarisi kullanmak için önceden yazılmış Uzantılar *Microsoft.Windows.Extensibility.dll* API yüzey yalıtım mimarisi ile çalışmaya yeni yaklaşıma geçirilmelidir. Uygulamada, varolan uzantıya yeni genişletilebilirlik API derlemelere karşı derlenmesi gerekir. Çalışma zamanı denetimi erişim türleri aracılığıyla [typeof](/dotnet/csharp/language-reference/keywords/typeof) veya çalışma zamanı örnekleri değiştirilmeli veya denetim kitaplıklarını artık farklı bir işlem içinde yüklendiği için kaldırıldı.

## <a name="new-extensibility-api-assemblies"></a>Yeni genişletilebilirlik API derlemeleri

Yeni genişletilebilirlik API derlemeleri mevcut genişletilebilirlik API derlemeleri için benzerdir, ancak bunları ayırt etmek için farklı bir adlandırma düzeni izleyin. Benzer şekilde, ad alanı adları, yeni derleme adları yansıtacak şekilde değiştirilmiştir.

| Tasarımcı yalıtım API derleme            | API yüzey yalıtım derleme                       |
|:------------------------------------------ |:---------------------------------------------------- |
| Microsoft.Windows.Design.Extensibility.dll | Microsoft.VisualStudio.DesignTools.Extensibility.dll |
| Microsoft.Windows.Design.Interaction.dll   | Microsoft.VisualStudio.DesignTools.Interaction.dll   |

## <a name="new-file-extension-and-discovery"></a>Yeni dosya uzantısı ve bulma

Yerine *. design.dll* dosya uzantısı, uzantıları kullanarak keşfedilmeyecek yeni surface *. designtools.dll* dosya uzantısı. *. design.dll* ve *. designtools.dll* uzantıları aynı varolabilir *tasarım* alt.

Üçüncü taraf denetim kitaplıklarını gerçek hedef çalışma zamanı'için (.NET Core veya UWP) derlenen sırada *. designtools.dll* uzantısı bir .NET Framework derlemesi her zaman derlenmelidir.

## <a name="decouple-attribute-tables-from-runtime-types"></a>Çalışma zamanı türleri özniteliği tablolardan birbirinden ayırın

Yüzey yalıtım genişletilebilirlik modeli üzerinde gerçek denetim kitaplıklarına bağımlı uzantıları için izin vermez ve bu nedenle, türleri Denetim Kitaplığı'ndan uzantılarına başvuramaz. Örneğin, *MyLibrary.designtools.dll* bir bağımlılık olmamalıdır *MyLibrary.dll*.

Bu tür bağımlılıkları özniteliği tabloları aracılığıyla türleri için meta verileri kaydedilirken en yaygın. Denetim Kitaplığı başvuran uzantı kodu türleri aracılığıyla doğrudan [typeof](/dotnet/csharp/language-reference/keywords/typeof) ([GetType](/dotnet/visual-basic/language-reference/operators/gettype-operator) Visual Basic'te) dize tabanlı tür adları kullanarak yeni API'ler değiştirilir:

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
      AttributeTableBuilder builder = new AttributeTableBuilder();
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

## <a name="feature-providers-and-model-api"></a>Özellik sağlayıcıları ve Model API

Özellik sağlayıcıları uzantısı derlemeleri uygulanan ve Visual Studio işlemde yüklü. `FeatureAttribute` özellik sağlayıcısı türleri kullanarak doğrudan başvurmaya devam eder [typeof](/dotnet/csharp/language-reference/keywords/typeof).

Özellik sağlayıcıları artık gerçek çalışma zamanı kod ve denetim kitaplıklarından farklı bir işlemde yüklendiği için bunlar artık çalışma zamanı nesneleri doğrudan erişebilir. Bunun yerine, karşılık gelen Model tabanlı API'leri kullanmak için tüm etkileşimleri dönüştürülmesi gerekir. Model API güncelleştirildi ve erişimi <xref:System.Type> veya <xref:System.Object> ya da artık kullanılmayan veya ile değiştirilmiştir `TypeIdentifier` ve `TypeDefinition`.

`TypeIdentifier` bir dizeyi bir türünü tanımlayan bir derleme adı temsil eder. A `TypeIdenfifier` hedefine çözümlenebilmesi bir `TypeDefinition` sorgu türü hakkında ek bilgiler. `TypeDefinition` örnekleri uzantı kodunda önbelleğe alınamaz.

```csharp
TypeDefinition type = ModelFactory.ResolveType(
    item.Context, new TypeIdentifier("MyLibrary.MyControl"));
TypeDefinition buttonType = ModelFactory.ResolveType(
    item.Context, new TypeIdentifier("System.Windows.Controls.Button"));
if (type != null && buttonType != type.IsSubclassOf(buttonType))
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

API yüzey yalıtım genişletilebilirlik API kümesinden kaldırıldı:

* `ModelFactory.CreateItem(EditingContext context, object item)`
* `ViewItem.PlatformObject`
* `ModelProperty.DefaultValue`

Kullandığınız API'leri `TypeIdentifier` yerine <xref:System.Type>:

* `ModelFactory.CreateItem(EditingContext context, Type itemType, params object[] arguments)`
* `ModelFactory.CreateItem(EditingContext context, Type itemType, CreateOptions options, params object[] arguments)`
* `ModelFactory.CreateStaticMemberItem(EditingContext context, Type type, string memberName)`
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

Kullandığınız API'leri `TypeIdentifier` yerine <xref:System.Type> ve artık oluşturucu bağımsız değişkenleri desteklemiyor:

* `ModelFactory.CreateItem(EditingContext context, TypeIdentifier typeIdentifier, params object[] arguments)`
* `ModelFactory.CreateItem(EditingContext context, TypeIdentifier typeIdentifier, CreateOptions options, params object[] arguments)`

Kullandığınız API'leri `TypeDefinition` yerine <xref:System.Type>:

* `ModelFactory.ResolveType(EditingContext context, TypeIdentifier typeIdentifier)`
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

Kullandığınız API'leri `ModelItem` yerine <xref:System.Object>:

* `ModelItemCollection.Insert(int index, object value)`
* `ModelItemCollection.Remove(object value)`
* `ModelItemDictionary.Add(object key, object value)`
* `ModelItemDictionary.ContainsKey(object key)`
* `ModelItemDictionary.Remove(object key)`
* `ModelItemDictionary.TryGetValue(object key, out ModelItem value)`

Gibi ilkel türler bilinen `Int32`, `String`, veya `Thickness` modeli API'si için .NET Framework örnekleri olarak geçirilebilir ve karşılık gelen nesne hedef çalışma zamanı işleminde dönüştürülür. Örneğin:

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

## <a name="limited-support-for-designdll-extensions"></a>Desteği sınırlı. design.dll uzantıları

Varsa *. designtools.dll* uzantısı için bir denetim kitaplığı bulunan, ilk ve bulma için yüklenen *. design.dll* uzantıları atlandı.

Hayır ise *. designtools.dll* uzantıları var ancak *. design.dll* uzantısı bulundu, XAML dil hizmeti desteklemek için öznitelik tablo bilgileri ayıklamak için bu derlemesini yükleme girişiminde temel düzenleyici ve Özellik denetçisi senaryoları. Bu mekanizma, kapsam içinde sınırlıdır. Bu özellik sağlayıcıları yürütmek için tasarımcı yalıtım uzantı izin vermez ancak temel desteği için mevcut WPF denetim kitaplığı sağlayabilir.
