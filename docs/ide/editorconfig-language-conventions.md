---
title: EditorConfig için .NET dil kuralları
ms.date: 06/17/2019
ms.topic: reference
dev_langs:
- CSharp
- VB
helpviewer_keywords:
- language code style rules [EditorConfig]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 0ddb6173095b8d4fd552e108f458a271321511c7
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/11/2019
ms.locfileid: "67823298"
---
# <a name="language-conventions"></a>Dil kuralları

Visual Studio'da EditorConfig için dil kuralları iki kategoriye ayrılır:

- [.NET kod stili ayarları](#net-code-style-settings)

- [C# kod stili ayarları](#c-code-style-settings)

> [!TIP]
> Tercih ettiğiniz programlama dilini kod örnekleri görmek için dil Seçici tarayıcı penceresinin sağ üst köşedeki kullanarak seçin.

## <a name="rule-format"></a>Kural biçimi

Dil kuralları için kuralları aşağıdaki genel biçime sahiptir:

`option_name = value:severity`

Her dil kural için varsa tanımlayan bir değeri veya ne zaman stili tercih belirtin. Birçok kuralları değerini kabul `true` (Bu stil tercih et) veya `false` (Bu stil tercih değil); başkalarının değerleri gibi kabul `when_on_single_line` veya `never`. İkinci bir kuralın parçası belirtir **önem derecesi**.

### <a name="severity"></a>Önem Derecesi

Bir dil kural önem derecesi, o stilin zorlamak düzeyinde belirtir. Olası önem derecesi değerlerini ve bunların etkileri aşağıdaki tabloda listelenmektedir:

Önem Derecesi | Efekt
:------- | ------
`none` | Bu kural ihlal edildiğinde herhangi bir şey kullanıcıya göstermez. Kod oluşturma özellikleri kodu bu stilde, ancak oluşturma. İle kurallar `none` önem derecesi hiçbir zaman görünür **hızlı Eylemler ve yeniden düzenlemeler** menüsü. Çoğu durumda, bu "yoksayıldı" veya "devre dışı" olarak kabul edilir.
`silent` (Ayrıca `refactoring` Visual Studio 2017 sürüm 15,8 ve üzeri) | Bu kural ihlal edildiğinde herhangi bir şey kullanıcıya göstermez. Kod oluşturma özellikleri kodu bu stilde, ancak oluşturma. İle kurallar `silent` önem derecesi temizleme katılmak yanı sıra görünür **hızlı Eylemler ve yeniden düzenlemeler** menüsü.
`suggestion` | Bu stil kuralı ihlal edildiğinde kullanıcıya öneri olarak gösterir. Öneriler, ilk iki karakter altındaki gri üç nokta olarak görünür.
`warning` | Bu stil kuralı ihlal edildiğinde bir derleyici uyarısı gösterir.
`error` | Bu stil kuralı ihlal edildiğinde bir derleyici hatası gösterir.

## <a name="net-code-style-settings"></a>.NET kod stili ayarları

Stil kurallarını Bu bölümde, hem C# ve Visual Basic için geçerlidir.

- ["This." ve "Me." niteleyicileri](#this-and-me)
  - DotNet\_stili\_nitelik\_for_field
  - DotNet\_stili\_nitelik\_for_property
  - DotNet\_stili\_nitelik\_for_method
  - DotNet\_stili\_nitelik\_for_event
- [Dil anahtar sözcükleri framework yerine tür başvurularını adlarını yazın](#language-keywords)
  - DotNet\_stili\_önceden tanımlanmış\_türü\_için\_Yereller\_parameters_members
  - DotNet\_stili\_önceden tanımlanmış\_türü\_için\_member_access
- [Değiştiricisi tercihleri](#normalize-modifiers)
  - DotNet\_stili\_gerektiren\_accessibility_modifiers
  - csharp\_preferred\_modifier_order
  - görsel\_temel\_tercih edilen\_modifier_order
  - DotNet\_stili\_salt okunur\_alan
- [Parantez tercihleri](#parentheses-preferences)
  - DotNet\_stili\_parantez\_içinde\_aritmetik\_ikili\_işleçleri
  - DotNet\_stili\_parantez\_içinde\_diğer\_ikili\_işleçleri
  - DotNet\_stili\_parantez\_içinde\_diğer\_işleçleri
  - DotNet\_stili\_parantez\_içinde\_ilişkisel\_ikili\_işleçleri
- [İfade düzeyi tercihleri](#expression-level-preferences)
  - DotNet\_stili\_object_initializer
  - DotNet\_stili\_collection_initializer
  - dotnet\_style\_explicit\_tuple_names
  - DotNet\_stili\_tercih\_çıkarılan\_tuple_names
  - DotNet\_stili\_tercih\_çıkarılan\_anonim\_türü\_member_names
  - DotNet\_stili\_tercih\_otomatik\_özellikleri
  - DotNet\_stili\_tercih\_olduğu\_null\_denetleyin\_üzerinden\_başvuru\_eşitlik\_yöntemi
  - DotNet\_stili\_tercih\_koşullu\_ifade\_üzerinden\_atama
  - DotNet\_stili\_tercih\_koşullu\_ifade\_üzerinden\_döndürür
- ["Null" Tercihler denetleniyor](#null-checking-preferences)
  - DotNet\_stili\_coalesce_expression
  - DotNet\_stili\_null_propagation

### <a name="this-and-me"></a>"This." ve "Me." niteleyicileri

Bu stil kuralı, alanlar, özellikler, yöntemler veya olayları için uygulanabilir. Değerini **true** anlamına gelir, kod simge ile başlayan tercih `this.` C# veya `Me.` Visual Basic'te. Değerini **false** anlamına gelir, kod öğesi tercih _değil_ başında için `this.` veya `Me.`.

Bu kurallar, görünebilir bir *.editorconfig* aşağıdaki gibi:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_qualification_for_field = false:suggestion
dotnet_style_qualification_for_property = false:suggestion
dotnet_style_qualification_for_method = false:suggestion
dotnet_style_qualification_for_event = false:suggestion
```

#### <a name="dotnetstylequalificationforfield"></a>DotNet\_stili\_nitelik\_for_field

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_field |
| **Kural Kimliği** | IDE0003 ve IDE0009 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -İle başlayan alanlar tercih `this.` içinde C# veya `Me.` Visual Basic'te<br /><br />`false` -Alanları tercih _değil_ başında için `this.` veya `Me.` |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// dotnet_style_qualification_for_field = true
this.capacity = 0;

// dotnet_style_qualification_for_field = false
capacity = 0;
```

```vb
' dotnet_style_qualification_for_field = true
Me.capacity = 0

' dotnet_style_qualification_for_field = false
capacity = 0
```

#### <a name="dotnetstylequalificationforproperty"></a>DotNet\_stili\_nitelik\_for_property

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_property |
| **Kural Kimliği** | IDE0003 ve IDE0009 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -İle başlayan için özellikleri tercih et `this.` içinde C# veya `Me.` Visual Basic'te<br /><br />`false` -Özellikleri tercih et _değil_ başında için `this.` veya `Me.` |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// dotnet_style_qualification_for_property = true
this.ID = 0;

// dotnet_style_qualification_for_property = false
ID = 0;
```

```vb
' dotnet_style_qualification_for_property = true
Me.ID = 0

' dotnet_style_qualification_for_property = false
ID = 0
```

#### <a name="dotnetstylequalificationformethod"></a>DotNet\_stili\_nitelik\_for_method

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_method |
| **Kural Kimliği** | IDE0003 ve IDE0009 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -İle başlayan yöntemleri tercih `this.` içinde C# veya `Me.` Visual Basic'te.<br /><br />`false` -Yöntemleri tercih _değil_ başında için `this.` veya `Me.`. |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// dotnet_style_qualification_for_method = true
this.Display();

// dotnet_style_qualification_for_method = false
Display();
```

```vb
' dotnet_style_qualification_for_method = true
Me.Display()

' dotnet_style_qualification_for_method = false
Display()
```

#### <a name="dotnetstylequalificationforevent"></a>DotNet\_stili\_nitelik\_for_event

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_event |
| **Kural Kimliği** | IDE0003 ve IDE0009 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -İle başlayan olayları tercih `this.` içinde C# veya `Me.` Visual Basic'te.<br /><br />`false` -Olayları tercih _değil_ başında için `this.` veya `Me.`. |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// dotnet_style_qualification_for_event = true
this.Elapsed += Handler;

// dotnet_style_qualification_for_event = false
Elapsed += Handler;
```

```vb
' dotnet_style_qualification_for_event = true
AddHandler Me.Elapsed, AddressOf Handler

' dotnet_style_qualification_for_event = false
AddHandler Elapsed, AddressOf Handler
```

### <a name="language-keywords"></a>Dil anahtar sözcükleri framework yerine tür başvurularını adlarını yazın

Bu stil kuralı, yerel değişkenler, yöntem parametreleri ve sınıf üyeleri veya üye erişimi ifadeleri yazmak için ayrı bir kural olarak uygulanabilir. Değerini **true** anlamına gelir, tercih ettiğiniz dil anahtar sözcüğü (örneğin, `int` veya `Integer`) tür adı yerine (örneğin, `Int32`) bunları temsil etmek için bir anahtar sözcük sahip türleri. Değerini **false** anlamına gelir, tercih ettiğiniz dil anahtar sözcüğü yerine tür adı.

Bu kurallar, görünebilir bir *.editorconfig* aşağıdaki gibi:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_predefined_type_for_locals_parameters_members = true:suggestion
dotnet_style_predefined_type_for_member_access = true:suggestion
```

#### <a name="dotnetstylepredefinedtypeforlocalsparametersmembers"></a>DotNet\_stili\_önceden tanımlanmış\_türü\_için\_Yereller\_parameters_members

|||
|-|-|
| **Kural adı** | dotnet_style_predefined_type_for_locals_parameters_members |
| **Kural Kimliği** | IDE0012 ve IDE0014 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Tercih ettiğiniz yerel değişkenler, yöntem parametreleri ve sınıf üyeleri, bunları temsil etmek için bir anahtar sözcüğüne sahip türler için tür adı yerine dil anahtar sözcüğü<br /><br />`false` -Yerel değişkenler, yöntem parametreleri ve dil anahtar sözcüğü yerine sınıf üyeleri için tür adını tercih et |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// dotnet_style_predefined_type_for_locals_parameters_members = true
private int _member;

// dotnet_style_predefined_type_for_locals_parameters_members = false
private Int32 _member;
```

```vb
' dotnet_style_predefined_type_for_locals_parameters_members = true
Private _member As Integer

' dotnet_style_predefined_type_for_locals_parameters_members = false
Private _member As Int32
```

#### <a name="dotnetstylepredefinedtypeformemberaccess"></a>DotNet\_stili\_önceden tanımlanmış\_türü\_için\_member_access

|||
|-|-|
| **Kural adı** | dotnet_style_predefined_type_for_member_access |
| **Kural Kimliği** | IDE0013 ve IDE0015 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Tercih ettiğiniz bunları temsil etmek için bir anahtar sözcüğüne sahip türler için tür adı yerine üye erişimi ifadeleri için dil anahtar sözcüğü<br /><br />`false` -Dil anahtar sözcüğü yerine üye erişimi ifadeleri için tür adını tercih et |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// dotnet_style_predefined_type_for_member_access = true
var local = int.MaxValue;

// dotnet_style_predefined_type_for_member_access = false
var local = Int32.MaxValue;
```

```vb
' dotnet_style_predefined_type_for_member_access = true
Dim local = Integer.MaxValue

' dotnet_style_predefined_type_for_member_access = false
Dim local = Int32.MaxValue
```

### <a name="normalize-modifiers"></a>Değiştiricisi tercihleri

Bu bölümdeki Stil kurallarının değiştiricisi tercihleri, erişilebilirlik değiştiricileri gerektiren, istenen değiştiricisi sıralama düzenini belirten ve salt okunur değiştiricisi gerektirme dahil olmak üzere uğraşmak.

Bu kurallar, görünebilir bir *.editorconfig* aşağıdaki gibi:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_require_accessibility_modifiers = always:suggestion
dotnet_style_readonly_field = true:warning

# CSharp code style settings:
[*.cs]
csharp_preferred_modifier_order = public,private,protected,internal,static,extern,new,virtual,abstract,sealed,override,readonly,unsafe,volatile,async:suggestion

# Visual Basic code style settings:
[*.vb]
visual_basic_preferred_modifier_order = Partial,Default,Private,Protected,Public,Friend,NotOverridable,Overridable,MustOverride,Overloads,Overrides,MustInherit,NotInheritable,Static,Shared,Shadows,ReadOnly,WriteOnly,Dim,Const,WithEvents,Widening,Narrowing,Custom,Async:suggestion
```

#### <a name="dotnetstylerequireaccessibilitymodifiers"></a>DotNet\_stili\_gerektiren\_accessibility_modifiers

|||
|-|-|
| **Kural adı** | dotnet_style_require_accessibility_modifiers |
| **Kural Kimliği** | IDE0040 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `always` -Belirtilmesi için erişilebilirlik değiştiricileri tercih eder.<br /><br />`for_non_interface_members` -Dışında ortak arabirim üyeleri için erişilebilirlik değiştiricileri tercih eder. (Bu, aynı **her zaman** ve gelecekteki sağlama örneğin eklendiğinden C# varsayılan arabirim yöntemleri ekler.)<br /><br />`never` -Erişilebilirlik değiştiricileri belirtilmesi tercih ediyorsunuz.<br /><br />`omit_if_default` -Dışında varsayılan değiştirici olup olmadıklarını belirtilmesi için erişilebilirlik değiştiricileri tercih eder. |
| **Visual Studio varsayılan** | `for_non_interface_members:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.5 |

Kod örnekleri:

```csharp
// dotnet_style_require_accessibility_modifiers = always
// dotnet_style_require_accessibility_modifiers = for_non_interface_members
class MyClass
{
    private const string thisFieldIsConst = "constant";
}

// dotnet_style_require_accessibility_modifiers = never
class MyClass
{
    const string thisFieldIsConst = "constant";
}
```

#### <a name="csharppreferredmodifierorder"></a>csharp_preferred_modifier_order

|||
|-|-|
| **Kural adı** | csharp_preferred_modifier_order |
| **Kural Kimliği** | IDE0036 |
| **Geçerli diller** | C# |
| **Değerler** | Bir veya daha fazla C# değiştiriciler, gibi `public`, `private`, ve `protected` |
| **Visual Studio varsayılan** | `public, private, protected, internal, static, extern, new, virtual, abstract, sealed, override, readonly, unsafe, volatile, async:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.5 |

- Bu kural değiştiriciler listesine ayarlandığında, belirtilen sıralama tercih eder.
- Bu kural dosyasından atlandığında, değiştirici sırasını tercih ediyorsunuz.

Kod örnekleri:

```csharp
// csharp_preferred_modifier_order = public,private,protected,internal,static,extern,new,virtual,abstract,sealed,override,readonly,unsafe,volatile,async
class MyClass
{
    private static readonly int _daysInYear = 365;
}
```

#### <a name="visualbasicpreferredmodifierorder"></a>visual_basic_preferred_modifier_order

|||
|-|-|
| **Kural adı** | visual_basic_preferred_modifier_order |
| **Kural Kimliği** | IDE0036 |
| **Geçerli diller** | Visual Basic |
| **Değerler** | Visual Basic değiştiriciler, bir veya daha fazla gibi `Partial`, `Private`, ve `Public` |
| **Visual Studio varsayılan** | `Partial, Default, Private, Protected, Public, Friend, NotOverridable, Overridable, MustOverride, Overloads, Overrides, MustInherit, NotInheritable, Static, Shared, Shadows, ReadOnly, WriteOnly, Dim, Const,WithEvents, Widening, Narrowing, Custom, Async:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.5 |

- Bu kural değiştiriciler listesine ayarlandığında, belirtilen sıralama tercih eder.
- Bu kural dosyasından atlandığında, değiştirici sırasını tercih ediyorsunuz.

Kod örnekleri:

```vb
' visual_basic_preferred_modifier_order = Partial,Default,Private,Protected,Public,Friend,NotOverridable,Overridable,MustOverride,Overloads,Overrides,MustInherit,NotInheritable,Static,Shared,Shadows,ReadOnly,WriteOnly,Dim,Const,WithEvents,Widening,Narrowing,Custom,Async
Public Class MyClass
    Private Shared ReadOnly daysInYear As Int = 365
End Class
```

#### <a name="dotnetstylereadonlyfield"></a>dotnet_style_readonly_field

|||
|-|-|
| **Kural adı** | dotnet_style_readonly_field |
| **Kural Kimliği** | IDE0044 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Tercih ettiğiniz alanları ile işaretlenmelidir `readonly` (C#) veya `ReadOnly` yalnızca satır içi hiç olmadığı kadar atandığı veya bir oluşturucu içinde olması durumunda (Visual Basic)<br /><br />`false` -Tercih yok olup alanları ile işaretlenmelidir üzerinden belirtin `readonly` (C#) veya `ReadOnly` (Visual Basic) |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |

Kod örnekleri:

```csharp
// dotnet_style_readonly_field = true
class MyClass
{
    private readonly int _daysInYear = 365;
}
```

```vb
' dotnet_style_readonly_field = true
Public Class MyClass
    Private ReadOnly daysInYear As Int = 365
End Class
```

### <a name="parentheses-preferences"></a>Parantez tercihleri

Bu bölümdeki Stil kurallarının parantez tercihleri, parantez aritmetik, ilişkisel, için ve diğer ikili işleçler kullanımı dahil olmak üzere uğraşmak.

Bu kurallar, görünebilir bir *.editorconfig* aşağıdaki gibi:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_parentheses_in_arithmetic_binary_operators = always_for_clarity:silent
dotnet_style_parentheses_in_relational_binary_operators = always_for_clarity:silent
dotnet_style_parentheses_in_other_binary_operators = always_for_clarity:silent
dotnet_style_parentheses_in_other_operators = never_if_unnecessary:silent
```

#### <a name="dotnetstyleparenthesesinarithmeticbinaryoperators"></a>DotNet\_stili\_parantez\_içinde\_aritmetik\_binary_operators

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_arithmetic_binary_operators |
| **Kural Kimliği** | IDE0047 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity` -Tercih ettiğiniz aritmetik işleç açıklamak için parantezler (`*`, `/`, `%`, `+`, `-`, `<<`, `>>`, `&`, `^`, `|`) önceliği<br /><br />`never_if_unnecessary` -Aritmetik olduğunda parantezler almamayı tercih işleci (`*`, `/`, `%`, `+`, `-`, `<<`, `>>`, `&`, `^`, `|`) önceliği açıktır |
| **Visual Studio varsayılan** | `always_for_clarity:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15,8 |

Kod örnekleri:

```csharp
// dotnet_style_parentheses_in_arithmetic_binary_operators = always_for_clarity
var v = a + (b * c);

// dotnet_style_parentheses_in_arithmetic_binary_operators = never_if_unnecessary
var v = a + b * c;
```

```vb
' dotnet_style_parentheses_in_arithmetic_binary_operators = always_for_clarity
Dim v = a + (b * c)

' dotnet_style_parentheses_in_arithmetic_binary_operators = never_if_unnecessary
Dim v = a + b * c
```

#### <a name="dotnetstyleparenthesesinrelationalbinaryoperators"></a>DotNet\_stili\_parantez\_içinde\_ilişkisel\_binary_operators

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_relational_binary_operators |
| **Kural Kimliği** | IDE0047 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity` -Tercih ettiğiniz ilişkisel işleç açıklamak için parantezler (`>`, `<`, `<=`, `>=`, `is`, `as`, `==`, `!=`) önceliği<br /><br />`never_if_unnecessary` -İlişkisel olduğunda parantezler almamayı tercih işleci (`>`, `<`, `<=`, `>=`, `is`, `as`, `==`, `!=`) belirgin önceliği |
| **Visual Studio varsayılan** | `always_for_clarity:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15,8 |

Kod örnekleri:

```csharp
// dotnet_style_parentheses_in_relational_binary_operators = always_for_clarity
var v = (a < b) == (c > d);

// dotnet_style_parentheses_in_relational_binary_operators = never_if_unnecessary
var v = a < b == c > d;
```

```vb
' dotnet_style_parentheses_in_relational_binary_operators = always_for_clarity
Dim v = (a < b) = (c > d)

' dotnet_style_parentheses_in_relational_binary_operators = never_if_unnecessary
Dim v = a < b = c > d
```

#### <a name="dotnetstyleparenthesesinotherbinaryoperators"></a>DotNet\_stili\_parantez\_içinde\_diğer\_binary_operators

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_other_binary_operators |
| **Kural Kimliği** | IDE0047 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity` -Tercih et diğer ikili işleç açıklamak için parantezler (`&&`, `||`, `??`) önceliği<br /><br />`never_if_unnecessary` -Parantez almamayı tercih, diğer ikili işleç (`&&`, `||`, `??`) belirgin önceliği |
| **Visual Studio varsayılan** | `always_for_clarity:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15,8 |

Kod örnekleri:

```csharp
// dotnet_style_parentheses_in_other_binary_operators = always_for_clarity
var v = a || (b && c);

// dotnet_style_parentheses_in_other_binary_operators = never_if_unnecessary
var v = a || b && c;
```

```vb
' dotnet_style_parentheses_in_other_binary_operators = always_for_clarity
Dim v = a OrElse (b AndAlso c)

' dotnet_style_parentheses_in_other_binary_operators = never_if_unnecessary
Dim v = a OrElse b AndAlso c
```

#### <a name="dotnetstyleparenthesesinotheroperators"></a>DotNet\_stili\_parantez\_içinde\_other_operators

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_other_operators |
| **Kural Kimliği** | IDE0047 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity` -İşleç önceliği netleştirmek için parantez tercih et<br /><br />`never_if_unnecessary` -İşleç önceliği belirgin olduğunda parantezler almamayı tercih et |
| **Visual Studio varsayılan** | `never_if_unnecessary:silent` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15,8 |

Kod örnekleri:

```csharp
// dotnet_style_parentheses_in_other_operators = always_for_clarity
var v = (a.b).Length;

// dotnet_style_parentheses_in_other_operators = never_if_unnecessary
var v = a.b.Length;
```

```vb
' dotnet_style_parentheses_in_other_operators = always_for_clarity
Dim v = (a.b).Length

' dotnet_style_parentheses_in_other_operators = never_if_unnecessary
Dim v = a.b.Length
```

### <a name="expression-level-preferences"></a>İfade düzeyi tercihleri

Stil nesne başlatıcıları, koleksiyon başlatıcıları, açık veya çıkarsanan demet adları, kullanımı dahil olmak üzere bu bölümü endişe ifade düzeyi tercihlerinde kuralları ve anonim türler sonuçlandı.

Bu kurallar, görünebilir bir *.editorconfig* aşağıdaki gibi:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_object_initializer = true:suggestion
dotnet_style_collection_initializer = true:suggestion
dotnet_style_explicit_tuple_names = true:suggestion
dotnet_style_prefer_inferred_tuple_names = true:suggestion
dotnet_style_prefer_inferred_anonymous_type_member_names = true:suggestion
dotnet_style_prefer_auto_properties = true:silent
dotnet_style_prefer_conditional_expression_over_assignment = true:suggestion
dotnet_style_prefer_conditional_expression_over_return = true:suggestion
```

#### <a name="dotnetstyleobjectinitializer"></a>DotNet\_stili\_object_initializer

|||
|-|-|
| **Kural adı** | dotnet_style_object_initializer |
| **Kural Kimliği** | IDE0017 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Nesne başlatıcıları mümkün olduğunda kullanarak başlatılacak nesneleri tercih edin<br /><br />`false` -Nesnelere tercih *değil* olması nesne başlatıcıları kullanılarak başlatılır |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// dotnet_style_object_initializer = true
var c = new Customer() { Age = 21 };

// dotnet_style_object_initializer = false
var c = new Customer();
c.Age = 21;
```

```vb
' dotnet_style_object_initializer = true
Dim c = New Customer() With {.Age = 21}

' dotnet_style_object_initializer = false
Dim c = New Customer()
c.Age = 21
```

#### <a name="dotnetstylecollectioninitializer"></a>DotNet\_stili\_collection_initializer

|||
|-|-|
| **Kural adı** | dotnet_style_collection_initializer |
| **Kural Kimliği** | IDE0028 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Koleksiyonlar mümkün olduğunda koleksiyon başlatıcıları kullanarak başlatılacak tercih et<br /><br />`false` -Koleksiyonlar için tercih ettiğiniz *değil* olması koleksiyon başlatıcıları kullanılarak başlatılır |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// dotnet_style_collection_initializer = true
var list = new List<int> { 1, 2, 3 };

// dotnet_style_collection_initializer = false
var list = new List<int>();
list.Add(1);
list.Add(2);
list.Add(3);
```

```vb
' dotnet_style_collection_initializer = true
Dim list = New List(Of Integer) From {1, 2, 3}

' dotnet_style_collection_initializer = false
Dim list = New List(Of Integer)
list.Add(1)
list.Add(2)
list.Add(3)
```

#### <a name="dotnetstyleexplicittuplenames"></a>dotnet\_style\_explicit\_tuple_names

|||
|-|-|
| **Kural adı** | dotnet_style_explicit_tuple_names |
| **Kural Kimliği** | IDE0033 |
| **Geçerli diller** | C# 7.0 + ve Visual Basic 15 + |
| **Değerler** | `true` -Demet adları için ItemX özellikleri tercih et<br /><br />`false` -Demet adları ItemX özellikleri tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// dotnet_style_explicit_tuple_names = true
(string name, int age) customer = GetCustomer();
var name = customer.name;

// dotnet_style_explicit_tuple_names = false
(string name, int age) customer = GetCustomer();
var name = customer.Item1;
```

```vb
 ' dotnet_style_explicit_tuple_names = true
Dim customer As (name As String, age As Integer) = GetCustomer()
Dim name = customer.name

' dotnet_style_explicit_tuple_names = false
Dim customer As (name As String, age As Integer) = GetCustomer()
Dim name = customer.Item1
```

#### <a name="dotnetstylepreferinferredtuplenames"></a>DotNet\_stili\_tercih\_çıkarılan\_tuple_names

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_inferred_tuple_names |
| **Kural Kimliği** | IDE0037 |
| **Geçerli diller** | C# 7.1 + ve Visual Basic 15 + |
| **Değerler** | `true` -Gösterilen demet öğesi adlarını tercih et<br /><br />`false` -Açık demet öğesi adlarını tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.6 |

Kod örnekleri:

```csharp
// dotnet_style_prefer_inferred_tuple_names = true
var tuple = (age, name);

// dotnet_style_prefer_inferred_tuple_names = false
var tuple = (age: age, name: name);
```

```vb
' dotnet_style_prefer_inferred_tuple_names = true
Dim tuple = (name, age)

' dotnet_style_prefer_inferred_tuple_names = false
Dim tuple = (name:=name, age:=age)
```

#### <a name="dotnetstylepreferinferredanonymoustypemembernames"></a>DotNet\_stili\_tercih\_çıkarılan\_anonim\_türü\_member_names

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_inferred_anonymous_type_member_names |
| **Kural Kimliği** | IDE0037 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Gösterilen anonim tip üye adlarını tercih et<br /><br />`false` -Açık anonim tip üye adlarını tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.6 |

Kod örnekleri:

```csharp
// dotnet_style_prefer_inferred_anonymous_type_member_names = true
var anon = new { age, name };

// dotnet_style_prefer_inferred_anonymous_type_member_names = false
var anon = new { age = age, name = name };
```

```vb
' dotnet_style_prefer_inferred_anonymous_type_member_names = true
Dim anon = New With {name, age}

' dotnet_style_prefer_inferred_anonymous_type_member_names = false
Dim anon = New With {.name = name, .age = age}
```

#### <a name="dotnetstylepreferautoproperties"></a>DotNet\_stili\_tercih\_otomatik\_özellikleri

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_auto_properties |
| **Kural Kimliği** | IDE0032 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Autoproperties üzerinden özel yedekleme alanlarla özellikleri tercih et<br /><br />`false` -Autoproperties özel yedekleme alanlarla özellikleri tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |

Kod örnekleri:

```csharp
// dotnet_style_prefer_auto_properties = true
private int Age { get; }

// dotnet_style_prefer_auto_properties = false
private int age;

public int Age
{
    get
    {
        return age;
    }
}
```

```vb
' dotnet_style_prefer_auto_properties = true
Public ReadOnly Property Age As Integer

' dotnet_style_prefer_auto_properties = false
Private _age As Integer

Public ReadOnly Property Age As Integer
    Get
        return _age
    End Get
End Property
```

#### <a name="dotnetstylepreferisnullcheckoverreferenceequalitymethod"></a>DotNet\_stili\_tercih\_olduğu\_null\_denetleyin\_üzerinden\_başvuru\_eşitlik\_yöntemi

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_is_null_check_over_reference_equality_method |
| **Kural Kimliği** | IDE0041 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Tercih ettiğiniz üzerinden null denetimi desen eşleştirme ile kullanma `object.ReferenceEquals`<br /><br />`false` -Tercih `object.ReferenceEquals` üzerinden null denetimi ile desen eşleştirme |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |

Kod örnekleri:

```csharp
// dotnet_style_prefer_is_null_check_over_reference_equality_method = true
if (value is null)
    return;

// dotnet_style_prefer_is_null_check_over_reference_equality_method = false
if (object.ReferenceEquals(value, null))
    return;
```

```vb
' dotnet_style_prefer_is_null_check_over_reference_equality_method = true
If value Is Nothing
    Return
End If

' dotnet_style_prefer_is_null_check_over_reference_equality_method = false
If Object.ReferenceEquals(value, Nothing)
    Return
End If
```

#### <a name="dotnetstylepreferconditionalexpressionoverassignment"></a>dotnet\_style\_prefer\_conditional\_expression\_over_assignment

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_conditional_expression_over_assignment |
| **Kural Kimliği** | IDE0045 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Tercih Üçlü koşullu atamaları bir if-else deyimi<br /><br />`false` -Bir if-else deyimi atamaları Üçlü koşullu tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15,8 |

Kod örnekleri:

```csharp
// dotnet_style_prefer_conditional_expression_over_assignment = true
string s = expr ? "hello" : "world";

// dotnet_style_prefer_conditional_expression_over_assignment = false
string s;
if (expr)
{
    s = "hello";
}
else
{
    s = "world";
}
```

```vb
' dotnet_style_prefer_conditional_expression_over_assignment = true
Dim s As String = If(expr, "hello", "world")

' dotnet_style_prefer_conditional_expression_over_assignment = false
Dim s As String
If expr Then
    s = "hello"
Else
    s = "world"
End If
```

#### <a name="dotnetstylepreferconditionalexpressionoverreturn"></a>dotnet\_style\_prefer\_conditional\_expression\_over_return

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_conditional_expression_over_return |
| **Kural Kimliği** | IDE0046 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Üçlü koşullu bir if-else deyimi kullanmak için dönüş deyimleri tercih et<br /><br />`false` -Üçlü koşullu bir if-else deyimi kullanılacak dönüş deyimleri tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15,8 |

Kod örnekleri:

```csharp
// dotnet_style_prefer_conditional_expression_over_return = true
return expr ? "hello" : "world"

// dotnet_style_prefer_conditional_expression_over_return = false
if (expr)
{
    return "hello";
}
else
{
    return "world";
}
```

```vb
' dotnet_style_prefer_conditional_expression_over_return = true
Return If(expr, "hello", "world")

' dotnet_style_prefer_conditional_expression_over_return = false
If expr Then
    Return "hello"
Else
    Return "world"
End If
```

### <a name="null-checking-preferences"></a>Null denetimi tercihleri

Bu bölümdeki Stil kurallarının null denetimi tercihleri ilgilendiriyor.

Bu kurallar, görünebilir bir *.editorconfig* aşağıdaki gibi:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_coalesce_expression = true:suggestion
dotnet_style_null_propagation = true:suggestion
```

#### <a name="dotnetstylecoalesceexpression"></a>DotNet\_stili\_coalesce_expression

|||
|-|-|
| **Kural adı** | dotnet_style_coalesce_expression |
| **Kural Kimliği** | IDE0029 |
| **Geçerli diller** | C# ve Visual Basic |
| **Değerler** | `true` -Denetimi Üçlü işleç null birleşim ifadelerini tercih et<br /><br />`false` -Tercih ettiğiniz Üçlü işleç için null birleşim ifadelerini denetleniyor |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// dotnet_style_coalesce_expression = true
var v = x ?? y;

// dotnet_style_coalesce_expression = false
var v = x != null ? x : y; // or
var v = x == null ? y : x;
```

```vb
' dotnet_style_coalesce_expression = true
Dim v = If(x, y)

' dotnet_style_coalesce_expression = false
Dim v = If(x Is Nothing, y, x) ' or
Dim v = If(x IsNot Nothing, x, y)
```

#### <a name="dotnetstylenullpropagation"></a>DotNet\_stili\_null_propagation

|||
|-|-|
| **Kural adı** | dotnet_style_null_propagation |
| **Kural Kimliği** | IDE0031 |
| **Geçerli diller** | C# 6.0 + ve Visual Basic 14 + |
| **Değerler** | `true` -Null koşullu işleci mümkün olduğunda kullanmayı tercih eder<br /><br />`false` -Üçlü null denetimi mümkün olduğunda kullanmayı tercih eder |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// dotnet_style_null_propagation = true
var v = o?.ToString();

// dotnet_style_null_propagation = false
var v = o == null ? null : o.ToString(); // or
var v = o != null ? o.String() : null;
```

```vb
' dotnet_style_null_propagation = true
Dim v = o?.ToString()

' dotnet_style_null_propagation = false
Dim v = If(o Is Nothing, Nothing, o.ToString()) ' or
Dim v = If(o IsNot Nothing, o.ToString(), Nothing)
```

## <a name="c-code-style-settings"></a>C# kod stili ayarları

Bu bölümdeki stil kuralları yalnızca C# için geçerlidir.

- [Örtük ve açık türleri](#implicit-and-explicit-types)
  - CSharp\_stili\_var\_için\_yerleşik\_in_types
  - CSharp\_stili\_var\_olduğunda\_türü\_is_apparent
  - csharp\_style\_var_elsewhere
- [İfade gövdeli üyeler](#expression-bodied-members)
  - csharp\_style\_expression\_bodied_methods
  - CSharp\_stili\_ifade\_bodied_constructors
  - CSharp\_stili\_ifade\_bodied_operators
  - CSharp\_stili\_ifade\_bodied_properties
  - CSharp\_stili\_ifade\_bodied_indexers
  - CSharp\_stili\_ifade\_bodied_accessors
- [Desen eşleştirme](#pattern-matching)
  - CSharp\_stili\_deseni\_eşleşen\_üzerinden\_olduğu\_ile\_cast_check
  - CSharp\_stili\_deseni\_eşleşen\_üzerinden\_olarak\_ile\_null_check
- [Satır içi değişken bildirimi](#inlined-variable-declarations)
  - CSharp\_stili\_satır içine alınmış\_variable_declaration
- [İfade düzeyi tercihleri](#expression-level-preferences)
  - csharp\_prefer\_simple\_default_expression
  - CSharp\_stili\_deconstructed\_variable_declaration
  - CSharp\_stili\_deseni\_yerel\_üzerinden\_anonymous_function
- ["Null" Tercihler denetleniyor](#null-checking-preferences)
  - csharp\_style\_throw_expression
  - csharp\_style\_conditional\_delegate_call
- [Kod bloğu tercihleri](#code-block-preferences)
  - CSharp\_prefer_braces

### <a name="implicit-and-explicit-types"></a>Örtük ve açık türleri

Bu bölümdeki Stil kurallarının kullanımını ilgilendiriyor [var](/dotnet/csharp/language-reference/keywords/var) anahtar sözcüğü Değişken bildiriminde açık bir tür karşılaştırması. Bu kural türü belirgin olduğunda yerleşik türler ve diğer yerlerde için ayrı olarak uygulanabilir.

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_var_for_built_in_types = true:suggestion
csharp_style_var_when_type_is_apparent = true:suggestion
csharp_style_var_elsewhere = true:suggestion
```

#### <a name="csharpstylevarforbuiltintypes"></a>CSharp\_stili\_var\_için\_yerleşik\_in_types

|||
|-|-|
| **Kural adı** | csharp_style_var_for_built_in_types |
| **Kural Kimliği** | IDE0007 ve IDE0008 |
| **Geçerli diller** | C#  |
| **Değerler** | `true` -Tercih `var` değişkenleri gibi yerleşik sistem türleriyle bildirmek için kullanılır `int`<br /><br />`false` -Üzerinden açık türü tercih `var` değişkenler gibi yerleşik sistem türleriyle bildirmek için `int` |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_var_for_built_in_types = true
var x = 5;

// csharp_style_var_for_built_in_types = false
int x = 5;
```

#### <a name="csharpstylevarwhentypeisapparent"></a>CSharp\_stili\_var\_olduğunda\_türü\_is_apparent

|||
|-|-|
| **Kural adı** | csharp_style_var_when_type_is_apparent |
| **Kural Kimliği** | IDE0007 ve IDE0008 |
| **Geçerli diller** | C#  |
| **Değerler** | `true` -Tercih `var` zaman türü zaten belirtilen bir bildirimi ifadesinin sağ tarafta<br /><br />`false` -Üzerinden açık türü tercih `var` zaman türü zaten belirtilen bir bildirimi ifadesinin sağ tarafta |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_var_when_type_is_apparent = true
var obj = new Customer();

// csharp_style_var_when_type_is_apparent = false
Customer obj = new Customer();
```

#### <a name="csharpstylevarelsewhere"></a>csharp\_style\_var_elsewhere

|||
|-|-|
| **Kural adı** | csharp_style_var_elsewhere |
| **Kural Kimliği** | IDE0007 ve IDE0008 |
| **Geçerli diller** | C#  |
| **Değerler** | `true` -Tercih `var` tüm durumlarda açık tür üzerinden başka bir kod stili kural tarafından geçersiz kılınmadığı sürece<br /><br />`false` -Üzerinden açık türü tercih `var` tüm durumlarda, başka bir kod stili kural tarafından geçersiz kılınmadığı sürece |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_var_elsewhere = true
var f = this.Init();

// csharp_style_var_elsewhere = false
bool f = this.Init();
```

### <a name="expression-bodied-members"></a>İfade gövdeli üyeler

Bu bölümdeki Stil kurallarının kullanımını ilgilendiriyor [ifade gövdeli üyeler](/dotnet/csharp/programming-guide/statements-expressions-operators/expression-bodied-members) zaman tek bir ifadeye oluşur mantığı. Bu kural, yöntemleri, Oluşturucular, işleçler, özellikler, dizin oluşturucular ve erişimcileri için uygulanabilir.

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_expression_bodied_methods = false:silent
csharp_style_expression_bodied_constructors = false:silent
csharp_style_expression_bodied_operators = false:silent
csharp_style_expression_bodied_properties = true:suggestion
csharp_style_expression_bodied_indexers = true:suggestion
csharp_style_expression_bodied_accessors = true:suggestion
```

#### <a name="csharpstyleexpressionbodiedmethods"></a>csharp\_style\_expression\_bodied_methods

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_methods |
| **Kural Kimliği** | IDE0022 |
| **Geçerli diller** | C# 6.0+  |
| **Değerler** | `true` -Metotlar için ifade gövdeli üyeler tercih et<br /><br />`when_on_single_line` -Bunlar tek bir satırda ne zaman metotlar için ifade gövdeli üyeler tercih et<br /><br />`false` -Metotlar için blok gövdeleri tercih et |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_methods = true
public int GetAge() => this.Age;

// csharp_style_expression_bodied_methods = false
public int GetAge() { return this.Age; }
```

#### <a name="csharpstyleexpressionbodiedconstructors"></a>CSharp\_stili\_ifade\_bodied_constructors

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_constructors |
| **Kural Kimliği** | IDE0021 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Oluşturucular için ifade gövdeli üyeler tercih et<br /><br />`when_on_single_line` -Bunlar tek bir satırda ne zaman oluşturucular için ifade gövdeli üyeler tercih et<br /><br />`false` -Oluşturucular için blok gövdeleri tercih et |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_constructors = true
public Customer(int age) => Age = age;

// csharp_style_expression_bodied_constructors = false
public Customer(int age) { Age = age; }
```

#### <a name="csharpstyleexpressionbodiedoperators"></a>CSharp\_stili\_ifade\_bodied_operators

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_operators |
| **Kural Kimliği** | IDE0023 ve IDE0024 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -İşleçler için ifade gövdeli üyeler tercih et<br /><br />`when_on_single_line` -Bunlar tek bir satırda ne zaman işleçler için ifade gövdeli üyeler tercih et<br /><br />`false` -Blok gövdeleri için işleçleri tercih etme |
| **Visual Studio varsayılan** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_operators = true
public static ComplexNumber operator + (ComplexNumber c1, ComplexNumber c2)
    => new ComplexNumber(c1.Real + c2.Real, c1.Imaginary + c2.Imaginary);

// csharp_style_expression_bodied_operators = false
public static ComplexNumber operator + (ComplexNumber c1, ComplexNumber c2)
{ return new ComplexNumber(c1.Real + c2.Real, c1.Imaginary + c2.Imaginary); }
```

#### <a name="csharpstyleexpressionbodiedproperties"></a>CSharp\_stili\_ifade\_bodied_properties

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_properties |
| **Kural Kimliği** | IDE0025 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -İfade gövdeli üyeler özellikleri tercih et<br /><br />`when_on_single_line` -Bunlar tek bir satırda ne zaman ifade gövdeli üyeler özellikleri tercih et<br /><br />`false` -Blok gövdeleri özellikleri tercih et |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_properties = true
public int Age => _age;

// csharp_style_expression_bodied_properties = false
public int Age { get { return _age; }}
```

#### <a name="csharpstyleexpressionbodiedindexers"></a>CSharp\_stili\_ifade\_bodied_indexers

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_indexers |
| **Kural Kimliği** | IDE0026 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Dizin oluşturucular için ifade gövdeli üyeler tercih et<br /><br />`when_on_single_line` -Bunlar tek bir satırda olacaktır, dizin oluşturucular için ifade gövdeli üyeler tercih et<br /><br />`false` -Dizin oluşturucular için blok gövdeleri tercih et |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_indexers = true
public T this[int i] => _values[i];

// csharp_style_expression_bodied_indexers = false
public T this[int i] { get { return _values[i]; } }
```

#### <a name="csharpstyleexpressionbodiedaccessors"></a>CSharp\_stili\_ifade\_bodied_accessors

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_accessors |
| **Kural Kimliği** | IDE0027 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Erişimciler için ifade gövdeli üyeler tercih et<br /><br />`when_on_single_line` -Bunlar tek bir satırda ne zaman erişimciler için ifade gövdeli üyeler tercih et<br /><br />`false` -Erişimciler için blok gövdeleri tercih et |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_accessors = true
public int Age { get => _age; set => _age = value; }

// csharp_style_expression_bodied_accessors = false
public int Age { get { return _age; } set { _age = value; } }
```

### <a name="pattern-matching"></a>Desen eşleştirme

Bu bölümdeki Stil kurallarının kullanımını ilgilendiriyor [desen eşleştirme](/dotnet/csharp/pattern-matching) C#.

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_pattern_matching_over_is_with_cast_check = true:suggestion
csharp_style_pattern_matching_over_as_with_null_check = true:suggestion
```

#### <a name="csharpstylepatternmatchingoveriswithcastcheck"></a>CSharp\_stili\_deseni\_eşleşen\_üzerinden\_olduğu\_ile\_cast_check

|||
|-|-|
| **Kural adı** | csharp_style_pattern_matching_over_is_with_cast_check |
| **Kural Kimliği** | IDE0020 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Tercih ettiğiniz yerine desen eşleştirme `is` tür atamaları ifadelerle<br /><br />`false` -Tercih `is` ifadelerle desen eşleştirme yerine tür atamaları |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_pattern_matching_over_is_with_cast_check = true
if (o is int i) {...}

// csharp_style_pattern_matching_over_is_with_cast_check = false
if (o is int) {var i = (int)o; ... }
```

#### <a name="csharpstylepatternmatchingoveraswithnullcheck"></a>CSharp\_stili\_deseni\_eşleşen\_üzerinden\_olarak\_ile\_null_check

|||
|-|-|
| **Kural adı** | csharp_style_pattern_matching_over_as_with_null_check |
| **Kural Kimliği** | IDE0019 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Tercih ettiğiniz yerine desen eşleştirme `as` sorun belirli bir tür olup olmadığını belirlemek için null denetimlerinin ifadelerle<br /><br />`false` -Tercih `as` sorun belirli bir tür olup olmadığını belirlemek için desen eşleştirme yerine null denetimleri içeren ifadeler |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_pattern_matching_over_as_with_null_check = true
if (o is string s) {...}

// csharp_style_pattern_matching_over_as_with_null_check = false
var s = o as string;
if (s != null) {...}
```

### <a name="inlined-variable-declarations"></a>Satır içi değişken bildirimi

Bu stil kuralı endişeleriniz mi `out` veya satır içi değişkenler bildirilir. C# 7'de başlayarak, şunları yapabilirsiniz [bağımsız değişken listesinde bir yöntem çağrısının dışına çıkan bir değişkeni bildirmek](/dotnet/csharp/language-reference/keywords/out-parameter-modifier#calling-a-method-with-an-out-argument), yerine ayrı bir değişken bildirimi.

#### <a name="csharpstyleinlinedvariabledeclaration"></a>CSharp\_stili\_satır içine alınmış\_variable_declaration

|||
|-|-|
| **Kural adı** | csharp_style_inlined_variable_declaration |
| **Kural Kimliği** | IDE0018 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Tercih `out` değişkenler mümkün olduğunda, bir yöntem çağrısının bağımsız değişken listesindeki, satır içi olarak<br /><br />`false` -Tercih `out` yöntem çağrısından önce bildirilmesi için değişkenleri |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_inlined_variable_declaration = true
if (int.TryParse(value, out int i) {...}

// csharp_style_inlined_variable_declaration = false
int i;
if (int.TryParse(value, out i) {...}
```

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_inlined_variable_declaration = true:suggestion
```

### <a name="expression-level-preferences"></a>İfade düzeyi tercihleri

Stil kurallarının bu bölümdeki ifade düzeyi tercihleri, kullanımı dahil olmak üzere uğraşmak [varsayılan ifadeleri](/dotnet/csharp/programming-guide/statements-expressions-operators/default-value-expressions#default-literal-and-type-inference), ayrıştırılmış değişkenleri ve anonim işlevler üzerinde yerel işlevler.

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_prefer_simple_default_expression = true:suggestion
csharp_style_deconstructed_variable_declaration = true:suggestion
csharp_style_pattern_local_over_anonymous_function = true:suggestion
```

#### <a name="csharpprefersimpledefaultexpression"></a>csharp\_prefer\_simple\_default_expression

Bu stil kuralı kullanarak ilgiliyse [ `default` değişmez değer için varsayılan değer ifadeleri](/dotnet/csharp/programming-guide/statements-expressions-operators/default-value-expressions#default-literal-and-type-inference) zaman derleyici tanım Çıkarsama ifadenin türü.

|||
|-|-|
| **Kural adı** | csharp_prefer_simple_default_expression |
| **Kural Kimliği** | IDE0034 |
| **Geçerli diller** | C# 7.1+  |
| **Değerler** | `true` -Tercih `default` üzerinden `default(T)`<br /><br />`false` -Tercih `default(T)` üzerinden `default` |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_prefer_simple_default_expression = true
void DoWork(CancellationToken cancellationToken = default) { ... }

// csharp_prefer_simple_default_expression = false
void DoWork(CancellationToken cancellationToken = default(CancellationToken)) { ... }
```

#### <a name="csharpstyledeconstructedvariabledeclaration"></a>CSharp\_stili\_deconstructed\_variable_declaration

|||
|-|-|
| **Kural adı** | csharp_style_deconstructed_variable_declaration |
| **Kural Kimliği** | IDE0042 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Ayrıştırılmış değişken bildirimini tercih et<br /><br />`false` -Ayrıştırma deyiminin değişken bildirimlerinde tercih eder misiniz: |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_deconstructed_variable_declaration = true
var (name, age) = GetPersonTuple();
Console.WriteLine($"{name} {age}");

(int x, int y) = GetPointTuple();
Console.WriteLine($"{x} {y}");

// csharp_style_deconstructed_variable_declaration = false
var person = GetPersonTuple();
Console.WriteLine($"{person.name} {person.age}");

(int x, int y) point = GetPointTuple();
Console.WriteLine($"{point.x} {point.y}");
```

#### <a name="csharpstylepatternlocaloveranonymousfunction"></a>CSharp\_stili\_deseni\_yerel\_üzerinden\_anonymous_function

|||
|-|-|
| **Kural adı** | csharp_style_pattern_local_over_anonymous_function |
| **Kural Kimliği** | IDE0039 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Yerel işlevler üzerinde anonim işlevler tercih et<br /><br />`false` -Anonim işlevler yerel işlevler üzerinde tercih et |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_pattern_local_over_anonymous_function = true
int fibonacci(int n)
{
    return n <= 1 ? 1 : fibonacci(n-1) + fibonacci(n-2);
}

// csharp_style_pattern_local_over_anonymous_function = false
Func<int, int> fibonacci = null;
fibonacci = (int n) =>
{
    return n <= 1 ? 1 : fibonacci(n - 1) + fibonacci(n - 2);
};
```

### <a name="null-checking-preferences"></a>Null denetimi tercihleri

Bu kuralları önemli etrafında sözdizimi stil `null` kullanma dahil olmak üzere, denetimi `throw` ifadeleri veya `throw` ifadeleri ve null denetimi gerçekleştirmek veya koşullu birleşim işleci kullanmayı (`?.`) bir çağrılırken[lambda ifadesi](/dotnet/csharp/lambda-expressions).

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_throw_expression = true:suggestion
csharp_style_conditional_delegate_call = false:suggestion
```

#### <a name="csharpstylethrowexpression"></a>csharp\_style\_throw_expression

|||
|-|-|
| **Kural adı** | csharp_style_throw_expression |
| **Kural Kimliği** | IDE0016 |
| **Geçerli diller** | C# 7.0+  |
| **Değerler** | `true` -Kullanmayı tercih `throw` ifadeler yerine `throw` deyimleri<br /><br />`false` -Kullanmayı tercih `throw` yerine deyimleri `throw` ifadeleri |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_throw_expression = true
this.s = s ?? throw new ArgumentNullException(nameof(s));

// csharp_style_throw_expression = false
if (s == null) { throw new ArgumentNullException(nameof(s)); }
this.s = s;
```

#### <a name="csharpstyleconditionaldelegatecall"></a>csharp\_style\_conditional\_delegate_call

|||
|-|-|
| **Kural adı** | csharp_style_conditional_delegate_call |
| **Kural Kimliği** | IDE0041 |
| **Geçerli diller** | C# 6.0+  |
| **Değerler** | `true` -Koşullu birleşim işleci kullanılacak bakın (`?.`) bir lambda ifadesi çağrılırken null gerçekleştirmek yerine denetleyin<br /><br />`false` -Koşullu birleşim işleci kullanmak yerine, bir lambda ifadesi çağırmadan önce bir null denetimi gerçekleştirmek tercih ettiğiniz (`?.`) |
| **Visual Studio varsayılan** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_conditional_delegate_call = true
func?.Invoke(args);

// csharp_style_conditional_delegate_call = false
if (func != null) { func(args); }
```

### <a name="code-block-preferences"></a>Kod bloğu tercihleri

Bu stil kuralı kaşlı ayraçlar kullanımı ile ilgilidir `{ }` kod blokları kapsamak için.

Örnek *.editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_prefer_braces = true:silent
```

#### <a name="csharppreferbraces"></a>CSharp\_tercih\_küme ayraçları

|||
|-|-|
| **Kural adı** | csharp_prefer_braces |
| **Kural Kimliği** | IDE0011 |
| **Geçerli diller** | C# |
| **Değerler** | `true` -Bir kod satırı bile için küme ayracı tercih et<br /><br />`false` -İzin veriliyorsa hiçbir küme ayracı tercih et |
| **Visual Studio varsayılan** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_prefer_braces = true
if (test) { this.Display(); }

// csharp_prefer_braces = false
if (test) this.Display();
```

## <a name="see-also"></a>Ayrıca bkz.

- [Biçimlendirme kuralları](editorconfig-formatting-conventions.md)
- [Adlandırma kuralları](editorconfig-naming-conventions.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](editorconfig-code-style-settings-reference.md)
