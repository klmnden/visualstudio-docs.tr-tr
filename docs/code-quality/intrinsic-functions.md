---
title: İç İşlevler
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _String_length_
- _Param_
- _Curr_
- _Old_
- _Nullterm_length_
- _Inexpressible_
ms.assetid: adf29f8c-89fd-4a5e-9804-35ac83e1c457
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 41ac8e38f501152d329e788572c500f68a8d2214
ms.sourcegitcommit: 21d667104199c2493accec20c2388cf674b195c3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55907964"
---
# <a name="intrinsic-functions"></a>İç İşlevler
SAL bir ifadede, yan etkilere sahip olmayan bir ifade olması şartıyla C/C++ ifade olabilir — örneğin, ++,--ve işlev çağrıları bu bağlamda tümüne sahip yan etkiler.  SAL ancak, bazı işlev benzeri nesnelerin ve SAL ifadelerde kullanılabilir ayrılmış bazı semboller sağlar. Bunlar olarak adlandırılır *iç işlevleri*.

## <a name="general-purpose"></a>Genel Amaçlı
 Aşağıdaki instrinsic işlevi ek açıklamalar için SAL genel yardımcı programını sağlar.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Curr_`|Şu anda Not eklenen nesne için bir eşanlamlı.  Zaman `_At_` ek açıklama, kullanımda olan `_Curr_` ilk parametre olarak aynı `_At_`.  Aksi takdirde, parametre veya ek açıklama sözcüksel olarak ilişkili olduğu tüm işlevi dönüş değeridir.|
|`_Inexpressible_(expr)`|Burada bir arabellek boyutu ek açıklama ifadesi kullanılarak temsil etmek için çok karmaşık bir durum ifade eder — Örneğin, ne zaman, bir giriş veri kümesi tarama ve sonra sayım hesaplanan üyeler seçili.|
|`_Nullterm_length_(param)`|`param` en fazla arabellek ancak bir null Sonlandırıcı içermeden öğeleri sayısıdır. Toplama olmayan, void olmayan tür herhangi bir arabellek için uygulanabilir.|
|`_Old_(expr)`|Önkoşul değerlendirildiğinde `_Old_` giriş değeri döndürür `expr`.  Sonrası koşulu değerlendirilirken, değeri döndürür. `expr` önkoşulu değerlendirilen gibi.|
|`_Param_(n)`|`n`Parametresinden 1'den sayım, bir işleve `n`, ve `n` değişmez değer bir tamsayı sabitidir. Parametre ise, bu ek açıklama parametre adıyla erişmek için aynıdır. **Not:** `n` üç nokta tanımlanan ya da adları değil kullanıldığı işlev prototiplerinde kullanılabilir konumsal parametreleri başvurabilir.|
|`return`|C/C++ ayrılmış anahtar sözcüğü `return` SAL ifadesinde bir işlev dönüş değeri belirtmek için kullanılabilir.  Değer yalnızca post kullanılabilir durumdadır; öncesi durumunda kullanmak için bir söz dizimi hatası var.|

## <a name="string-specific"></a>Belirli dize
 Şu iç işlev ek açıklamaları, dizeleri işlenmesini etkinleştirin. Bu işlevlerin dört aynı amaca hizmet eder: null Sonlandırıcı önce bulunan tür öğelerinin sayısını döndürmek için. Fark başvurulan öğeleri veri türleri vardır. Null ile sonlandırılmış uzunluğunu belirtmek istiyorsanız, arabellek Not değil karakterlerinden oluşan, kullanın `_Nullterm_length_(param)` önceki bölümde ek açıklama.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_String_length_(param)`|`param` dize kadar ancak bir null Sonlandırıcı içermeden öğeleri sayısıdır. Bu ek açıklama karakter dize türleri için ayrılmıştır.|
|`strlen(param)`|`param` dize kadar ancak bir null Sonlandırıcı içermeden öğeleri sayısıdır. Bu ek açıklama ayrılmış karakter kullanın, diziler ve C çalışma zamanı işlevi benzer [strlen()](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l).|
|`wcslen(param)`|`param` en fazla (ancak dahil değil) dizedeki öğe sayısı null Sonlandırıcı. Bu ek açıklama geniş karakter kullanın, diziler ve C çalışma zamanı işlevi benzer ayrılmış [wcslen ()](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l).|

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Yapıları ve Sınıfları Yorumlama](../code-quality/annotating-structs-and-classes.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)