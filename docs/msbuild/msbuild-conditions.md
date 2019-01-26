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
ms.openlocfilehash: 30ac71ccce1b237913db5acc8b34300b0517bcd6
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54969752"
---
# <a name="msbuild-conditions"></a>MSBuild koşulları
[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] olabilir koşulları belirli bir kümesini destekler yerde uygulanan bir `Condition` özniteliğine izin verilir. Aşağıdaki tabloda, bu koşullar açıklanmaktadır.  
  
|Koşul|Açıklama|  
|---------------|-----------------|  
|'`stringA`' == '`stringB`'|Değerlendiren `true` varsa `stringA` eşittir `stringB`.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'=='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tırnak gerekmez. Ancak, tek tırnak, boş değerler için gereklidir.|  
|'`stringA`' != '`stringB`'|Değerlendiren `true` varsa `stringA` eşit değildir `stringB`.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'!='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tırnak gerekmez. Ancak, tek tırnak, boş değerler için gereklidir.|  
|\<, >, \<=, >=|Sayısal değerlerin işlenenden değerlendirir. Döndürür `true` ilişkisel değerlendirme doğru olması durumunda. İşlenen, bir ondalık ya da onaltılık sayı değerlendirmelidir. Onaltılık sayılar "0 x" başlaması gerekir. **Not:**  XML'de karakterleri `<` ve `>` kaçış karakterleri eklenmelidir. Simgenin `<` olarak temsil edilir `&lt;`. Simgenin `>` olarak temsil edilir `&gt;`.|  
|Var ('`stringA`')|Değerlendiren `true` bir dosya veya klasör adıyla `stringA` bulunmaktadır.<br /><br /> Örneğin:<br /><br /> `Condition="!Exists('$(builtdir)')"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tırnak gerekmez. Ancak, tek tırnak, boş değerler için gereklidir.|  
|HasTrailingSlash('`stringA`')|Değerlendiren `true` ya da arkaya eğik belirtilen dizeyi içerip içermediğini (\\) veya İleri eğik çizgi (/) karakteri.<br /><br /> Örneğin:<br /><br /> `Condition="!HasTrailingSlash('$(OutputPath)')"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tırnak gerekmez. Ancak, tek tırnak, boş değerler için gereklidir.|  
|!|Değerlendiren `true` işlenen değerlendirilirse `false`.|  
|Ve|Değerlendiren `true` her iki işlenen de sonucunu verirse `true`.|  
|Veya|Değerlendiren `true` en az bir işlenen değerlendirilirse `true`.|  
|()|Değerlendiren mekanizması gruplandırma `true` ifadeler içinde yer alan sonucunu verirse `true`.|  
|$if$ ( %expression% ), $else$, $endif$|Denetler olup belirtilen `%expression%` geçirilen özel bir şablon parametresinin dize değeri eşler. Varsa `$if$` değerlendirilen koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$else$` koşul denetlenir. Varsa `$else$` koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$endif$` koşul ifade değerlendirme sona erer.<br /><br /> Kullanım örnekleri için bkz: [Visual Studio Proje/öğe şablon parametre mantıksal](http://stackoverflow.com/questions/6709057/visual-studio-project-item-template-parameter-logic).|  
  
## <a name="see-also"></a>Ayrıca bkz.  
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Koşullu yapılar](../msbuild/msbuild-conditional-constructs.md)   
 [İzlenecek yol: Sıfırdan bir MSBuild proje dosyası oluşturma](../msbuild/walkthrough-creating-an-msbuild-project-file-from-scratch.md)
