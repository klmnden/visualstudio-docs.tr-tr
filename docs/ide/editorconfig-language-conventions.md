---
title: EditorConfig için .NET dil kuralları
ms.date: 07/17/2019
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
ms.openlocfilehash: 7b88824e6be7dbb216aa14ca9a22fd692474ec2f
ms.sourcegitcommit: a124076dfd6b4e5aecda4d01984fee7b0c034745
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2019
ms.locfileid: "68787416"
---
# <a name="language-conventions"></a>Dil kuralları

Visual Studio 'da EditorConfig için dil kuralları iki kategoriye ayrılır: Visual Basic ve C#ve C# özel olanlar için geçerlidir. Dil kuralları, bir programlama dilinin çeşitli yönlerinin nasıl kullanıldığını, örneğin değiştiriciler ve ayraçları etkiler.

> [!TIP]
> - **Bu makalede** , sayfanın farklı bölümlerine gitmek için bağlantıları kullanın.
> - Kod örneklerini tercih ettiğiniz programlama dilinde görmek için, tarayıcı penceresinin sağ üst köşesindeki dil seçicisini kullanarak bunu seçin.
>
>   ![Kod dili seçici denetimi](media/code-language-picker.png)

## <a name="rule-format"></a>Kural biçimi

Dil kuralları kuralları aşağıdaki genel biçimdedir:

`option_name = value:severity`

Her dil kuralı için, stilin ne zaman tercih edilmesi gerektiğini tanımlayan bir değer belirtirsiniz. `true` Birçok kural bir değeri kabul eder (Bu stili tercih edin) veya `false` (Bu stili tercih etmez); `when_on_single_line` diğerleri veya `never`gibi değerleri kabul eder. Kuralın ikinci bölümü **önem derecesini**belirtir.

### <a name="severity"></a>Önem Derecesi

Dil kuralı önem derecesi, bu stilin zorlanmasını sağlayan düzeyi belirtir. Aşağıdaki tabloda olası önem düzeyi değerleri ve bunların etkileri listelenmektedir:

Önem Derecesi | Efekt
:------- | ------
`none` | Bu kural ihlal edildiğinde kullanıcıya herhangi bir şey gösterme. Kod oluşturma özellikleri bu stilde kod üretir. Önem derecesine `none` sahip kurallar, **Hızlı Eylemler ve yeniden düzenlemeler** menüsünde hiçbir şekilde görünmez. Çoğu durumda bu, "devre dışı" veya "yoksayıldı" olarak değerlendirilir.
`silent`(Ayrıca `refactoring` , Visual Studio 2017 sürüm 15,8 ve üstü) | Bu kural ihlal edildiğinde kullanıcıya herhangi bir şey gösterme. Kod oluşturma özellikleri bu stilde kod üretir. Önem derecesine `silent` sahip kurallar Temizleme **ve hızlı eylemler ve yeniden düzenlemeler** menüsünde görünür.
`suggestion` | Bu stil kuralı ihlal edildiğinde kullanıcıya öneri olarak gösterin. Öneriler, ilk iki karakterin altında üç gri nokta olarak görünür.
`warning` | Bu stil kuralı ihlal edildiğinde, bir derleyici uyarısı gösterin.
`error` | Bu stil kuralı ihlal edildiğinde, bir derleyici hatası gösterir.

## <a name="net-code-style-settings"></a>.NET kod stili ayarları

Bu bölümdeki stil kuralları hem hem de C# Visual Basic için geçerlidir.

- ["This." ve "Me." niteleyicileri](#this-and-me)
  - DotNet\_stil\_niteliğifor_field\_
  - DotNet\_stil\_niteliğifor_property\_
  - DotNet\_stil\_niteliğifor_method\_
  - DotNet\_stil\_niteliğifor_event\_
- [Tür başvuruları için çerçeve türü adları yerine dil anahtar sözcükleri](#language-keywords)
  - \_Yereller\_\_için DotNet stili önceden tanımlanmış türü\_parameters_members\_\_
  - member_access\_için\_DotNetstiliönceden tanımlanmış\_türü\_\_
- [Değiştirici tercihleri](#normalize-modifiers)
  - DotNet\_stili\_accessibility_modifiersgerektirir\_
  - CSharp\_Tercihli\_modifier_order
  - Visual\_Basic\_tercihedilen\_modifier_order
  - DotNet\_stili\_ReadOnlyalanı\_
- [Parantez tercihleri](#parentheses-preferences)
  - \_aritmetik\_\_\_ikiliişleçlerindeDotNetstilayraçları\_\_
  - \_diğer\_\_\_ikiliişleçlerindeDotNetstilayraçları\_\_
  - diğer\_\_işleçlerdekiDotNet\_stil ayraçları\_\_
  - \_ilişkisel\_\_\_ikiliişleçlerindeDotNetstilayraçları\_\_
- [İfade düzeyi tercihleri](#expression-level-preferences)
  - DotNet\_stili\_object_initializer
  - DotNet\_stili\_collection_initializer
  - DotNet\_stili\_açıktuple_names\_
  - DotNet\_\_stili,çıkarılan\_tuple_names tercih eder\_
  - DotNet\_\_stili,gösterilen\_anonimtür\_member_namestercih et\_\_
  - DotNet\_\_stili\_otomatiközellikleritercih\_eder
  - DotNet\_\_\_stili,başvuru\_eşitlik\_yönteminin üzerinde null denetimi olmasını tercih ediyor\_\_\_\_
  - DotNet\_\_stili\_atama üzerindekoşullu\_ifadeyiterciheder\_\_
  - DotNet\_\_stili\_dönüşte\_koşulluifadeyi\_tercih et\_
  - DotNet\_\_stili\_bileşikatamayıtercih\_eder
- ["Null" Denetim tercihleri](#null-checking-preferences)
  - DotNet\_stili\_coalesce_expression
  - DotNet\_stili\_null_propagation

### <a name="this-and-me"></a>"This." ve "Me." ilerini

Bu stil kuralı alanlara, özelliklere, yöntemlere veya olaylara uygulanabilir. **True** değeri, kod sembolünün Visual Basic `this.` içinde veya C# `Me.` içinde ön planda hazır olmasını tercih eder. **False** değeri, kod öğesinin veya `Me.`ile `this.` önceden başında _olmaması_ gerektiğini gösterir.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_qualification_for_field = false:suggestion
dotnet_style_qualification_for_property = false:suggestion
dotnet_style_qualification_for_method = false:suggestion
dotnet_style_qualification_for_event = false:suggestion
```

#### <a name="dotnet_style_qualification_for_field"></a>DotNet\_stil\_niteliğifor_field\_

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_field |
| **Kural KIMLIĞI** | IDE0003 ve IDE0009 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Visual Basic `this.` içinde veya C# `Me.` içinde ön planda çıkacak alanları tercih et<br /><br />`false`-Veya ile `this.` kullanıma hazır olmayan alanları tercih et`Me.` |
| **Visual Studio varsayılanı** | `false:silent` |

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

#### <a name="dotnet_style_qualification_for_property"></a>DotNet\_stil\_niteliğifor_property\_

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_property |
| **Kural KIMLIĞI** | IDE0003 ve IDE0009 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Visual Basic `this.` içinde veya C# `Me.` içinde ön planda çıkacak özellikleri tercih et<br /><br />`false`-Veya ile birlikte `this.` kullanıma hazır olmayan özellikleri tercih et`Me.` |
| **Visual Studio varsayılanı** | `false:silent` |

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

#### <a name="dotnet_style_qualification_for_method"></a>DotNet\_stil\_niteliğifor_method\_

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_method |
| **Kural KIMLIĞI** | IDE0003 ve IDE0009 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Visual Basic ' de veya `this.` `Me.` ' de ön planda C# olan yöntemleri tercih edin.<br /><br />`false`-Veya `this.` ileönyüklenemezYöntemlertercihedin.`Me.` |
| **Visual Studio varsayılanı** | `false:silent` |

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

#### <a name="dotnet_style_qualification_for_event"></a>DotNet\_stil\_niteliğifor_event\_

|||
|-|-|
| **Kural adı** | dotnet_style_qualification_for_event |
| **Kural KIMLIĞI** | IDE0003 ve IDE0009 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Visual Basic içinde veya `this.` C# `Me.` ' de ön planda yapılacak olayları tercih edin.<br /><br />`false`-Veya `this.` ileönyüklenemezolaylarıtercihedin.`Me.` |
| **Visual Studio varsayılanı** | `false:silent` |

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

### <a name="language-keywords"></a>Tür başvuruları için çerçeve türü adları yerine dil anahtar sözcükleri

Bu stil kuralı yerel değişkenlere, yöntem parametrelerine ve sınıf üyelerine veya üye erişim ifadeleri yazmak için ayrı bir kural olarak uygulanabilir. **True** değeri, dil anahtar sözcüğünü ( `int` Örneğin, veya), bunları temsil etmek için anahtar sözcüğü olan türler için tür adı `Int32`değil (örneğin, veya `Integer`) tercih eder. **False** değeri, Language anahtar sözcüğü yerine tür adını tercih eder anlamına gelir.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_predefined_type_for_locals_parameters_members = true:suggestion
dotnet_style_predefined_type_for_member_access = true:suggestion
```

#### <a name="dotnet_style_predefined_type_for_locals_parameters_members"></a>\_Yereller\_\_için DotNet stili önceden tanımlanmış türü\_parameters_members\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_predefined_type_for_locals_parameters_members |
| **Kural KIMLIĞI** | IDE0012 ve IDE0014 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Bu tür adı yerine yerel değişkenler, yöntem parametreleri ve sınıf üyeleri için dil anahtar sözcüğünü tercih eden bir anahtar sözcük olan türler için tercih edin<br /><br />`false`-Dil anahtar sözcüğü yerine yerel değişkenler, yöntem parametreleri ve sınıf üyeleri için tür adını tercih edin |
| **Visual Studio varsayılanı** | `true:silent` |

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

#### <a name="dotnet_style_predefined_type_for_member_access"></a>member_access\_için\_DotNetstiliönceden tanımlanmış\_türü\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_predefined_type_for_member_access |
| **Kural KIMLIĞI** | IDE0013 ve IDE0015 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Temsil eden bir anahtar sözcüğe sahip türler için tür adı yerine üye erişim ifadeleri için dil anahtar sözcüğünü tercih edin<br /><br />`false`-Dil anahtar sözcüğü yerine üye erişim ifadeleri için tür adını tercih edin |
| **Visual Studio varsayılanı** | `true:silent` |

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

### <a name="normalize-modifiers"></a>Değiştirici tercihleri

Bu bölümdeki stil kuralları, erişilebilirlik değiştiricileri gerektirme, istenen değiştirici sıralama düzenini belirtme ve salt okunurdur değiştirici gerektirme dahil olmak üzere değiştirici tercihlerine devam ediyor.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

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

#### <a name="dotnet_style_require_accessibility_modifiers"></a>DotNet\_stili\_accessibility_modifiersgerektirir\_

|||
|-|-|
| **Kural adı** | dotnet_style_require_accessibility_modifiers |
| **Kural KIMLIĞI** | IDE0040 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `always`-Erişilebilirlik değiştiricilerini belirtilen şekilde tercih edin.<br /><br />`for_non_interface_members`-Genel arabirim üyeleri dışında belirtilecek erişilebilirlik değiştiricilerini tercih edin. (Bu **her zaman** ile aynıdır ve varsayılan arabirim yöntemleri C# eklerse ileride prova için eklenmiştir.)<br /><br />`never`-Erişilebilirlik değiştiricilerini belirtilen şekilde tercih etme.<br /><br />`omit_if_default`-Varsayılan değiştirici olup olmamaları dışında, erişilebilirlik değiştiricilerini belirtilmesini tercih edin. |
| **Visual Studio varsayılanı** | `for_non_interface_members:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15.5 |

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

#### <a name="csharp_preferred_modifier_order"></a>csharp_preferred_modifier_order

|||
|-|-|
| **Kural adı** | csharp_preferred_modifier_order |
| **Kural KIMLIĞI** | IDE0036 |
| **Uygun diller** | C# |
| **Değerler** | , Ve gibi C# bir veya daha fazla `public`değiştirici `private``protected` |
| **Visual Studio varsayılanı** | `public, private, protected, internal, static, extern, new, virtual, abstract, sealed, override, readonly, unsafe, volatile, async:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15.5 |

- Bu kural bir değiştiriciler listesine ayarlandığında, belirtilen sıralamayı tercih edin.
- Bu kural dosyadan atlandığında, bir değiştirici sırası tercih etmez.

Kod örnekleri:

```csharp
// csharp_preferred_modifier_order = public,private,protected,internal,static,extern,new,virtual,abstract,sealed,override,readonly,unsafe,volatile,async
class MyClass
{
    private static readonly int _daysInYear = 365;
}
```

#### <a name="visual_basic_preferred_modifier_order"></a>visual_basic_preferred_modifier_order

|||
|-|-|
| **Kural adı** | visual_basic_preferred_modifier_order |
| **Kural KIMLIĞI** | IDE0036 |
| **Uygun diller** | Visual Basic |
| **Değerler** | , Ve gibi bir veya daha fazla Visual Basic `Partial`değiştiricisi `Private``Public` |
| **Visual Studio varsayılanı** | `Partial, Default, Private, Protected, Public, Friend, NotOverridable, Overridable, MustOverride, Overloads, Overrides, MustInherit, NotInheritable, Static, Shared, Shadows, ReadOnly, WriteOnly, Dim, Const,WithEvents, Widening, Narrowing, Custom, Async:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15.5 |

- Bu kural bir değiştiriciler listesine ayarlandığında, belirtilen sıralamayı tercih edin.
- Bu kural dosyadan atlandığında, bir değiştirici sırası tercih etmez.

Kod örnekleri:

```vb
' visual_basic_preferred_modifier_order = Partial,Default,Private,Protected,Public,Friend,NotOverridable,Overridable,MustOverride,Overloads,Overrides,MustInherit,NotInheritable,Static,Shared,Shadows,ReadOnly,WriteOnly,Dim,Const,WithEvents,Widening,Narrowing,Custom,Async
Public Class MyClass
    Private Shared ReadOnly daysInYear As Int = 365
End Class
```

#### <a name="dotnet_style_readonly_field"></a>dotnet_style_readonly_field

|||
|-|-|
| **Kural adı** | dotnet_style_readonly_field |
| **Kural KIMLIĞI** | IDE0044 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Yalnızca satır içi olarak veya bir oluşturucunun `readonly` içindeC#varsa alanların `ReadOnly` () veya (Visual Basic) birlikte işaretlenmesini tercih eder<br /><br />`false`-Alanların ( `readonly` C#) veya `ReadOnly` (Visual Basic) ile işaretlenmesi gerekip gerekmediğini belirtmek için bir tercih yok |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |

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

Bu bölümdeki stil kuralları, aritmetik, ilişkisel ve diğer ikili işleçler için parantez kullanımı dahil olmak üzere parantezler tercihlerine yöneliktir.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_parentheses_in_arithmetic_binary_operators = always_for_clarity:silent
dotnet_style_parentheses_in_relational_binary_operators = always_for_clarity:silent
dotnet_style_parentheses_in_other_binary_operators = always_for_clarity:silent
dotnet_style_parentheses_in_other_operators = never_if_unnecessary:silent
```

#### <a name="dotnet_style_parentheses_in_arithmetic_binary_operators"></a>aritmetik\_\_binary_operatorsiçindeDotNet\_stil ayraçları\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_arithmetic_binary_operators |
| **Kural KIMLIĞI** | IDE0047 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity`-`*`Aritmetik işleci (, ,,,`-` ,,`|`,,,) önceliğini netleştirmek için ayraçları tercih edin `<<` `%` `/` `+` `>>` `&` `^`<br /><br />`never_if_unnecessary`-`*`Aritmetik işleç (, `-` ,`|`,,,, ,`&`,, ,,,,)sırasındaparantezler`^`içermemelidir `<<` `>>` `%` `/` `+` öncelik belirgin |
| **Visual Studio varsayılanı** | `always_for_clarity:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,8 |

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

#### <a name="dotnet_style_parentheses_in_relational_binary_operators"></a>ilişkisel\_\_binary_operatorsiçindeDotNet\_stil ayraçları\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_relational_binary_operators |
| **Kural KIMLIĞI** | IDE0047 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity``>`-İlişkisel işleç (, `<` `<=` ,`>=`,, ,,,,`as`,,, )önceliğininetleştirmekiçinayraçlarıtercih`!=` `is` `==`<br /><br />`never_if_unnecessary``>`-İlişkisel operatör (, `<`, `<=` `>=`,, `is` ,`==`,,,,,,, )önceliğibelirginolduğundaparantezleriiçermemelidir`!=` `as` |
| **Visual Studio varsayılanı** | `always_for_clarity:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,8 |

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

#### <a name="dotnet_style_parentheses_in_other_binary_operators"></a>diğer\_\_binary_operatorsiçindeDotNet\_stil ayraçları\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_other_binary_operators |
| **Kural KIMLIĞI** | IDE0047 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity`-Diğer ikili işleci (`&&`, `||`, `??`) önceliğini netleştirmek için parantezleri tercih et<br /><br />`never_if_unnecessary`-Diğer ikili işleç (`&&`, `||`, `??`) önceliği belirgin olduğunda parantez içermemelidir |
| **Visual Studio varsayılanı** | `always_for_clarity:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,8 |

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

#### <a name="dotnet_style_parentheses_in_other_operators"></a>other_operators\_içinde\_\_DotNet stil ayraçları\_

|||
|-|-|
| **Kural adı** | dotnet_style_parentheses_in_other_operators |
| **Kural KIMLIĞI** | IDE0047 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `always_for_clarity`-İşleç önceliğini netleştirmek için parantez tercih et<br /><br />`never_if_unnecessary`-İşleç önceliği belirgin olduğunda parantez içermemelidir |
| **Visual Studio varsayılanı** | `never_if_unnecessary:silent` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,8 |

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

Bu bölümdeki stil kuralları, nesne başlatıcıları, koleksiyon başlatıcıları, açık veya Çıkarsanan ad alanları ve çıkartılan anonim türler kullanımı dahil olmak üzere, ifade düzeyi tercihlere yönelik olarak sorun.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

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
dotnet_style_prefer_compound_assignment = true:suggestion
```

#### <a name="dotnet_style_object_initializer"></a>DotNet\_stili\_object_initializer

|||
|-|-|
| **Kural adı** | dotnet_style_object_initializer |
| **Kural KIMLIĞI** | IDE0017 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Mümkün olduğunda nesne başlatıcıları kullanılarak başlatılacak nesneleri tercih et<br /><br />`false`-Nesne başlatıcıları kullanarak *başlatılmayan* nesneleri tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

#### <a name="dotnet_style_collection_initializer"></a>DotNet\_stili\_collection_initializer

|||
|-|-|
| **Kural adı** | dotnet_style_collection_initializer |
| **Kural KIMLIĞI** | IDE0028 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Koleksiyonları mümkün olduğunda koleksiyon başlatıcıları kullanılarak başlatılacak şekilde tercih et<br /><br />`false`-Koleksiyonların koleksiyon başlatıcıları kullanılarak başlatılmamaları tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

#### <a name="dotnet_style_explicit_tuple_names"></a>DotNet\_stili\_açıktuple_names\_

|||
|-|-|
| **Kural adı** | dotnet_style_explicit_tuple_names |
| **Kural KIMLIĞI** | IDE0033 |
| **Uygun diller** | C#7.0 + ve Visual Basic 15 + |
| **Değerler** | `true`-Demet adlarını IMX özelliklerine tercih et<br /><br />`false`-Tür tanımlama alanları için IMX özelliklerini tercih edin |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

#### <a name="dotnet_style_prefer_inferred_tuple_names"></a>DotNet\_\_stili,çıkarılan\_tuple_names tercih eder\_

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_inferred_tuple_names |
| **Kural KIMLIĞI** | IDE0037 |
| **Uygun diller** | C#7.1 + ve Visual Basic 15 + |
| **Değerler** | `true`-Gösterilen demet öğesi adlarını tercih et<br /><br />`false`-Açık demet öğesi adlarını tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15.6 |

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

#### <a name="dotnet_style_prefer_inferred_anonymous_type_member_names"></a>DotNet\_\_stili,gösterilen\_anonimtür\_member_namestercih et\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_inferred_anonymous_type_member_names |
| **Kural KIMLIĞI** | IDE0037 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Gösterilen anonim türdeki üye adlarını tercih et<br /><br />`false`-Açık anonim tür üye adlarını tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15.6 |

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

#### <a name="dotnet_style_prefer_auto_properties"></a>DotNet\_\_stili\_otomatiközellikleritercih\_eder

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_auto_properties |
| **Kural KIMLIĞI** | IDE0032 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Özel yedekleme alanları olan özellikler üzerinde oto özellikleri tercih et<br /><br />`false`-Gizli özellikler üzerinde özel yedekleme alanları içeren özellikleri tercih edin |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |

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

#### <a name="dotnet_style_prefer_is_null_check_over_reference_equality_method"></a>DotNet\_\_\_stili,başvuru\_eşitlik\_yönteminin üzerinde null denetimi olmasını tercih ediyor\_\_\_\_

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_is_null_check_over_reference_equality_method |
| **Kural KIMLIĞI** | IDE0041 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-İle bir null denetimi kullanmayı tercih edin`object.ReferenceEquals`<br /><br />`false`-Desenler `object.ReferenceEquals` eşleme ile null denetimi tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |

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

#### <a name="dotnet_style_prefer_conditional_expression_over_assignment"></a>DotNet\_\_stili,koşullu\_ifadeover_assignment\_tercih eder\_

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_conditional_expression_over_assignment |
| **Kural KIMLIĞI** | IDE0045 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-İf-else bildiriminde Üçlü koşullu olarak atamaları tercih edin<br /><br />`false`-Üçlü koşullu bir if-else ifadesiyle atamaları tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,8 |

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

#### <a name="dotnet_style_prefer_conditional_expression_over_return"></a>DotNet\_\_stili,koşullu\_ifadeover_return\_tercih eder\_

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_conditional_expression_over_return |
| **Kural KIMLIĞI** | IDE0046 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Return deyimlerini bir if-else deyimi üzerinde Üçlü koşullu olarak kullanmak için tercih et<br /><br />`false`-Return deyimlerini, Üçlü koşullu koşullu bir if-else deyimi kullanacak şekilde tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,8 |

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

#### <a name="dotnet_style_prefer_compound_assignment"></a>DotNet\_\_stili\_bileşikatamayıtercih\_eder

|||
|-|-|
| **Kural adı** | dotnet_style_prefer_compound_assignment |
| **Kural KIMLIĞI** | IDE0054 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`- [Bileşik atama](/dotnet/csharp/language-reference/operators/assignment-operator#compound-assignment) ifadelerini tercih et<br /><br />`false`-Bileşik atama ifadelerini tercih etmeyin |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// dotnet_style_prefer_compound_assignment = true
x += 1;

// dotnet_style_prefer_compound_assignment = false
x = x + 1;
```

```vb
' dotnet_style_prefer_compound_assignment = true
x += 1

' dotnet_style_prefer_compound_assignment = false
x = x + 1
```

### <a name="null-checking-preferences"></a>Null denetleme tercihleri

Bu bölümdeki stil kuralları null denetleme tercihleri ile ilgilendirin.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

```ini
# CSharp and Visual Basic code style settings:
[*.{cs,vb}]
dotnet_style_coalesce_expression = true:suggestion
dotnet_style_null_propagation = true:suggestion
```

#### <a name="dotnet_style_coalesce_expression"></a>DotNet\_stili\_coalesce_expression

|||
|-|-|
| **Kural adı** | dotnet_style_coalesce_expression |
| **Kural KIMLIĞI** | IDE0029 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `true`-Üçlü operatör denetimi için null birleşim ifadeleri tercih et<br /><br />`false`-Üçlü işleç denetimini null birleştirme ifadelerine göre tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

#### <a name="dotnet_style_null_propagation"></a>DotNet\_stili\_null_propagation

|||
|-|-|
| **Kural adı** | dotnet_style_null_propagation |
| **Kural KIMLIĞI** | IDE0031 |
| **Uygun diller** | C#6.0 + ve Visual Basic 14 + |
| **Değerler** | `true`-Mümkün olduğunda null koşullu işleç kullanmayı tercih et<br /><br />`false`-Mümkün olduğunda Üçlü null denetimi kullanmayı tercih eder |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

## <a name="net-code-quality-settings"></a>.NET kod kalitesi ayarları

Bu bölümdeki kalite kuralları hem hem de C# Visual Basic koduna uygulanır. Visual Studio tümleşik geliştirme ortamında (IDE) yerleşik olarak bulunan kod Çözümleyicileri yapılandırmak için kullanılırlar. Bir EditorConfig dosyası ile FxCop çözümleyicileri yapılandırma hakkında bilgi için bkz. [FxCop çözümleyicileri yapılandırma](../code-quality/configure-fxcop-analyzers.md).

- [Parametre tercihleri](#parameter-preferences)
  - DotNet\_kod\_kalitesikullanılmayan\_parametreler\_

### <a name="parameter-preferences"></a>Parametre tercihleri

Bu bölümdeki kalite kuralları Yöntem parametrelerine önem vermez.

Bu kurallar bir *. editorconfig* dosyasında aşağıdaki gibi görünebilir:

```ini
# CSharp and Visual Basic code quality settings:
[*.{cs,vb}]
dotnet_code_quality_unused_parameters = all:suggestion
```

#### <a name="dotnet_code_quality_unused_parameters"></a>DotNet\_kod\_kalitesikullanılmayan\_parametreler\_

|||
|-|-|
| **Kural adı** | dotnet_code_quality_unused_parameters |
| **Kural KIMLIĞI** | IDE0060 |
| **Uygun diller** | C# ve Visual Basic |
| **Değerler** | `all`-Kullanılmayan parametreleri içeren herhangi bir erişilebilirliğe sahip bayrak yöntemleri<br /><br />`non_public`-Yalnızca kullanılmayan parametreleri içeren genel olmayan metotları işaretle |
| **Visual Studio varsayılanı** | `all:suggestion` |

Kod örnekleri:

```csharp
// dotnet_code_quality_unused_parameters = all:suggestion
public int GetNum() { return 1; }

// dotnet_code_quality_unused_parameters = non_public:suggestion
public int GetNum(int arg1) { return 1; }
```

```vb
' dotnet_code_quality_unused_parameters = all:suggestion
Public Function GetNum()
    Return 1
End Function

' dotnet_code_quality_unused_parameters = non_public:suggestion
Public Function GetNum(arg1 As Integer)
    Return 1
End Function
```

## <a name="c-code-style-settings"></a>C#kod stili ayarları

Bu bölümdeki stil kuralları yalnızca için C# geçerlidir.

- [Örtük ve açık türler](#implicit-and-explicit-types)
  - oluşturulan\_\_in_typesiçinCSharp\_Style var\_\_
  - is_apparent\_\_\_türündeCSharp\_stili var\_
  - CSharp\_Style\_var_elsewhere
- [İfade gövdeli üyeler](#expression-bodied-members)
  - csharp\_style\_expression\_bodied_methods
  - CSharp\_Style\_ifadesibodied_constructors\_
  - CSharp\_Style\_ifadesibodied_operators\_
  - CSharp\_Style\_ifadesibodied_properties\_
  - CSharp\_Style\_ifadesibodied_indexers\_
  - CSharp\_Style\_ifadesibodied_accessors\_
  - CSharp\_Style\_ifadesibodied_lambdas\_
  - CSharp\_Style\_ifadesigövdelilocal_functions\_\_
- [Desen eşleştirme](#pattern-matching)
  - cast_check\_\_\_ileeşleşen\_CSharp Style Model desenli\_\_\_
  - null_check\_ile\_birlikte\_farklıCSharpstili\_modelkarşılaştırması\_\_\_
- [Satır içi değişken bildirimleri](#inlined-variable-declarations)
  - CSharp\_stili\_satıriçi\_variable_declaration
- [İfade düzeyi tercihleri](#c-expression-level-preferences)
  - csharp\_prefer\_simple\_default_expression
- ["Null" Denetim tercihleri](#c-null-checking-preferences)
  - csharp\_style\_throw_expression
  - CSharp\_stili\_koşulludelegate_call\_
- [Kod bloğu tercihleri](#code-block-preferences)
  - CSharp\_prefer_braces
- [Kullanılmayan değer tercihleri](#unused-value-preferences)
  - CSharp\_stili\_kullanılmamış\_değerifadesistatement_preference\_\_
  - CSharp\_stili\_kullanılmayandeğer\_assignment_preference\_
- [Dizin ve Aralık tercihleri](#index-and-range-preferences)
  - CSharp\_\_stili\_index_operator tercih et
  - CSharp\_\_stili\_range_operator tercih et
- [Çeşitli tercihler](#miscellaneous-preferences)
  - CSharp\_stili\_ayrıştırılmışvariable_declaration\_
  - anonymous_function\_üzerinde\_YerelCSharp\_stil kalıbı\_\_
  - \_yönerge\_yerleşiminikullanan\_CSharp
  - CSharp\_\_statiklocal_function\_tercih et
  - CSharp\_\_basitusing_statement\_tercih et
  - CSharp\_\_stili\_switch_expression tercih et

### <a name="implicit-and-explicit-types"></a>Örtük ve açık türler

Bu bölümdeki stil kuralları, [var](/dotnet/csharp/language-reference/keywords/var) olan anahtar sözcüğünün kullanımını ve değişken bildiriminde açık bir tür ile ilgilendirin. Bu kural, türü görünür olduğunda ve başka bir yerde yerleşik türlere ayrı olarak uygulanabilir.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_var_for_built_in_types = true:suggestion
csharp_style_var_when_type_is_apparent = true:suggestion
csharp_style_var_elsewhere = true:suggestion
```

#### <a name="csharp_style_var_for_built_in_types"></a>oluşturulan\_\_in_typesiçinCSharp\_Style var\_\_

|||
|-|-|
| **Kural adı** | csharp_style_var_for_built_in_types |
| **Kural KIMLIĞI** | IDE0007 ve IDE0008 |
| **Uygun diller** | C#  |
| **Değerler** | `true`-Tercih `var` , gibi yerleşik sistem türleriyle değişkenleri bildirmek için kullanılır`int`<br /><br />`false`-Gibi yerleşik sistem türleriyle `var` değişkenleri bildirmek için açık türü tercih et`int` |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_var_for_built_in_types = true
var x = 5;

// csharp_style_var_for_built_in_types = false
int x = 5;
```

#### <a name="csharp_style_var_when_type_is_apparent"></a>is_apparent\_\_\_türündeCSharp\_stili var\_

|||
|-|-|
| **Kural adı** | csharp_style_var_when_type_is_apparent |
| **Kural KIMLIĞI** | IDE0007 ve IDE0008 |
| **Uygun diller** | C#  |
| **Değerler** | `true`-Tür `var` , bir bildirim ifadesinin sağ tarafında zaten bahsedildiğinde tercih edilir<br /><br />`false`-Tür, bir bildirim `var` ifadesinin sağ tarafında zaten bahsedildiğinde açık türü tercih et |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_var_when_type_is_apparent = true
var obj = new Customer();

// csharp_style_var_when_type_is_apparent = false
Customer obj = new Customer();
```

#### <a name="csharp_style_var_elsewhere"></a>CSharp\_Style\_var_elsewhere

|||
|-|-|
| **Kural adı** | csharp_style_var_elsewhere |
| **Kural KIMLIĞI** | IDE0007 ve IDE0008 |
| **Uygun diller** | C#  |
| **Değerler** | `true`-Başka `var` bir kod stili kural tarafından geçersiz kılınmadıkça tüm durumlarda açık tür üzerinde tercih yapın<br /><br />`false`-Başka bir kod stili `var` kuralı tarafından geçersiz kılınmadığı müddetçe, her durumda açık tür üzerinde tercih yapın |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_var_elsewhere = true
var f = this.Init();

// csharp_style_var_elsewhere = false
bool f = this.Init();
```

### <a name="expression-bodied-members"></a>İfade gövdeli üyeler

Bu bölümdeki stil kuralları, mantık tek bir ifadeden oluşur [ifadesi Bodied üyelerin](/dotnet/csharp/programming-guide/statements-expressions-operators/expression-bodied-members) kullanımına neden olabilir. Bu kural metotlar, oluşturucular, işleçler, özellikler, Dizin oluşturucular ve erişimciler için uygulanabilir.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_expression_bodied_methods = false:silent
csharp_style_expression_bodied_constructors = false:silent
csharp_style_expression_bodied_operators = false:silent
csharp_style_expression_bodied_properties = true:suggestion
csharp_style_expression_bodied_indexers = true:suggestion
csharp_style_expression_bodied_accessors = true:suggestion
csharp_style_expression_bodied_lambdas = true:silent
csharp_style_expression_bodied_local_functions = false:silent
```

#### <a name="csharp_style_expression_bodied_methods"></a>csharp\_style\_expression\_bodied_methods

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_methods |
| **Kural KIMLIĞI** | IDE0022 |
| **Uygun diller** | C#6.0 +  |
| **Değerler** | `true`-Yöntemler için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek bir çizgi olabilecekleri yöntemler için ifade gövdeleri tercih edin<br /><br />`false`-Yöntemler için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_methods = true
public int GetAge() => this.Age;

// csharp_style_expression_bodied_methods = false
public int GetAge() { return this.Age; }
```

#### <a name="csharp_style_expression_bodied_constructors"></a>CSharp\_Style\_ifadesibodied_constructors\_

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_constructors |
| **Kural KIMLIĞI** | IDE0021 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Oluşturucular için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satır olabilecekleri oluşturucular için ifade gövdeleri tercih et<br /><br />`false`-Oluşturucular için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_constructors = true
public Customer(int age) => Age = age;

// csharp_style_expression_bodied_constructors = false
public Customer(int age) { Age = age; }
```

#### <a name="csharp_style_expression_bodied_operators"></a>CSharp\_Style\_ifadesibodied_operators\_

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_operators |
| **Kural KIMLIĞI** | IDE0023 ve IDE0024 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-İşleçler için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satırlarsa işleçler için ifade gövdeleri tercih eder<br /><br />`false`-İşleçler için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_operators = true
public static ComplexNumber operator + (ComplexNumber c1, ComplexNumber c2)
    => new ComplexNumber(c1.Real + c2.Real, c1.Imaginary + c2.Imaginary);

// csharp_style_expression_bodied_operators = false
public static ComplexNumber operator + (ComplexNumber c1, ComplexNumber c2)
{ return new ComplexNumber(c1.Real + c2.Real, c1.Imaginary + c2.Imaginary); }
```

#### <a name="csharp_style_expression_bodied_properties"></a>CSharp\_Style\_ifadesibodied_properties\_

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_properties |
| **Kural KIMLIĞI** | IDE0025 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Özellikler için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satırlarsa özellikler için ifade gövdeleri tercih eder<br /><br />`false`-Özellikler için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_properties = true
public int Age => _age;

// csharp_style_expression_bodied_properties = false
public int Age { get { return _age; }}
```

#### <a name="csharp_style_expression_bodied_indexers"></a>CSharp\_Style\_ifadesibodied_indexers\_

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_indexers |
| **Kural KIMLIĞI** | IDE0026 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Dizin oluşturucular için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satır olacak şekilde Dizin oluşturucular için ifade gövdeleri tercih edin<br /><br />`false`-Dizin oluşturucular için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_indexers = true
public T this[int i] => _values[i];

// csharp_style_expression_bodied_indexers = false
public T this[int i] { get { return _values[i]; } }
```

#### <a name="csharp_style_expression_bodied_accessors"></a>CSharp\_Style\_ifadesibodied_accessors\_

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_accessors |
| **Kural KIMLIĞI** | IDE0027 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Erişimciler için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satır olabilecekleri erişimcileri için ifade gövdeleri tercih et<br /><br />`false`-Erişimciler için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_accessors = true
public int Age { get => _age; set => _age = value; }

// csharp_style_expression_bodied_accessors = false
public int Age { get { return _age; } set { _age = value; } }
```

#### <a name="csharp_style_expression_bodied_lambdas"></a>CSharp\_Style\_ifadesibodied_lambdas\_

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_lambdas |
| **Kural KIMLIĞI** | IDE0053 |
| **Değerler** | `true`-Lambdalar için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satırlarsa Lambdalar için ifade gövdeleri tercih eder<br /><br />`false`-Lambdalar için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_lambdas = true
Func<int, int> square = x => x * x;

// csharp_style_expression_bodied_lambdas = false
Func<int, int> square = x => { return x * x; };
```

#### <a name="csharp_style_expression_bodied_local_functions"></a>CSharp\_Style\_ifadesigövdelilocal_functions\_\_

7,0 ile C# başlayarak C# [Yerel işlevleri](/dotnet/csharp/programming-guide/classes-and-structs/local-functions)destekler. Yerel işlevler, başka bir üyede iç içe yerleştirilmiş bir türün özel yöntemleridir.

|||
|-|-|
| **Kural adı** | csharp_style_expression_bodied_local_functions |
| **Kural KIMLIĞI** | IDE0061 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Yerel işlevler için ifade gövdeleri tercih et<br /><br />`when_on_single_line`-Tek satırlarsa yerel işlevler için ifade gövdeleri tercih eder<br /><br />`false`-Yerel işlevler için blok gövdeleri tercih et |
| **Visual Studio varsayılanı** | `false:silent` |

Kod örnekleri:

```csharp
// csharp_style_expression_bodied_local_functions = true
void M()
{
    Hello();
    void Hello() => Console.WriteLine("Hello");
}

// csharp_style_expression_bodied_local_functions = false
void M()
{
    Hello();
    void Hello()
    {
        Console.WriteLine("Hello");
    }
}
```

### <a name="pattern-matching"></a>Desen eşleştirme

Bu bölümdeki stil kuralları ' de C# [model eşleme](/dotnet/csharp/pattern-matching) kullanımını sorun.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_pattern_matching_over_is_with_cast_check = true:suggestion
csharp_style_pattern_matching_over_as_with_null_check = true:suggestion
```

#### <a name="csharp_style_pattern_matching_over_is_with_cast_check"></a>cast_check\_\_\_ileeşleşen\_CSharp Style Model desenli\_\_\_

|||
|-|-|
| **Kural adı** | csharp_style_pattern_matching_over_is_with_cast_check |
| **Kural KIMLIĞI** | IDE0020 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Tür atamaları olan `is` ifadeler yerine kalıp eşleştirmeyi tercih et<br /><br />`false`-Tür `is` atamaları olan ifadeleri desenler eşleme yerine tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_pattern_matching_over_is_with_cast_check = true
if (o is int i) {...}

// csharp_style_pattern_matching_over_is_with_cast_check = false
if (o is int) {var i = (int)o; ... }
```

#### <a name="csharp_style_pattern_matching_over_as_with_null_check"></a>null_check\_ile\_birlikte\_farklıCSharpstili\_modelkarşılaştırması\_\_\_

|||
|-|-|
| **Kural adı** | csharp_style_pattern_matching_over_as_with_null_check |
| **Kural KIMLIĞI** | IDE0019 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Belirli bir türün bir şeyin `as` olup olmadığını anlamak için null denetimleri olan ifadeler yerine kalıp eşleştirmeyi tercih et<br /><br />`false`-Belirli `as` bir türün bir şeyin olup olmadığını anlamak için, desenler eşleme yerine null denetimleri olan ifadeler tercih edin |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_pattern_matching_over_as_with_null_check = true
if (o is string s) {...}

// csharp_style_pattern_matching_over_as_with_null_check = false
var s = o as string;
if (s != null) {...}
```

### <a name="inlined-variable-declarations"></a>Satır içi değişken bildirimleri

Bu stil kuralı, değişkenlerin `out` satır içi olarak verilip verilmeyeceğini belirtir. C# 7 ' den başlayarak, ayrı bir değişken bildiriminde değil, [yöntem çağrısının bağımsız değişken listesinde bir out değişkeni bildirebilirsiniz](/dotnet/csharp/language-reference/keywords/out-parameter-modifier#calling-a-method-with-an-out-argument).

#### <a name="csharp_style_inlined_variable_declaration"></a>CSharp\_stili\_satıriçi\_variable_declaration

|||
|-|-|
| **Kural adı** | csharp_style_inlined_variable_declaration |
| **Kural KIMLIĞI** | IDE0018 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Mümkün `out` olduğunda bir yöntem çağrısının bağımsız değişken listesinde satır içi olarak belirtilecek değişkenleri tercih et<br /><br />`false`-Yöntem `out` çağrısından önce belirtilecek değişkenleri tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_inlined_variable_declaration = true
if (int.TryParse(value, out int i) {...}

// csharp_style_inlined_variable_declaration = false
int i;
if (int.TryParse(value, out i) {...}
```

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_inlined_variable_declaration = true:suggestion
```

### <a name="c-expression-level-preferences"></a>C#ifade düzeyi tercihleri

Bu bölümdeki stil kuralları, ifade düzeyi tercihlerine önem vermez.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_prefer_simple_default_expression = true:suggestion
```

#### <a name="csharp_prefer_simple_default_expression"></a>csharp\_prefer\_simple\_default_expression

Bu stil kuralı, derleyici ifadenin türünü çıkarsandığı zaman [ `default` varsayılan değer ifadeleri için değişmez değeri](/dotnet/csharp/programming-guide/statements-expressions-operators/default-value-expressions#default-literal-and-type-inference) kullanılarak ilgilidir.

|||
|-|-|
| **Kural adı** | csharp_prefer_simple_default_expression |
| **Kural KIMLIĞI** | IDE0034 |
| **Uygun diller** | C#7.1 +  |
| **Değerler** | `true`-Tercih `default` et`default(T)`<br /><br />`false`-Tercih `default(T)` et`default` |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_prefer_simple_default_expression = true
void DoWork(CancellationToken cancellationToken = default) { ... }

// csharp_prefer_simple_default_expression = false
void DoWork(CancellationToken cancellationToken = default(CancellationToken)) { ... }
```

### <a name="c-null-checking-preferences"></a>C#null denetleme tercihleri

Bu stil kuralları, `null` ifadelerin veya `throw` deyimlerin kullanımı `throw` dahil olmak üzere denetim etrafında sözdizimi sağlar ve bir null denetimi gerçekleştirip gerçekleştirmeyeceğinizi`?.`veya bir [ Lambda ifadesi](/dotnet/csharp/lambda-expressions).

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_throw_expression = true:suggestion
csharp_style_conditional_delegate_call = false:suggestion
```

#### <a name="csharp_style_throw_expression"></a>csharp\_style\_throw_expression

|||
|-|-|
| **Kural adı** | csharp_style_throw_expression |
| **Kural KIMLIĞI** | IDE0016 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Deyimler `throw` `throw` yerine ifadeler kullanmayı tercih et<br /><br />`false`- `throw` İfadeler`throw` yerine deyimleri kullanmayı tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_throw_expression = true
this.s = s ?? throw new ArgumentNullException(nameof(s));

// csharp_style_throw_expression = false
if (s == null) { throw new ArgumentNullException(nameof(s)); }
this.s = s;
```

#### <a name="csharp_style_conditional_delegate_call"></a>CSharp\_stili\_koşulludelegate_call\_

|||
|-|-|
| **Kural adı** | csharp_style_conditional_delegate_call |
| **Kural KIMLIĞI** | IDE0041 |
| **Uygun diller** | C#6.0 +  |
| **Değerler** | `true`-bir lambda ifadesi çağrılırken, null denetimi yapmak yerine`?.`koşullu birleştirme işlecini () kullanma konusuna bakın<br /><br />`false`-Koşullu birleştirme işlecini (`?.`) kullanmak yerine bir lambda ifadesini çağırmadan önce null denetimi gerçekleştirmeyi tercih eder |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_conditional_delegate_call = true
func?.Invoke(args);

// csharp_style_conditional_delegate_call = false
if (func != null) { func(args); }
```

### <a name="code-block-preferences"></a>Kod bloğu tercihleri

Bu stil kuralı, kod blokları çevrelemek için `{ }` küme ayraçları kullanımıyla ilgilidir.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_prefer_braces = true:silent
```

#### <a name="csharp_prefer_braces"></a>CSharp\_tercih\_edilen ayraçları

|||
|-|-|
| **Kural adı** | csharp_prefer_braces |
| **Kural KIMLIĞI** | IDE0011 |
| **Uygun diller** | C# |
| **Değerler** | `true`-Bir kod satırı için bile küme ayraçları tercih et<br /><br />`false`-İzin veriliyorsa küme ayracı olmadan tercih edin |
| **Visual Studio varsayılanı** | `true:silent` |

Kod örnekleri:

```csharp
// csharp_prefer_braces = true
if (test) { this.Display(); }

// csharp_prefer_braces = false
if (test) this.Display();
```

### <a name="unused-value-preferences"></a>Kullanılmayan değer tercihleri

Bu stil kuralları kullanılmayan ifadelere ve değer atamalarına sorun.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_unused_value_expression_statement_preference = discard_variable:silent
csharp_style_unused_value_assignment_preference = discard_variable:suggestion
```

#### <a name="csharp_style_unused_value_expression_statement_preference"></a>csharp_style_unused_value_expression_statement_preference

|||
|-|-|
| **Kural adı** | csharp_style_unused_value_expression_statement_preference |
| **Kural KIMLIĞI** | IDE0058 |
| **Uygun diller** | C# |
| **Değerler** | `discard_variable`-Bir [atma](/dotnet/csharp/discards) için kullanılmamış bir ifade atamayı tercih et <br /><br />`unused_local_variable`-Kullanılmayan bir ifadeyi yerel bir değişkene atamayı tercih et |
| **Visual Studio varsayılanı** | `discard_variable:silent` |

Kod örnekleri:

```csharp
// Original code:
System.Convert.ToInt32("35");

// After code fix for IDE0058:

// csharp_style_unused_value_expression_statement_preference = discard_variable
_ = System.Convert.ToInt32("35");

// csharp_style_unused_value_expression_statement_preference = unused_local_variable
var unused = Convert.ToInt32("35");
```

#### <a name="csharp_style_unused_value_assignment_preference"></a>csharp_style_unused_value_assignment_preference

|||
|-|-|
| **Kural adı** | csharp_style_unused_value_assignment_preference |
| **Kural KIMLIĞI** | IDE0059 |
| **Uygun diller** | C# |
| **Değerler** | `discard_variable`-Kullanılmayan bir değer atarken [atmayı](/dotnet/csharp/discards) kullanmayı tercih et<br /><br />`unused_local_variable`-Kullanılmayan bir değer atarken yerel bir değişken kullanmayı tercih et |
| **Visual Studio varsayılanı** | `discard_variable:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_unused_value_assignment_preference = discard_variable
int GetCount(Dictionary<string, int> wordCount, string searchWord)
{
    _ = wordCount.TryGetValue(searchWord, out var count);
    return count;
}

// csharp_style_unused_value_assignment_preference = unused_local_variable
int GetCount(Dictionary<string, int> wordCount, string searchWord)
{
    var unused = wordCount.TryGetValue(searchWord, out var count);
    return count;
}
```

### <a name="index-and-range-preferences"></a>Dizin ve Aralık tercihleri

Bu stil kuralları, C# 8,0 ve üzeri sürümlerde kullanılabilen dizin ve Aralık işleçleri kullanımını sorun.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_prefer_index_operator = true:suggestion
csharp_style_prefer_range_operator = true:suggestion
```

#### <a name="csharp_style_prefer_index_operator"></a>CSharp\_\_stili\_index_operator tercih et

|||
|-|-|
| **Kural adı** | csharp_style_prefer_index_operator |
| **Kural KIMLIĞI** | IDE0056 |
| **Uygun diller** | C#8.0 + |
| **Değerler** | `true`-Bir koleksiyonun sonundan bir `^` Dizin hesaplarken işleci kullanmayı tercih eder<br /><br />`false`-Bir koleksiyonun sonundan bir dizin `^` hesaplarken işleci kullanmayı tercih etmeyin |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_prefer_index_operator = true
string[] names = { "Archimedes", "Pythagoras", "Euclid" };
var index = names[^1];

// csharp_style_prefer_index_operator = false
string[] names = { "Archimedes", "Pythagoras", "Euclid" };
var index = names[names.Length - 1];
```

#### <a name="csharp_style_prefer_range_operator"></a>CSharp\_\_stili\_range_operator tercih et

|||
|-|-|
| **Kural adı** | csharp_style_prefer_range_operator |
| **Kural KIMLIĞI** | IDE0057 |
| **Uygun diller** | C#8.0 + |
| **Değerler** | `true`-Bir koleksiyonun "dilimini" ayıkladığınızda Range işlecini `..` kullanmayı tercih et<br /><br />`false`-Bir koleksiyonun "dilimini" ayıkladığınızda `..` Range işlecini kullanmayı tercih etmeyin |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_style_prefer_range_operator = true
string sentence = "the quick brown fox";
var sub = sentence[0..^4];

// csharp_style_prefer_range_operator = false
string sentence = "the quick brown fox";
var sub = sentence.Substring(0, sentence.Length - 4);
```

### <a name="miscellaneous-preferences"></a>Çeşitli tercihler

Bu bölüm çeşitli stil kurallarını içerir.

Örnek *. editorconfig* dosyası:

```ini
# CSharp code style settings:
[*.cs]
csharp_style_deconstructed_variable_declaration = true:suggestion
csharp_style_pattern_local_over_anonymous_function = true:suggestion
csharp_using_directive_placement = outside_namespace:silent
csharp_prefer_static_local_function = true:suggestion
csharp_prefer_simple_using_statement = true:suggestion
csharp_style_prefer_switch_expression = true:suggestion
```

#### <a name="csharp_style_deconstructed_variable_declaration"></a>CSharp\_stili\_ayrıştırılmışvariable_declaration\_

|||
|-|-|
| **Kural adı** | csharp_style_deconstructed_variable_declaration |
| **Kural KIMLIĞI** | IDE0042 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Oluşturulmuş değişken bildirimini tercih et<br /><br />`false`-Değişken bildirimlerinde oluşturmayı tercih etme |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

#### <a name="csharp_style_pattern_local_over_anonymous_function"></a>anonymous_function\_üzerinde\_YerelCSharp\_stil kalıbı\_\_

7,0 ile C# başlayarak C# [Yerel işlevleri](/dotnet/csharp/programming-guide/classes-and-structs/local-functions)destekler. Yerel işlevler, başka bir üyede iç içe yerleştirilmiş bir türün özel yöntemleridir.

|||
|-|-|
| **Kural adı** | csharp_style_pattern_local_over_anonymous_function |
| **Kural KIMLIĞI** | IDE0039 |
| **Uygun diller** | C#7.0 + |
| **Değerler** | `true`-Anonim işlevler üzerinde yerel işlevleri tercih et<br /><br />`false`-Yerel işlevler üzerinde anonim işlevleri tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |

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

#### <a name="csharp_using_directive_placement"></a>directive_placement\_kullanarak\_CSharp

|||
|-|-|
| **Kural adı** | csharp_using_directive_placement |
| **Kural KIMLIĞI** | IDE0065 |
| **Uygun diller** | C# |
| **Değerler** | `outside_namespace`-Ad `using` alanının dışına yerleştirilecek yönergeleri tercih et<br /><br />`inside_namespace`-Ad `using` alanının içine yerleştirilecek yönergeleri tercih et |
| **Visual Studio varsayılanı** | `outside_namespace:silent` |

Kod örnekleri:

```csharp
// csharp_using_directive_placement = outside_namespace
using System;

namespace Conventions
{
    ...
}

// csharp_using_directive_placement = inside_namespace
namespace Conventions
{
    using System;
    ...
}
```

#### <a name="csharp_prefer_static_local_function"></a>CSharp\_\_statiklocal_function\_tercih et

|||
|-|-|
| **Kural adı** | csharp_prefer_static_local_function |
| **Kural KIMLIĞI** | IDE0062 |
| **Uygun diller** | C#8.0 + |
| **Değerler** | `true`-Yerel işlevlerin işaretlenmesini tercih et`static`<br /><br />`false`-Yerel işlevlerin işaretlenmesini tercih etmeyin`static` |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_prefer_static_local_function = true
void M()
{
    Hello();
    static void Hello()
    {
        Console.WriteLine("Hello");
    }
}

// csharp_prefer_static_local_function = false
void M()
{
    Hello();
    void Hello()
    {
        Console.WriteLine("Hello");
    }
}
```

#### <a name="csharp_prefer_simple_using_statement"></a>CSharp\_\_basitusing_statement\_tercih et

|||
|-|-|
| **Kural adı** | csharp_prefer_simple_using_statement |
| **Kural KIMLIĞI** | IDE0063 |
| **Uygun diller** | C#8.0 + |
| **Değerler** | `true`- *Basit* `using` bir ifade kullanmayı tercih et<br /><br />`false`- *Basit* `using` bir ifade kullanmayı tercih etmeyin |
| **Visual Studio varsayılanı** | `true:suggestion` |

Kod örnekleri:

```csharp
// csharp_prefer_simple_using_statement = true
using var a = b;

// csharp_prefer_simple_using_statement = false
using (var a = b) { }
```

#### <a name="csharp_style_prefer_switch_expression"></a>CSharp\_\_stili\_switch_expression tercih et

|||
|-|-|
| **Kural adı** | csharp_style_prefer_switch_expression |
| **Kural KIMLIĞI** | IDE0066 |
| **Uygun diller** | C#8.0 + |
| **Değerler** | `true`-Bir `switch` ifade kullanmayı tercih et (8,0 ile C# tanıtılan)<br /><br />`false`- [Switch ifadesinin](/dotnet/csharp/language-reference/keywords/switch) kullanılmasını tercih et |
| **Visual Studio varsayılanı** | `true:suggestion` |
| **Tanıtılan sürüm** | Visual Studio 2019 sürüm 16,2 |

Kod örnekleri:

```csharp
// csharp_style_prefer_switch_expression = true
return x switch
{
    1 => 1 * 1,
    2 => 2 * 2,
    _ => 0,
};

// csharp_style_prefer_switch_expression = false
switch (x)
{
    case 1:
        return 1 * 1;
    case 2:
        return 2 * 2;
    default:
        return 0;
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Biçimlendirme kuralları](editorconfig-formatting-conventions.md)
- [Adlandırma kuralları](editorconfig-naming-conventions.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](editorconfig-code-style-settings-reference.md)
