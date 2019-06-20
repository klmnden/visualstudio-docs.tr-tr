---
title: EditorConfig için .NET biçimlendirme kuralları
ms.date: 06/17/2019
ms.topic: reference
dev_langs:
- CSharp
- VB
helpviewer_keywords:
- formatting conventions [EditorConfig]
author: gewarren
ms.author: gewarren
manager: jillfra
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 340d8ca7f7b578ae952c0b5024cd6962f20a0dff
ms.sourcegitcommit: b468d71052a1b8a697f477ab23a3644de139f1e9
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/19/2019
ms.locfileid: "67262831"
---
# <a name="formatting-conventions"></a>Biçimlendirme kuralları

Visual Studio için EditorConfig için biçimlendirme kurallarını iki kategoriye ayrılır:

- [.NET biçimlendirme ayarları](#net-formatting-settings)

- [C# biçimlendirme ayarları](#c-formatting-settings)

## <a name="rule-format"></a>Kural biçimi

Biçimlendirme kurallarını kuralları aşağıdaki biçime sahiptir:

`rule_name = value`

Birçok kuralları için ya da belirttiğiniz `true` (Bu stil tercih et) veya `false` (Bu stil tercih ediyorsunuz) için `value`. Diğer kuralları için bir değer gibi belirttiğiniz `flush_left` veya `before_and_after` kuralının nerde ve ne zaman tanımlamak için. Bir önem derecesi belirtmeyin.

## <a name="net-formatting-settings"></a>.NET biçimlendirme ayarları

Bu bölümdeki biçimlendirme kurallarını uygulamak C# ve Visual Basic kodu.

- [Using'leri düzenleme](#organize-using-directives)
   - dotnet_sort_system_directives_first
   - dotnet_separate_import_directive_groups

### <a name="organize-using-directives"></a>Using yönergelerini düzenleme

Bu biçimlendirme kurallarını sıralama ilgilendiriyor ve görüntüsünü `using` yönergeleri ve `Imports` deyimleri.

Örnek *.editorconfig* dosyası:

```ini
# .NET formatting settings
[*.{cs,vb}]
dotnet_sort_system_directives_first = true
dotnet_separate_import_directive_groups = true
```

#### <a name="dotnetsortsystemdirectivesfirst"></a>DotNet\_sıralama\_sistem\_directives_first

|||
|-|-|
| **Kural adı** | dotnet_sort_system_directives_first |
| **Geçerli diller** | C# ve Visual Basic |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -System.* sıralama `using` yönergeleri alfabetik olarak ve diğer önce yerleştirin yönergeleri kullanarak.<br /><br />`false` -System.* yerleştirmeyin `using` önce diğer yönergeleri `using` yönergeleri. |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// dotnet_sort_system_directives_first = true
using System.Collections.Generic;
using System.Threading.Tasks;
using Octokit;

// dotnet_sort_system_directives_first = false
using System.Collections.Generic;
using Octokit;
using System.Threading.Tasks;
```

#### <a name="dotnetseparateimportdirectivegroups"></a>DotNet\_ayrı\_alma\_yönergesi\_grupları

|||
|-|-|
| **Kural adı** | dotnet_separate_import_directive_groups |
| **Geçerli diller** | C# ve Visual Basic |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.5 |
| **Değerler** | `true` -Arasına boş bir satır yerleştirin `using` yönerge gruplarını.<br /><br />`false` -Boş bir satır arasında yerleştirmeyin `using` yönerge gruplarını. |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// dotnet_separate_import_directive_groups = true
using System.Collections.Generic;
using System.Threading.Tasks;

using Octokit;

// dotnet_separate_import_directive_groups = false
using System.Collections.Generic;
using System.Threading.Tasks;
using Octokit;
```

## <a name="c-formatting-settings"></a>C# biçimlendirme ayarları

Yalnızca C# kodu için bu bölümdeki biçimlendirme kurallarını uygulayın.

- [Yeni satır seçenekleri](#new-line-options)
   - csharp_new_line_before_open_brace
   - csharp_new_line_before_else
   - csharp_new_line_before_catch
   - csharp_new_line_before_finally
   - csharp_new_line_before_members_in_object_initializers
   - csharp_new_line_before_members_in_anonymous_types
   - csharp_new_line_between_query_expression_clauses
- [Girintileme seçenekleri](#indentation-options)
   - csharp_indent_case_contents
   - csharp_indent_switch_labels
   - csharp_indent_labels
- [Aralık Seçenekleri](#spacing-options)
   - csharp_space_after_cast
   - csharp_space_after_keywords_in_control_flow_statements
   - csharp_space_between_method_declaration_parameter_list_parentheses
   - csharp_space_between_method_call_parameter_list_parentheses
   - csharp_space_between_parentheses
   - csharp_space_before_colon_in_inheritance_clause
   - csharp_space_after_colon_in_inheritance_clause
   - csharp_space_around_binary_operators
   - csharp_space_between_method_declaration_empty_parameter_list_parentheses
   - csharp_space_between_method_call_name_and_opening_parenthesis
   - csharp_space_between_method_call_empty_parameter_list_parentheses
   - csharp_space_after_comma
   - csharp_space_after_dot
- [Kaydırma seçenekleri](#wrap-options)
   - csharp_preserve_single_line_statements
   - csharp_preserve_single_line_blocks

### <a name="new-line-options"></a>Yeni satır seçenekleri

Bu biçimlendirme kurallarını kod biçimlendirmek için yeni satırlar kullanımını ilgilendiriyor.

Örnek *.editorconfig* dosyası:

```ini
# CSharp formatting settings:
[*.cs]
csharp_new_line_before_open_brace = methods, properties, control_blocks, types
csharp_new_line_before_else = true
csharp_new_line_before_catch = true
csharp_new_line_before_finally = true
csharp_new_line_before_members_in_object_initializers = true
csharp_new_line_before_members_in_anonymous_types = true
csharp_new_line_between_query_expression_clauses = true
```

#### <a name="csharpnewlinebeforeopenbrace"></a>CSharp\_yeni\_satırı\_önce\_open_brace

Bu kural, bir açık küme ayracı olup olmadığını işlemiyle ilgili `{` projeler yukarıdaki kodla aynı satırda veya yeni bir satıra yerleştirilmelidir. Bu kural için belirttiğiniz **tüm**, **hiçbiri**, veya bir veya daha fazla öğe gibi kod **yöntemleri** veya **özellikleri**, ne zaman tanımlamak için bu kural uygulanmalıdır. Birden çok kod öğelerini belirtmek için virgül (,) ayırın.

|||
|-|-|
| **Kural adı** | csharp_new_line_before_open_brace |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `all` -Tüm ifadeler ("Allman" stil) için yeni bir satırdsa olacak şekilde küme ayraçları gerektirir.<br /><br />`none` -Küme ayraçları ("K & R") tüm ifadeler için aynı satırda olmasını gerektirir.<br /><br />`accessors`, `anonymous_methods`, `anonymous_types`, `control_blocks`, `events`, `indexers`, `lambdas`, `local_functions`, `methods`, `object_collection_array_initializers`, `properties`, `types` -İçin yeni bir satırdsa olacak şekilde küme ayraçları gerektirin Belirtilen kod öğesi ("Allman" stil). |
| **Visual Studio varsayılan** | `all` |

Kod örnekleri:

```csharp
// csharp_new_line_before_open_brace = all
void MyMethod()
{
    if (...)
    {
        ...
    }
}

// csharp_new_line_before_open_brace = none
void MyMethod() {
    if (...) {
        ...
    }
}
```

#### <a name="csharpnewlinebeforeelse"></a>CSharp\_yeni\_satırı\_before_else

|||
|-|-|
| **Kural adı** | csharp_new_line_before_else |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Yerleştirin `else` yeni bir satıra deyimleri.<br /><br />`false` -Yerleştirin `else` deyimleri aynı satırda. |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_new_line_before_else = true
if (...) {
    ...
}
else {
    ...
}

// csharp_new_line_before_else = false
if (...) {
    ...
} else {
    ...
}
```

#### <a name="csharpnewlinebeforecatch"></a>CSharp\_yeni\_satırı\_before_catch

|||
|-|-|
| **Kural adı** | csharp_new_line_before_catch |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Yerleştirin `catch` yeni bir satıra deyimleri.<br /><br />`false` -Yerleştirin `catch` deyimleri aynı satırda. |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_new_line_before_catch = true
try {
    ...
}
catch (Exception e) {
    ...
}

// csharp_new_line_before_catch = false
try {
    ...
} catch (Exception e) {
    ...
}
```

#### <a name="csharpnewlinebeforefinally"></a>CSharp\_yeni\_satırı\_before_finally

|||
|-|-|
| **Kural adı** | csharp_new_line_before_finally |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Gerekli `finally` kapatma küme ayracından sonra yeni bir satıra olmasını deyimleri.<br /><br />`false` -Gerekli `finally` kapanış küme ayracı ile aynı satırda olmasını deyimleri. |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_new_line_before_finally = true
try {
    ...
}
catch (Exception e) {
    ...
}
finally {
    ...
}

// csharp_new_line_before_finally = false
try {
    ...
} catch (Exception e) {
    ...
} finally {
    ...
}
```

#### <a name="csharpnewlinebeforemembersinobjectinitializers"></a>CSharp\_yeni\_satırı\_önce\_üyeleri\_içinde\_object_initializers

|||
|-|-|
| **Kural adı** | csharp_new_line_before_members_in_object_initializers |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Üyelerinin nesne başlatıcıları ayrı satırlarda olmasını gerektirir<br /><br />`false` -Aynı satırda bulunması için nesne başlatıcıları üyeleri gerektirir |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_new_line_before_members_in_object_initializers = true
var z = new B()
{
    A = 3,
    B = 4
}

// csharp_new_line_before_members_in_object_initializers = false
var z = new B()
{
    A = 3, B = 4
}
```

#### <a name="csharpnewlinebeforemembersinanonymoustypes"></a>CSharp\_yeni\_satırı\_önce\_üyeleri\_içinde\_anonymous_types

|||
|-|-|
| **Kural adı** | csharp_new_line_before_members_in_anonymous_types |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Ayrı satırlarda olmasını anonim türlerin üyelerini gerektirir<br /><br />`false` -Aynı satırda olmasını anonim türlerin üyelerini gerektirir |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_new_line_before_members_in_anonymous_types = true
var z = new
{
    A = 3,
    B = 4
}

// csharp_new_line_before_members_in_anonymous_types = false
var z = new
{
    A = 3, B = 4
}
```

#### <a name="csharpnewlinebetweenqueryexpressionclauses"></a>csharp_new_line_between_query_expression_clauses

|||
|-|-|
| **Kural adı** | csharp_new_line_between_query_expression_clauses |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Öğeleri sorgu ifadesi tümceleri ayrı satırlarda olmasını gerektirir<br /><br />`false` -Öğeleri sorgu ifadesi tümceleri aynı satırda olmasını gerektirir |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_new_line_between_query_expression_clauses = true
var q = from a in e
        from b in e
        select a * b;

// csharp_new_line_between_query_expression_clauses = false
var q = from a in e from b in e
        select a * b;
```

### <a name="indentation-options"></a>Girintileme seçenekleri

Bu biçimlendirme kuralları biçimi koda girinti kullanımını ilgilendiriyor.

Örnek *.editorconfig* dosyası:

```ini
# CSharp formatting settings:
[*.cs]
csharp_indent_case_contents = true
csharp_indent_switch_labels = true
csharp_indent_labels = flush_left
```

#### <a name="csharpindentcasecontents"></a>CSharp\_girinti\_case_contents

|||
|-|-|
| **Kural adı** | csharp_indent_case_contents |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Girintile `switch` case içerikleri<br /><br />`false` -Girinti değil `switch` case içerikleri |
| **Visual Studio varsayılan** | `true` |

- Bu kural ayarlandığında **true**, ediyorum.
- Bu kural ayarlandığında **false**, d.

Kod örnekleri:

```csharp
// csharp_indent_case_contents = true
switch(c) {
    case Color.Red:
        Console.WriteLine("The color is red");
        break;
    case Color.Blue:
        Console.WriteLine("The color is blue");
        break;
    default:
        Console.WriteLine("The color is unknown.");
        break;
}

// csharp_indent_case_contents = false
switch(c) {
    case Color.Red:
    Console.WriteLine("The color is red");
    break;
    case Color.Blue:
    Console.WriteLine("The color is blue");
    break;
    default:
    Console.WriteLine("The color is unknown.");
    break;
}
```

#### <a name="csharpindentswitchlabels"></a>CSharp\_girinti\_switch_labels

|||
|-|-|
| **Kural adı** | csharp_indent_switch_labels |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Girintile `switch` etiketleri<br /><br />`false` -Girinti değil `switch` etiketleri |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_indent_switch_labels = true
switch(c) {
    case Color.Red:
        Console.WriteLine("The color is red");
        break;
    case Color.Blue:
        Console.WriteLine("The color is blue");
        break;
    default:
        Console.WriteLine("The color is unknown.");
        break;
}

// csharp_indent_switch_labels = false
switch(c) {
case Color.Red:
    Console.WriteLine("The color is red");
    break;
case Color.Blue:
    Console.WriteLine("The color is blue");
    break;
default:
    Console.WriteLine("The color is unknown.");
    break;
}
```

#### <a name="csharpindentlabels"></a>CSharp\_indent_labels

|||
|-|-|
| **Kural adı** | csharp_indent_labels |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `flush_left` -Etiketleri en soldaki sütuna yerleştirilir.<br /><br />`one_less_than_current` -Etiketleri tek tek geçerli bağlam için daha az girinti yerleştirilir<br /><br />`no_change` -Etiketleri aynı girintisi geçerli bağlamı olarak yer alır |
| **Visual Studio varsayılan** | `no_change` |

Kod örnekleri:

```csharp
// csharp_indent_labels= flush_left
class C
{
    private string MyMethod(...)
    {
        if (...) {
            goto error;
        }
error:
        throw new Exception(...);
    }
}

// csharp_indent_labels = one_less_than_current
class C
{
    private string MyMethod(...)
    {
        if (...) {
            goto error;
        }
    error:
        throw new Exception(...);
    }
}

// csharp_indent_labels= no_change
class C
{
    private string MyMethod(...)
    {
        if (...) {
            goto error;
        }
        error:
        throw new Exception(...);
    }
}
```

### <a name="spacing-options"></a>Aralık Seçenekleri

Bu biçimlendirme kuralları koduna boşluk karakterleri kullanımını ilgilendiriyor.

Örnek *.editorconfig* dosyası:

```ini
# CSharp formatting settings:
[*.cs]
csharp_space_after_cast = true
csharp_space_after_keywords_in_control_flow_statements = true
csharp_space_between_method_declaration_parameter_list_parentheses = true
csharp_space_between_method_call_parameter_list_parentheses = true
csharp_space_between_parentheses = control_flow_statements, type_casts
csharp_space_before_colon_in_inheritance_clause = true
csharp_space_after_colon_in_inheritance_clause = true
csharp_space_around_binary_operators = before_and_after
csharp_space_between_method_declaration_empty_parameter_list_parentheses = false
csharp_space_between_method_call_name_and_opening_parenthesis = false
csharp_space_between_method_call_empty_parameter_list_parentheses = false
csharp_space_after_comma = true
csharp_space_after_dot = false
```

#### <a name="csharpspaceaftercast"></a>CSharp\_alanı\_after_cast

|||
|-|-|
| **Kural adı** | csharp_space_after_cast |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Bir dönüştürme ve değer arasında bir boşluk gerektirir<br /><br />`false` -Gerekli _hiçbir_ cast değeri arasındaki boşluk |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_after_cast = true
int y = (int) x;

// csharp_space_after_cast = false
int y = (int)x;
```

#### <a name="csharpspaceafterkeywordsincontrolflowstatements"></a>csharp_space_after_keywords_in_control_flow_statements

|||
|-|-|
| **Kural adı** | csharp_space_after_keywords_in_control_flow_statements |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Boşlukla sonra bir denetim akışı ifadesi içinde bir anahtar sözcüğü gibi gereken bir `for` döngü<br /><br />`false` -Gerekli _hiçbir_ gibi bir anahtar sözcüğü bir denetim akışı ifadesi içinde'sonra boşluk bir `for` döngü |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_space_after_keywords_in_control_flow_statements = true
for (int i;i<x;i++) { ... }

// csharp_space_after_keywords_in_control_flow_statements = false
for(int i;i<x;i++) { ... }
```

#### <a name="csharpspacebetweenmethoddeclarationparameterlistparentheses"></a>csharp_space_between_method_declaration_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_declaration_parameter_list_parentheses |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Yer açma parantezinden sonra ve bir yöntem bildiriminin parametre listesinin kapatma parantezinden önce bir boşluk karakteri<br /><br />`false` -Boşluk karakterleri açma parantezinden sonra ve kapatma parantezinden yöntemi bildirimi parametre listesini önce yerleştirmeyin |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_declaration_parameter_list_parentheses = true
void Bark( int x ) { ... }

// csharp_space_between_method_declaration_parameter_list_parentheses = false
void Bark(int x) { ... }
```

#### <a name="csharpspacebetweenmethodcallparameterlistparentheses"></a>csharp_space_between_method_call_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_call_parameter_list_parentheses |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Yer açma parantezinden sonra ve bir yöntem çağrısının kapatma parantezinden önce bir boşluk karakteri<br /><br />`false` -Boşluk karakterleri açma parantezinden sonra ve bir yöntem çağrısının kapatma parantezinden önce yerleştirmeyin |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_call_parameter_list_parentheses = true
MyMethod( argument );

// csharp_space_between_method_call_parameter_list_parentheses = false
MyMethod(argument);
```

#### <a name="csharpspacebetweenparentheses"></a>csharp_space_between_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_parentheses |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `control_flow_statements` -Denetim akışı deyimlerinin parantezler arasında boşluk koyun<br /><br />`expressions` -İfadelerin parantezler arasında boşluk koyun<br /><br />`type_casts` -Parantez içinde tür atamaları arasındaki boşluk koyun |
| **Visual Studio varsayılan** | `false` |

Bu kural atlayın veya dışında bir değer kullanın `control_flow_statements`, `expressions`, veya `type_casts`, ayar uygulanmaz.

Kod örnekleri:

```csharp
// csharp_space_between_parentheses = control_flow_statements
for ( int i = 0; i < 10; i++ ) { }

// csharp_space_between_parentheses = expressions
var z = ( x * y ) - ( ( y - x ) * 3 );

// csharp_space_between_parentheses = type_casts
int y = ( int )x;
```

#### <a name="csharpspacebeforecolonininheritanceclause"></a>CSharp\_alanı\_önce\_iki nokta üst üste\_içinde\_inheritance_clause

|||
|-|-|
| **Kural adı** | csharp_space_before_colon_in_inheritance_clause |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |
| **Değerler** | `true` -İki nokta üst üste için tabanları veya bir tür bildiriminde arabirimleri önce bir alan gerektirir<br /><br />`false` -Gerekli _hiçbir_ için iki nokta üst üste tabanları veya bir tür bildiriminde arabirimleri önce boşluk |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_space_before_colon_in_inheritance_clause = true
interface I
{

}

class C : I
{

}

// csharp_space_before_colon_in_inheritance_clause = false
interface I
{

}

class C: I
{

}
```

#### <a name="csharpspaceaftercolonininheritanceclause"></a>CSharp\_alanı\_sonra\_iki nokta üst üste\_içinde\_inheritance_clause

|||
|-|-|
| **Kural adı** | csharp_space_after_colon_in_inheritance_clause |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |
| **Değerler** | `true` -Tabanları için iki noktadan sonra boşluk ya da bir tür bildiriminde arabirimleri gerektirir<br /><br />`false` -Gerekli _hiçbir_ için iki nokta üst üste tabanları ya da bir tür bildiriminde arabirimleri sonra boşluk |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_space_after_colon_in_inheritance_clause = true
interface I
{

}

class C : I
{

}

// csharp_space_after_colon_in_inheritance_clause = false
interface I
{

}

class C :I
{

}
```

#### <a name="csharpspacearoundbinaryoperators"></a>CSharp\_alanı\_etrafında\_binary_operators

|||
|-|-|
| **Kural adı** | csharp_space_around_binary_operators |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |
| **Değerler** | `before_and_after` -Önce ve ikili işleç sonra boşluk Ekle<br /><br />`none` -Önce ve sonra ikili işleç boşlukları Kaldır<br /><br />`ignore` -İkili işleçler etrafındaki boşlukları yoksay |
| **Visual Studio varsayılan** | `before_and_after` |

Bu kural atlayın veya dışında bir değer kullanın, `before_and_after`, `none`, veya `ignore`, ayar uygulanmaz.

Kod örnekleri:

```csharp
// csharp_space_around_binary_operators = before_and_after
return x * (x - y);

// csharp_space_around_binary_operators = none
return x*(x-y);

// csharp_space_around_binary_operators = ignore
return x  *  (x-y);
```

#### <a name="csharpspacebetweenmethoddeclarationemptyparameterlistparentheses"></a>csharp_space_between_method_declaration_empty_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_declaration_empty_parameter_list_parentheses |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |
| **Değerler** | `true` -Bir yöntem bildiriminde için boş parametre listesi parantezlerinin içine boşluk ekleyin<br /><br />`false` -Bir yöntem bildiriminde için boş parametre listesi parantezlerinin içine boşluk Kaldır |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_declaration_empty_parameter_list_parentheses = true
void Goo( )
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}

// csharp_space_between_method_declaration_empty_parameter_list_parentheses = false
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}
```

#### <a name="csharpspacebetweenmethodcallnameandopeningparenthesis"></a>csharp_space_between_method_call_name_and_opening_parenthesis

|||
|-|-|
| **Kural adı** | csharp_space_between_method_call_name_and_opening_parenthesis |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |
| **Değerler** | `true` -Yöntem çağrısı adı ve açma parantezi arasına boşluk Ekle<br /><br />`false` -Yöntem çağrısı adı ve açma parantezi arasına boşluk Kaldır |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_call_name_and_opening_parenthesis = true
void Goo()
{
    Goo (1);
}

void Goo(int x)
{
    Goo ();
}

// csharp_space_between_method_call_name_and_opening_parenthesis = false
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}
```

#### <a name="csharpspacebetweenmethodcallemptyparameterlistparentheses"></a>csharp_space_between_method_call_empty_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_call_empty_parameter_list_parentheses |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.7 |
| **Değerler** | `true` -Boş bağımsız değişken listesi parantezlerinin içine boşluk ekleyin<br /><br />`false` -Boş bağımsız değişken listesi parantezlerinin içine boşluk Kaldır |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_call_empty_parameter_list_parentheses = true
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo( );
}

// csharp_space_between_method_call_empty_parameter_list_parentheses = false
void Goo()
{
    Goo(1);
}

void Goo(int x)
{
    Goo();
}
```

#### <a name="csharpspaceaftercomma"></a>csharp_space_after_comma

|||
|-|-|
| **Kural adı** | csharp_space_after_comma |
| **Geçerli diller** | C# |
| **Değerler** | `true` -Virgülden sonra boşluk Ekle<br /><br />`false` -Virgülden sonra boşluk kaldırın. |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
// csharp_space_after_comma = true
int[] x = new int[] { 1, 2, 3, 4, 5 };

// csharp_space_after_comma = false
int[] x = new int[] { 1,2,3,4,5 }
```

#### <a name="csharpspaceafterdot"></a>csharp_space_after_dot

|||
|-|-|
| **Kural adı** | csharp_space_after_dot |
| **Geçerli diller** | C# |
| **Değerler** | `true` -Bir noktadan sonra boşluk Ekle<br /><br />`false` -Sonra bir nokta boşluğu Kaldır |
| **Visual Studio varsayılan** | `false` |

Kod örnekleri:

```csharp
// csharp_space_after_dot = true
this. Goo();

// csharp_space_after_dot = false
this.Goo();
```

### <a name="wrap-options"></a>Kaydırma seçenekleri

Bu biçimlendirme kuralları ifadeleri ve kod blokları için ayrı satırlara karşı tek satır kullanımını ilgilendiriyor.

Örnek *.editorconfig* dosyası:

```ini
# CSharp formatting settings:
[*.cs]
csharp_preserve_single_line_statements = true
csharp_preserve_single_line_blocks = true
```

#### <a name="csharppreservesinglelinestatements"></a>csharp_preserve_single_line_statements

|||
|-|-|
| **Kural adı** | csharp_preserve_single_line_statements |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -İfadeleri ve üye bildirimlerini aynı satırda bırakın<br /><br />`false` -İfadeleri ve üye bildirimlerini farklı satırlarda bırakın |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
//csharp_preserve_single_line_statements = true
int i = 0; string name = "John";

//csharp_preserve_single_line_statements = false
int i = 0;
string name = "John";
```

#### <a name="csharppreservesinglelineblocks"></a>csharp_preserve_single_line_blocks

|||
|-|-|
| **Kural adı** | csharp_preserve_single_line_blocks |
| **Geçerli diller** | C# |
| **Sunulan sürümü** | Visual Studio 2017 sürüm 15.3 |
| **Değerler** | `true` -Kod bloğu tek satırda bırak<br /><br />`false` -Kod bloğu ayrı satırlarda bırakın |
| **Visual Studio varsayılan** | `true` |

Kod örnekleri:

```csharp
//csharp_preserve_single_line_blocks = true
public int Foo { get; set; }

//csharp_preserve_single_line_blocks = false
public int MyProperty
{
    get; set;
}
```

## <a name="see-also"></a>Ayrıca bkz.

- [Dil kuralları](editorconfig-language-conventions.md)
- [Adlandırma kuralları](editorconfig-naming-conventions.md)
- [Kodlama kuralı ayarlarına EditorConfig için .NET](editorconfig-code-style-settings-reference.md)