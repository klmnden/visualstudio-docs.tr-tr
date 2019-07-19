---
title: EditorConfig için .NET biçimlendirme kuralları
ms.date: 07/17/2019
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
ms.openlocfilehash: ccebfc38d5170920fe3f3c37ee77aabaf660a3b8
ms.sourcegitcommit: 8562a337cc9f674c756a4a0b2c7e288ebd61b51e
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/19/2019
ms.locfileid: "68345672"
---
# <a name="formatting-conventions"></a>Biçimlendirme kuralları

Visual Studio için EditorConfig 'in biçimlendirme kuralları şu kategorilere ayrılır:

- [.NET biçimlendirme ayarları](#net-formatting-settings)

- [C#biçimlendirme ayarları](#c-formatting-settings)

## <a name="rule-format"></a>Kural biçimi

Biçimlendirme kuralları için kurallar aşağıdaki biçimdedir:

`rule_name = value`

Birçok kural için `true` (Bu stili tercih et) veya `false` (Bu stili tercih etme) için `value`bir tane belirtin. Diğer kurallar için, `flush_left` ya `before_and_after` da kuralın ne zaman ve nereye uygulanacağını betimleyen bir değer belirtirsiniz. Önem derecesi belirtmezsiniz.

## <a name="net-formatting-settings"></a>.NET biçimlendirme ayarları

Bu bölümdeki biçimlendirme kuralları için C# geçerlidir ve kodu Visual Basic.

- [Using deyimlerini Düzenle](#organize-using-directives)
  - dotnet_sort_system_directives_first
  - dotnet_separate_import_directive_groups

### <a name="organize-using-directives"></a>Yönergeleri kullanarak düzenleme

Bu biçimlendirme kuralları `using` yönergeleri ve `Imports` deyimleri sıralamayı ve görüntülemeyi sorun.

Örnek *. editorconfig* dosyası:

```ini
# .NET formatting settings
[*.{cs,vb}]
dotnet_sort_system_directives_first = true
dotnet_separate_import_directive_groups = true
```

#### <a name="dotnetsortsystemdirectivesfirst"></a>DotNet\_sıralama\_sistemdirectives_first\_

|||
|-|-|
| **Kural adı** | dotnet_sort_system_directives_first |
| **Uygun diller** | C# ve Visual Basic |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-System. * `using` yönergelerini alfabetik olarak sıralayın ve diğer using yönergelerinden önce yerleştirin.<br /><br />`false`-System. * `using` yönergelerini diğer `using` yönergelerden önce yerleştirmeyin. |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="dotnetseparateimportdirectivegroups"></a>DotNet\_ayrı\_içeriaktarma\_yönergesigrupları\_

|||
|-|-|
| **Kural adı** | dotnet_separate_import_directive_groups |
| **Uygun diller** | C# ve Visual Basic |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15.5 |
| **Değerler** | `true`-Yönerge grupları arasına `using` boş bir satır koyun.<br /><br />`false`-Yönerge grupları arasına `using` boş bir satır yerleştirmeyin. |
| **Visual Studio varsayılanı** | `false` |

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

## <a name="c-formatting-settings"></a>C#biçimlendirme ayarları

Bu bölümdeki biçimlendirme kuralları yalnızca kod için C# geçerlidir.

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
  - csharp_indent_block_contents
  - csharp_indent_braces
  - csharp_indent_case_contents_when_block
- [Aralık seçenekleri](#spacing-options)
  - csharp_space_after_cast
  - csharp_space_after_keywords_in_control_flow_statements
  - csharp_space_between_parentheses
  - csharp_space_before_colon_in_inheritance_clause
  - csharp_space_after_colon_in_inheritance_clause
  - csharp_space_around_binary_operators
  - csharp_space_between_method_declaration_parameter_list_parentheses
  - csharp_space_between_method_declaration_empty_parameter_list_parentheses
  - csharp_space_between_method_declaration_name_and_open_parenthesis
  - csharp_space_between_method_call_parameter_list_parentheses
  - csharp_space_between_method_call_empty_parameter_list_parentheses
  - csharp_space_between_method_call_name_and_opening_parenthesis
  - csharp_space_after_comma
  - csharp_space_before_comma
  - csharp_space_after_dot
  - csharp_space_before_dot
  - csharp_space_after_semicolon_in_for_statement
  - csharp_space_before_semicolon_in_for_statement
  - csharp_space_around_declaration_statements
  - csharp_space_before_open_square_brackets
  - csharp_space_between_empty_square_brackets
  - csharp_space_between_square_brackets
- [Sarlama seçenekleri](#wrap-options)
  - csharp_preserve_single_line_statements
  - csharp_preserve_single_line_blocks

### <a name="new-line-options"></a>Yeni satır seçenekleri

Bu biçimlendirme kuralları kodu biçimlendirmek için yeni satırların kullanılmasını sağlar.

Örnek *. editorconfig* dosyası:

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

#### <a name="csharpnewlinebeforeopenbrace"></a>open_brace\_öncesi\_\_CSharp yeni satır\_

Bu kural, bir açık küme ayracın `{` önceki kodla aynı satıra mi yoksa yeni bir satıra mı yerleştirileceğini ele alır. Bu kural için, bu kuralın ne zaman uygulanacağını tanımlamak üzere **Yöntemler** veya **Özellikler**gibi **All**, **none**veya bir ya da daha fazla kod öğesi belirtirsiniz. Birden çok kod öğesi belirtmek için bunları virgülle (,) ayırın.

|||
|-|-|
| **Kural adı** | csharp_new_line_before_open_brace |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `all`-Küme ayracın tüm ifadeler için yeni bir satırda olması gerekir ("Allman" stili).<br /><br />`none`-Küme ayracın tüm ifadeler için aynı satırda olması gerekir ("K & R").<br /><br />`accessors`, `anonymous_methods`, `anonymous_types`, ,`control_blocks` ,`indexers`, ,`local_functions`,, ,`object_collection_array_initializers`, -Kümeayraçlarıiçinyeni`types` bir satırda olması gerekir `properties` `methods` `lambdas` `events` Belirtilen kod öğesi ("Allman" Style). |
| **Visual Studio varsayılanı** | `all` |

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

#### <a name="csharpnewlinebeforeelse"></a>CSharp\_yeni\_satırbefore_else\_

|||
|-|-|
| **Kural adı** | csharp_new_line_before_else |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Deyimlerini `else` yeni bir satıra yerleştir.<br /><br />`false`-Deyimleri `else` aynı satıra yerleştir. |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="csharpnewlinebeforecatch"></a>CSharp\_yeni\_satırbefore_catch\_

|||
|-|-|
| **Kural adı** | csharp_new_line_before_catch |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Deyimlerini `catch` yeni bir satıra yerleştir.<br /><br />`false`-Deyimleri `catch` aynı satıra yerleştir. |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="csharpnewlinebeforefinally"></a>CSharp\_yeni\_satırbefore_finally\_

|||
|-|-|
| **Kural adı** | csharp_new_line_before_finally |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Deyimlerin `finally` , kapanış ayracından sonra yeni bir satırda olmasını gerektir.<br /><br />`false`-Deyimlerinin `finally` kapanış ayracı ile aynı satırda olmasını gerektir. |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="csharpnewlinebeforemembersinobjectinitializers"></a>object_initializers\_içindeki\_üyelerden\_öncekiCSharp\_yenisatır\_\_

|||
|-|-|
| **Kural adı** | csharp_new_line_before_members_in_object_initializers |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Nesne başlatıcılarının üyelerinin ayrı satırlarda olmasını gerektir<br /><br />`false`-Nesne başlatıcılarının üyelerinin aynı satırda olmasını gerektir |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="csharpnewlinebeforemembersinanonymoustypes"></a>anonymous_types\_içindeki\_üyelerden\_öncekiCSharp\_yenisatır\_\_

|||
|-|-|
| **Kural adı** | csharp_new_line_before_members_in_anonymous_types |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Anonim türlerin üyelerinin ayrı satırlarda olmasını gerektir<br /><br />`false`-Anonim türlerin üyelerinin aynı satırda olmasını gerektir |
| **Visual Studio varsayılanı** | `true` |

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
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Sorgu ifadesi yan tümcelerinin öğelerinin ayrı satırlarda olmasını gerektir<br /><br />`false`-Sorgu ifadesi yan tümcelerinin öğelerin aynı satırda olmasını gerektir |
| **Visual Studio varsayılanı** | `true` |

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

Bu biçimlendirme kuralları kodu biçimlendirmek için girintileme kullanımını sağlar.

Örnek *. editorconfig* dosyası:

```ini
# CSharp formatting settings:
[*.cs]
csharp_indent_case_contents = true
csharp_indent_switch_labels = true
csharp_indent_labels = flush_left
csharp_indent_block_contents = true
csharp_indent_braces = false
csharp_indent_case_contents_when_block = true
```

#### <a name="csharpindentcasecontents"></a>CSharp\_girintileme\_case_contents

|||
|-|-|
| **Kural adı** | csharp_indent_case_contents |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Case `switch` içeriğini Girintile<br /><br />`false`-Servis talebi içeriklerini `switch` girintileme |
| **Visual Studio varsayılanı** | `true` |

- Bu kural **true**olarak ayarlandığında, ı.
- Bu kural **false**, d olarak ayarlandığında.

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

#### <a name="csharpindentswitchlabels"></a>CSharp\_girintileme\_switch_labels

|||
|-|-|
| **Kural adı** | csharp_indent_switch_labels |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Etiketleri `switch` Girintile<br /><br />`false`-Etiketleri girintileme `switch` |
| **Visual Studio varsayılanı** | `true` |

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
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `flush_left`-Etiketler en soldaki sütuna yerleştirilir<br /><br />`one_less_than_current`-Etiketler geçerli bağlama göre daha az bir girintide yerleştirilir<br /><br />`no_change`-Etiketler, geçerli bağlamla aynı girintide yer alır |
| **Visual Studio varsayılanı** | `no_change` |

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

#### <a name="csharpindentblockcontents"></a>csharp_indent_block_contents

|||
|-|-|
| **Kural adı** | csharp_indent_block_contents |
| **Uygun diller** | C# |
| **Değerler** | `true` - <br /><br />`false` -  |
| **Visual Studio varsayılanı** | `true` |

Kod örnekleri:

```csharp
// csharp_indent_block_contents = true
static void Hello()
{
    Console.WriteLine("Hello");
}

// csharp_indent_block_contents = false
static void Hello()
{
Console.WriteLine("Hello");
}
```

#### <a name="csharpindentbraces"></a>csharp_indent_braces

|||
|-|-|
| **Kural adı** | csharp_indent_braces |
| **Uygun diller** | C# |
| **Değerler** | `true` - <br /><br />`false` -  |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_indent_braces = true
static void Hello()
    {
    Console.WriteLine("Hello");
    }

// csharp_indent_braces = false
static void Hello()
{
    Console.WriteLine("Hello");
}
```

#### <a name="csharpindentcasecontentswhenblock"></a>csharp_indent_case_contents_when_block

|||
|-|-|
| **Kural adı** | csharp_indent_case_contents_when_block |
| **Uygun diller** | C# |
| **Değerler** | `true` - <br /><br />`false` -  |
| **Visual Studio varsayılanı** | `true` |

Kod örnekleri:

```csharp
// csharp_indent_case_contents_when_block = true
case 0:
    {
        Console.WriteLine("Hello");
        break;
    }

// csharp_indent_case_contents_when_block = false
case 0:
{
    Console.WriteLine("Hello");
    break;
}
```

### <a name="spacing-options"></a>Aralık seçenekleri

Bu biçimlendirme kuralları kodu biçimlendirmek için boşluk karakterlerinin kullanılmasını sağlar.

Örnek *. editorconfig* dosyası:

```ini
# CSharp formatting settings:
[*.cs]
csharp_space_after_cast = true
csharp_space_after_keywords_in_control_flow_statements = true
csharp_space_between_parentheses = control_flow_statements, type_casts
csharp_space_before_colon_in_inheritance_clause = true
csharp_space_after_colon_in_inheritance_clause = true
csharp_space_around_binary_operators = before_and_after
csharp_space_between_method_declaration_parameter_list_parentheses = true
csharp_space_between_method_declaration_empty_parameter_list_parentheses = false
csharp_space_between_method_declaration_name_and_open_parenthesis = false
csharp_space_between_method_call_parameter_list_parentheses = true
csharp_space_between_method_call_empty_parameter_list_parentheses = false
csharp_space_between_method_call_name_and_opening_parenthesis = false
csharp_space_after_comma = true
csharp_space_before_comma = false
csharp_space_after_dot = false
csharp_space_before_dot = false
csharp_space_after_semicolon_in_for_statement = true
csharp_space_before_semicolon_in_for_statement = false
csharp_space_around_declaration_statements = false
csharp_space_before_open_square_brackets = false
csharp_space_between_empty_square_brackets = false
csharp_space_between_square_brackets = false
```

#### <a name="csharpspaceaftercast"></a>CSharp\_Space\_after_cast

|||
|-|-|
| **Kural adı** | csharp_space_after_cast |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Bir atama ve değer arasına bir boşluk karakteri koyun<br /><br />`false`-Cast ve değer arasındaki boşluğu kaldır |
| **Visual Studio varsayılanı** | `false` |

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
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`- `for` Döngü gibi bir denetim akışı deyimindeki anahtar sözcükten sonra bir boşluk karakteri yerleştir<br /><br />`false`- `for` Döngü gibi bir denetim akışı deyimindeki anahtar sözcükten sonra boşluk kaldır |
| **Visual Studio varsayılanı** | `true` |

Kod örnekleri:

```csharp
// csharp_space_after_keywords_in_control_flow_statements = true
for (int i;i<x;i++) { ... }

// csharp_space_after_keywords_in_control_flow_statements = false
for(int i;i<x;i++) { ... }
```

#### <a name="csharpspacebetweenparentheses"></a>csharp_space_between_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_parentheses |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `control_flow_statements`-Denetim akışı deyimlerinin parantezleri arasına boşluk yerleştir<br /><br />`expressions`-İfadelerin parantezleri arasına boşluk yerleştir<br /><br />`type_casts`-Tür atamalerdeki parantezler arasında boşluk yerleştir |
| **Visual Studio varsayılanı** | `false` |

Bu kuralı atlarsanız veya `control_flow_statements`, `expressions`, veya `type_casts`dışında bir değer kullanırsanız, ayar uygulanmaz.

Kod örnekleri:

```csharp
// csharp_space_between_parentheses = control_flow_statements
for ( int i = 0; i < 10; i++ ) { }

// csharp_space_between_parentheses = expressions
var z = ( x * y ) - ( ( y - x ) * 3 );

// csharp_space_between_parentheses = type_casts
int y = ( int )x;
```

#### <a name="csharpspacebeforecolonininheritanceclause"></a>inheritance_clause\_içinde\_\_ikinoktadan\_önce CSharp Space\_

|||
|-|-|
| **Kural adı** | csharp_space_before_colon_in_inheritance_clause |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |
| **Değerler** | `true`-Bir tür bildiriminde temeller veya arabirimler için iki noktadan önce bir boşluk karakteri yerleştirin<br /><br />`false`-Tür bildiriminde temeller veya arabirimler için iki noktadan önce boşluğu kaldır |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="csharpspaceaftercolonininheritanceclause"></a>inheritance_clause\_içinde\_\_ikinoktadan\_sonra CSharp Space\_

|||
|-|-|
| **Kural adı** | csharp_space_after_colon_in_inheritance_clause |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |
| **Değerler** | `true`-Bir tür bildiriminde tabanların veya arabirimlerin iki noktadan sonra bir boşluk karakteri yerleştir<br /><br />`false`-Bir tür bildiriminde temeller veya arabirimler için iki noktadan sonra boşluk kaldır |
| **Visual Studio varsayılanı** | `true` |

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

#### <a name="csharpspacearoundbinaryoperators"></a>binary_operators etrafında\_\_CSharp\_Space

|||
|-|-|
| **Kural adı** | csharp_space_around_binary_operators |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |
| **Değerler** | `before_and_after`-İkili işleçten önce ve sonra boşluk Ekle<br /><br />`none`-İkili işleçten önce ve sonra boşlukları kaldır<br /><br />`ignore`-İkili operatörlerin çevresindeki boşlukları yoksay |
| **Visual Studio varsayılanı** | `before_and_after` |

Bu kuralı atlarsanız veya `before_and_after`, `none`, veya `ignore`dışında bir değer kullanırsanız, ayar uygulanmaz.

Kod örnekleri:

```csharp
// csharp_space_around_binary_operators = before_and_after
return x * (x - y);

// csharp_space_around_binary_operators = none
return x*(x-y);

// csharp_space_around_binary_operators = ignore
return x  *  (x-y);
```

#### <a name="csharpspacebetweenmethoddeclarationparameterlistparentheses"></a>csharp_space_between_method_declaration_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_declaration_parameter_list_parentheses |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Açma parantezinden sonra ve bir yöntem bildirimi parametre listesinin kapatma parantezinden önce bir boşluk karakteri yerleştirin<br /><br />`false`-Boşluk karakterlerini açma parantezinden sonra ve bir yöntem bildirimi parametre listesinin kapatma parantezinden önce kaldırın |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_declaration_parameter_list_parentheses = true
void Bark( int x ) { ... }

// csharp_space_between_method_declaration_parameter_list_parentheses = false
void Bark(int x) { ... }
```

#### <a name="csharpspacebetweenmethoddeclarationemptyparameterlistparentheses"></a>csharp_space_between_method_declaration_empty_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_declaration_empty_parameter_list_parentheses |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |
| **Değerler** | `true`-Yöntem bildirimi için boş parametre listesi ayraçları içine boşluk Ekle<br /><br />`false`-Yöntem bildirimi için boş parametre listesi ayraçları içindeki alanı kaldır |
| **Visual Studio varsayılanı** | `false` |

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

#### <a name="csharpspacebetweenmethoddeclarationnameandopenparenthesis"></a>csharp_space_between_method_declaration_name_and_open_parenthesis

|||
|-|-|
| **Kural adı** | csharp_space_between_method_declaration_name_and_open_parenthesis |
| **Uygun diller** | C# |
| **Değerler** | `true`-Yöntem bildiriminde Yöntem adı ve açma ayracı arasına bir boşluk karakteri koyun<br /><br />`false`-Yöntem bildiriminde Yöntem adı ve açma ayracı arasındaki boşluk karakterlerini kaldırın |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_declaration_name_and_open_parenthesis = true
void M () { }

// csharp_space_between_method_declaration_name_and_open_parenthesis = false
void M() { }
```

#### <a name="csharpspacebetweenmethodcallparameterlistparentheses"></a>csharp_space_between_method_call_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_call_parameter_list_parentheses |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Açma parantezinden sonra ve bir yöntem çağrısının kapatma parantezinden önce bir boşluk karakteri yerleştirin<br /><br />`false`-Açma parantezinden sonra ve bir yöntem çağrısının kapanış parantezinden önce boşluk karakterlerini kaldırın |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_method_call_parameter_list_parentheses = true
MyMethod( argument );

// csharp_space_between_method_call_parameter_list_parentheses = false
MyMethod(argument);
```

#### <a name="csharpspacebetweenmethodcallemptyparameterlistparentheses"></a>csharp_space_between_method_call_empty_parameter_list_parentheses

|||
|-|-|
| **Kural adı** | csharp_space_between_method_call_empty_parameter_list_parentheses |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |
| **Değerler** | `true`-Boş bağımsız değişken listesi ayraçları içine boşluk Ekle<br /><br />`false`-Boş bağımsız değişken listesi ayraçları içindeki alanı kaldır |
| **Visual Studio varsayılanı** | `false` |

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

#### <a name="csharpspacebetweenmethodcallnameandopeningparenthesis"></a>csharp_space_between_method_call_name_and_opening_parenthesis

|||
|-|-|
| **Kural adı** | csharp_space_between_method_call_name_and_opening_parenthesis |
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,7 |
| **Değerler** | `true`-Yöntem çağrısı adı ve açma ayracı arasına boşluk Ekle<br /><br />`false`-Yöntem çağrı adı ve açılış ayracı arasındaki boşluğu kaldır |
| **Visual Studio varsayılanı** | `false` |

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

#### <a name="csharpspaceaftercomma"></a>csharp_space_after_comma

|||
|-|-|
| **Kural adı** | csharp_space_after_comma |
| **Uygun diller** | C# |
| **Değerler** | `true`-Virgülden sonra boşluk Ekle<br /><br />`false`-Virgülden sonra boşluk kaldır |
| **Visual Studio varsayılanı** | `true` |

Kod örnekleri:

```csharp
// csharp_space_after_comma = true
int[] x = new int[] { 1, 2, 3, 4, 5 };

// csharp_space_after_comma = false
int[] x = new int[] { 1,2,3,4,5 }
```

#### <a name="csharpspacebeforecomma"></a>csharp_space_before_comma

|||
|-|-|
| **Kural adı** | csharp_space_before_comma |
| **Uygun diller** | C# |
| **Değerler** | `true`-Virgülden önce boşluk Ekle<br /><br />`false`-Bir virgülden önce boşluğu kaldır |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_before_comma = true
int[] x = new int[] { 1 , 2 , 3 , 4 , 5 };

// csharp_space_before_comma = false
int[] x = new int[] { 1, 2, 3, 4, 5 };
```

#### <a name="csharpspaceafterdot"></a>csharp_space_after_dot

|||
|-|-|
| **Kural adı** | csharp_space_after_dot |
| **Uygun diller** | C# |
| **Değerler** | `true`-Noktadan sonra boşluk Ekle<br /><br />`false`-Noktadan sonra boşluk kaldır |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_after_dot = true
this. Goo();

// csharp_space_after_dot = false
this.Goo();
```

#### <a name="csharpspacebeforedot"></a>csharp_space_before_dot

|||
|-|-|
| **Kural adı** | csharp_space_before_dot |
| **Uygun diller** | C# |
| **Değerler** | `true`-Noktadan önce boşluk Ekle <br /><br />`false`-Noktadan önce boşluğu kaldır |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_before_dot = true
this .Goo();

// csharp_space_before_dot = false
this.Goo();
```

#### <a name="csharpspaceaftersemicoloninforstatement"></a>csharp_space_after_semicolon_in_for_statement

|||
|-|-|
| **Kural adı** | csharp_space_after_semicolon_in_for_statement |
| **Uygun diller** | C# |
| **Değerler** | `true`-Bir `for` ifadede her noktalı virgülden sonra boşluk Ekle<br /><br />`false`-Bir `for` bildirimde her noktalı virgülden sonra boşluk kaldır |
| **Visual Studio varsayılanı** | `true` |

Kod örnekleri:

```csharp
// csharp_space_after_semicolon_in_for_statement = true
for (int i = 0; i < x.Length; i++)

// csharp_space_after_semicolon_in_for_statement = false
for (int i = 0;i < x.Length;i++)
```

##### <a name="csharpspacebeforesemicoloninforstatement"></a>csharp_space_before_semicolon_in_for_statement

|||
|-|-|
| **Kural adı** | csharp_space_before_semicolon_in_for_statement |
| **Uygun diller** | C# |
| **Değerler** | `true`-Bir `for` bildirimde her noktalı virgülden önce boşluk Ekle <br /><br />`false`-Bir `for` bildirimde her noktalı virgülden önce boşluk kaldır |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_before_semicolon_in_for_statement = true
for (int i = 0 ; i < x.Length ; i++)

// csharp_space_before_semicolon_in_for_statement = false
for (int i = 0; i < x.Length; i++)
```

#### <a name="csharpspacearounddeclarationstatements"></a>csharp_space_around_declaration_statements

|||
|-|-|
| **Kural adı** | csharp_space_around_declaration_statements |
| **Uygun diller** | C# |
| **Değerler** | `ignore`-Bildirim deyimlerine fazladan boşluk karakterleri kaldırmayın<br /><br />`false`-Bildirim deyimlerine ek boşluk karakterlerini kaldır |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_around_declaration_statements = ignore
int    x    =    0   ;

// csharp_space_around_declaration_statements = false
int x = 0;
```

#### <a name="csharpspacebeforeopensquarebrackets"></a>csharp_space_before_open_square_brackets

|||
|-|-|
| **Kural adı** | csharp_space_before_open_square_brackets |
| **Uygun diller** | C# |
| **Değerler** | `true`-Açılış köşeli ayracından önce boşluk Ekle`[` <br /><br />`false`-Köşeli ayraçları açmadan önce boşluğu kaldır`[` |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_before_open_square_brackets = true
int [] numbers = new int [] { 1, 2, 3, 4, 5 };

// csharp_space_before_open_square_brackets = false
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
```

#### <a name="csharpspacebetweenemptysquarebrackets"></a>csharp_space_between_empty_square_brackets

|||
|-|-|
| **Kural adı** | csharp_space_between_empty_square_brackets |
| **Uygun diller** | C# |
| **Değerler** | `true`-Boş köşeli ayraç arasına boşluk Ekle`[ ]` <br /><br />`false`-Boş köşeli ayraçlar arasındaki boşluğu kaldır`[]` |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_empty_square_brackets = true
int[ ] numbers = new int[ ] { 1, 2, 3, 4, 5 };

// csharp_space_between_empty_square_brackets = false
int[] numbers = new int[] { 1, 2, 3, 4, 5 };
```

#### <a name="csharpspacebetweensquarebrackets"></a>csharp_space_between_square_brackets

|||
|-|-|
| **Kural adı** | csharp_space_between_square_brackets |
| **Uygun diller** | C# |
| **Değerler** | `true`-Boş olmayan köşeli Parantezde boşluk karakterleri Ekle`[ 0 ]` <br /><br />`false`-Boş olmayan köşeli ayraçdaki boşluk karakterlerini kaldır`[0]` |
| **Visual Studio varsayılanı** | `false` |

Kod örnekleri:

```csharp
// csharp_space_between_square_brackets = true
int index = numbers[ 0 ];

// csharp_space_between_square_brackets = false
int index = numbers[0];
```

### <a name="wrap-options"></a>Sarlama seçenekleri

Bu biçimlendirme kuralları, deyimler ve kod blokları için ayrı satırlara karşı tek satırların kullanımını önemli olarak kullanır.

Örnek *. editorconfig* dosyası:

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
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Deyimleri ve üye bildirimlerini aynı satırda bırak<br /><br />`false`-Deyimleri ve üye bildirimlerini farklı satırlarda bırak |
| **Visual Studio varsayılanı** | `true` |

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
| **Uygun diller** | C# |
| **Tanıtılan sürüm** | Visual Studio 2017 sürüm 15,3 |
| **Değerler** | `true`-Kod bloğunu tek satırda bırak<br /><br />`false`-Kod bloğunu ayrı satırlarda bırak |
| **Visual Studio varsayılanı** | `true` |

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
