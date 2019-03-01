---
title: MSBuild koşulları | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: msbuild
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
caps.latest.revision: 17
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cd5fb6f70504fd89c0d08f7a8aa760b3c7b68323
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54758338"
---
# <a name="msbuild-conditions"></a>MSBuild Koşulları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

  
[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] olabilir koşulları belirli bir kümesini destekler yerde uygulanan bir `Condition` özniteliğine izin verilir. Aşağıdaki tabloda, bu koşullar açıklanmaktadır.  
  
|Koşul|Açıklama|  
|---------------|-----------------|  
|'`stringA`' == '`stringB`'|Eğer `stringA` eşittir `stringB` ise `true` olarak değerlendirilir.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'=='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boolean değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|'`stringA`' != '`stringB`'|Değerlendiren `true` varsa `stringA` eşit değildir `stringB`.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'!='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boolean değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|\<, >, \<=, >=|Sayısal değerlerin işlenenden değerlendirir. Döndürür `true` ilişkisel değerlendirme doğru olması durumunda. İşlenen, bir ondalık ya da onaltılık sayı değerlendirmelidir. Onaltılık sayılar "0 x" başlaması gerekir. **Not:**  XML'de karakterleri `<` ve `>` kaçış karakterleri eklenmelidir. Simgenin `<` olarak temsil edilir `<`. Simgenin `>` olarak temsil edilir `>`.|  
|Var ('`stringA`')|Değerlendiren `true` bir dosya veya klasör adıyla `stringA` bulunmaktadır.<br /><br /> Örneğin:<br /><br /> `Condition="!Exists('$(builtdir)')"`<br /><br /> Basit alfasayısal dize veya Boolean değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|HasTrailingSlash('`stringA`')|Değerlendiren `true` ya da arkaya eğik belirtilen dizeyi içerip içermediğini (\\) veya İleri eğik çizgi (/) karakteri.<br /><br /> Örneğin:<br /><br /> `Condition="!HasTrailingSlash('$(OutputPath)')"`<br /><br /> Basit alfasayısal dize veya Boolean değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|!|Değerlendiren `true` işlenen değerlendirilirse `false`.|  
|And|Değerlendiren `true` her iki işlenen de sonucunu verirse `true`.|  
|Or|Değerlendiren `true` en az bir işlenen değerlendirilirse `true`.|  
|()|Değerlendiren mekanizması gruplandırma `true` ifadeler içinde yer alan sonucunu verirse `true`.|  
|$if$ ( %expression% ), $else$, $endif$|Denetler olup belirtilen `%expression%` geçirilen özel bir şablon parametresinin dize değeri eşler. Varsa `$if$` değerlendirilen koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$else$` koşul denetlenir. Varsa `$else$` koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$endif$` koşul ifade değerlendirme sona erer.<br /><br /> Kullanım örnekleri için bkz: [Visual Studio Proje/öğe şablon parametre mantıksal](http://stackoverflow.com/questions/6709057/visual-studio-project-item-template-parameter-logic).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Koşullu yapılar](../msbuild/msbuild-conditional-constructs.md)   
 [İzlenecek yol: Sıfırdan MSBuild proje dosyası oluşturma](../msbuild/walkthrough-creating-an-msbuild-project-file-from-scratch.md)
