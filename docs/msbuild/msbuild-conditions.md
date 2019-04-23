---
title: MSBuild koşulları | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- MSBuild, conditions
- conditions [MSBuild]
ms.assetid: 9d7aa308-b667-48ed-b4c9-a61e49eb0a85
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b1070483e492bbbf6cc9f6e9f4a8f4b225f2b74b
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60096172"
---
# <a name="msbuild-conditions"></a>MSBuild koşulları
[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] olabilir koşulları belirli bir kümesini destekler yerde uygulanan bir `Condition` özniteliğine izin verilir. Aşağıdaki tabloda, bu koşullar açıklanmaktadır.

|Koşul|Açıklama|
|---------------|-----------------|
|'`stringA`' == '`stringB`'|Eğer `stringA` eşittir `stringB` ise `true` olarak değerlendirilir.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'=='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|
|'`stringA`' != '`stringB`'|Değerlendiren `true` varsa `stringA` eşit değildir `stringB`.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'!='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|
|\<, >, \<=, >=|İşleçlerin sayısal değerlerini karşılaştırır. İlişkisel değerlendirme doğru olması durumunda `true` döndürür. İşlenenler, bir ondalık ya da onaltılık sayıya dönüşebilmelidir. Onaltılık sayıların "0x" ile başlaması gerekir. **Not:**  XML'de `<` ve `>` için kaçış karakterleri eklenmelidir. `<` simgesi `&lt;` olarak temsil edilir. `>` simgesi `&gt;` olarak temsil edilir.|
|Exists('`stringA`')|`stringA` adında bir dosya veya klasör varsa `true` olarak değerlendirilir.<br /><br /> Örneğin:<br /><br /> `Condition="!Exists('$(builtdir)')"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|
|HasTrailingSlash('`stringA`')|Değerlendiren `true` ya da arkaya eğik belirtilen dizeyi içerip içermediğini (\\) veya İleri eğik çizgi (/) karakteri.<br /><br /> Örneğin:<br /><br /> `Condition="!HasTrailingSlash('$(OutputPath)')"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|
|!|Değerlendiren `true` işlenen değerlendirilirse `false`.|
|And|Değerlendiren `true` her iki işlenen de sonucunu verirse `true`.|
|Or|Değerlendiren `true` en az bir işlenen değerlendirilirse `true`.|
|()|Değerlendiren mekanizması gruplandırma `true` ifadeler içinde yer alan sonucunu verirse `true`.|
|$if$ ( %expression% ), $else$, $endif$|Denetler olup belirtilen `%expression%` geçirilen özel bir şablon parametresinin dize değeri eşler. Varsa `$if$` değerlendirilen koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$else$` koşul denetlenir. Varsa `$else$` koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$endif$` koşul ifade değerlendirme sona erer.<br /><br /> Kullanım örnekleri için bkz: [Visual Studio Proje/öğe şablon parametre mantıksal](http://stackoverflow.com/questions/6709057/visual-studio-project-item-template-parameter-logic).|

## <a name="see-also"></a>Ayrıca bkz.
- [MSBuild başvurusu](../msbuild/msbuild-reference.md)
- [Koşullu yapılar](../msbuild/msbuild-conditional-constructs.md)
- [İzlenecek yol: Sıfırdan bir MSBuild proje dosyası oluşturma](../msbuild/walkthrough-creating-an-msbuild-project-file-from-scratch.md)
