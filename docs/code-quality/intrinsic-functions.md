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
ms.openlocfilehash: 65a5272d74e1987cd7838932182e7e59c9c53f21
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923943"
---
# <a name="intrinsic-functions"></a>İç İşlevler
SAL içindeki bir ifade, yan etkileri olmayan birC++ ifade olan bir C/ifadesi olabilir; Örneğin, + +,--, ve işlev çağrılarının hepsi bu bağlamda yan etkilere sahiptir.  Ancak, SAL ifadelerde kullanılabilecek bazı işlev benzeri nesneler ve bazı ayrılmış semboller sağlar. Bunlar *iç işlevler*olarak adlandırılır.

## <a name="general-purpose"></a>Genel Amaçlı
Aşağıdaki ınstrinsic işlev ek açıklamaları SAL için genel yardımcı program sağlar.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Curr_`|Şu anda açıklanmakta olan nesne için bir eş anlamlı.  Ek açıklama kullanımda olduğunda, `_Curr_` ilk parametresiyle `_At_`aynı olur. `_At_`  Aksi takdirde, ek açıklamanın sözcüksel olarak ilişkilendirildiği parametre veya tam işlev/dönüş değeridir.|
|`_Inexpressible_(expr)`|Bir arabelleğin boyutunun, bir ek açıklama ifadesi kullanılarak temsil edilebilmesi için çok karmaşık olduğu, örneğin bir girdi veri kümesi tarayarak ve ardından seçilen Üyeler sayımının hesaplandığı bir durumu ifade eder.|
|`_Nullterm_length_(param)`|`param`Arabellekteki öğelerin sayısı, bir null Sonlandırıcı dahil değildir. Toplama olmayan, void olmayan türdeki herhangi bir arabelleğe uygulanabilir.|
|`_Old_(expr)`|Önkoşula göre değerlendirildiğinde, `_Old_` giriş değerini `expr`döndürür.  Koşul sonrası değerlendirildiğinde değeri `expr` , önkoşullardan değerlendirildiği gibi döndürür.|
|`_Param_(n)`|1 ile arasında sayarak ve `n` sabit bir integral sabiti olan bir işleve olan THparametresi.`n` `n` Parametre adlandırılmışsa, bu ek açıklama parametreye adına göre erişmek için aynıdır. **Not:** `n` bir üç nokta tarafından tanımlanan konumsal parametrelere başvurabilir veya adların kullanıldığı işlev Prototiplerde kullanılabilir.|
|`return`|C/C++ ayrılmış anahtar sözcüğü `return` , bir işlevin dönüş değerini göstermek için Sal ifadesinde kullanılabilir.  Değer yalnızca gönderi durumunda kullanılabilir; Bu, ön durumunda kullanmak için bir sözdizimi hatasıdır.|

## <a name="string-specific"></a>Dizeye özgü
Aşağıdaki iç işlev ek açıklamaları dizelerin düzenlenmesini etkinleştirir. Bu işlevlerin dört dördü de aynı amaca sahiptir: null Sonlandırıcı 'dan önce bulunan türdeki öğelerin sayısını döndürmek için. Farklılıklar, başvurulan öğelerdeki veri türleridir. Karakterlerden oluşan null ile sonlandırılmış bir arabelleğin uzunluğunu belirtmek isterseniz, önceki bölümde yer alan `_Nullterm_length_(param)` ek açıklamayı kullanın.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_String_length_(param)`|`param`dizedeki öğe sayısı olan, ancak bir null Sonlandırıcı dahil değil. Bu ek açıklama, karakter dizesi türleri için ayrılmıştır.|
|`strlen(param)`|`param`dizedeki öğe sayısı olan, ancak bir null Sonlandırıcı dahil değil. Bu ek açıklama, karakter dizileri üzerinde kullanılmak üzere ayrılmıştır ve C çalışma zamanı işlevine [strlen ()](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l)benzerdir.|
|`wcslen(param)`|`param`, bir null Sonlandırıcı (dahil değil) olan dizedeki öğe sayısıdır. Bu ek açıklama geniş karakter dizileri üzerinde kullanılmak üzere ayrılmıştır ve C çalışma zamanı işlevine [wcslen ()](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l)benzerdir.|

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Yapıları ve Sınıfları Yorumlama](../code-quality/annotating-structs-and-classes.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)