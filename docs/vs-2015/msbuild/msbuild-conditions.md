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
ms.openlocfilehash: b29138ef9ab5bffa263a8392396091a38ea91a2e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68181108"
---
# <a name="msbuild-conditions"></a>MSBuild Koşulları
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

[!INCLUDE[vstecmsbuild](../includes/vstecmsbuild-md.md)] olabilir koşulları belirli bir kümesini destekler yerde uygulanan bir `Condition` özniteliğine izin verilir. Aşağıdaki tabloda, bu koşullar açıklanmaktadır.  
  
|Koşul|Açıklama|  
|---------------|-----------------|  
|'`stringA`' == '`stringB`'|Eğer `stringA` eşittir `stringB` ise `true` olarak değerlendirilir.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'=='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|'`stringA`' != '`stringB`'|Değerlendiren `true` varsa `stringA` eşit değildir `stringB`.<br /><br /> Örneğin:<br /><br /> `Condition="'$(CONFIG)'!='DEBUG'"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|\<, >, \<=, >=|İşleçlerin sayısal değerlerini karşılaştırır. İlişkisel değerlendirme doğru olması durumunda `true` döndürür. İşlenenler, bir ondalık ya da onaltılık sayıya dönüşebilmelidir. Onaltılık sayıların "0x" ile başlaması gerekir. **Not:**  XML'de `<` ve `>` için kaçış karakterleri eklenmelidir.           `<` simgesi `<` olarak temsil edilir.           `>` simgesi `>` olarak temsil edilir.|  
|Exists('`stringA`')|          `stringA` adında bir dosya veya klasör varsa `true` olarak değerlendirilir.<br /><br /> Örneğin:<br /><br /> `Condition="!Exists('$(builtdir)')"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|HasTrailingSlash ('`stringA`')|Değerlendiren `true` ya da arkaya eğik belirtilen dizeyi içerip içermediğini (\\) veya İleri eğik çizgi (/) karakteri.<br /><br /> Örneğin:<br /><br /> `Condition="!HasTrailingSlash('$(OutputPath)')"`<br /><br /> Basit alfasayısal dize veya Boole değerleri için tek tırnak gerekmez. Ancak boş değerler için tek tırnak gereklidir.|  
|!|Değerlendiren `true` işlenen değerlendirilirse `false`.|  
|And|Değerlendiren `true` her iki işlenen de sonucunu verirse `true`.|  
|Or|Değerlendiren `true` en az bir işlenen değerlendirilirse `true`.|  
|()|Değerlendiren mekanizması gruplandırma `true` ifadeler içinde yer alan sonucunu verirse `true`.|  
|(% ifade %) $if$ $başka$, $endif$|Denetler olup belirtilen `%expression%` geçirilen özel bir şablon parametresinin dize değeri eşler. Varsa `$if$` değerlendirilen koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$else$` koşul denetlenir. Varsa `$else$` koşul `true`, kendi deyimleri sonra çalışır; Aksi halde, `$endif$` koşul ifade değerlendirme sona erer.<br /><br /> Kullanım örnekleri için bkz: [Visual Studio Proje/öğe şablon parametre mantıksal](http://stackoverflow.com/questions/6709057/visual-studio-project-item-template-parameter-logic).|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [MSBuild başvurusu](../msbuild/msbuild-reference.md)   
 [Koşullu yapılar](../msbuild/msbuild-conditional-constructs.md)   
 [İzlenecek yol: Sıfırdan MSBuild Proje Dosyası Oluşturma](../msbuild/walkthrough-creating-an-msbuild-project-file-from-scratch.md)
