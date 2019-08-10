---
title: Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _Group_
- _At_
- _When_
- _At_buffer_
ms.assetid: 8e4f4f9c-5dfa-4835-87df-ecd1698fc650
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 6c7adb310db9eece1d8d4a2881057cc1acde1062
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68923811"
---
# <a name="specifying-when-and-where-an-annotation-applies"></a>Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme
Ek açıklama koşullu olduğunda, çözümleyiciye belirtmek için diğer ek açıklamalar gerekebilir.  Örneğin, bir işlevin zaman uyumlu veya zaman uyumsuz olabilecek bir değişkeni varsa, işlev aşağıdaki gibi davranır: Zaman uyumlu durumda, her zaman başarılı olur ancak zaman uyumsuz durumda, hemen başarısız olmazsa bir hata bildirir. İşlev zaman uyumlu olarak çağrıldığında, sonuç değerinin denetlenmesi, döndürülmeyeceği için kod Çözümleyicisi 'ne değer vermez.  Ancak, işlev zaman uyumsuz olarak çağrıldığında ve işlev sonucu denetlenirse, ciddi bir hata oluşabilir. Bu örnekte, denetlemeyi etkinleştirmek için `_When_` ek açıklamayı (Bu makalede daha sonra açıklanan) kullanabileceğiniz bir durum gösterilmektedir.

## <a name="structural-annotations"></a>Yapısal ek açıklamaları
Ek açıklamaların ne zaman ve nerede uygulanacağını denetlemek için aşağıdaki yapısal ek açıklamaları kullanın.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_At_(expr, anno-list)`|`expr`, lvalue veren bir ifadedir. İçindeki `anno-list` ek açıklamalar tarafından `expr`adlandırılan nesnesine uygulanır. `anno-list` İçindeki`expr` her ek açıklama için, ek açıklama ön koşul olarak yorumlandığında ön koşul olarak yorumlanır ve ek açıklama koşul sonrası olarak yorumlandığında koşul sonrası olarak yorumlanır.|
|`_At_buffer_(expr, iter, elem-count, anno-list)`|`expr`, lvalue veren bir ifadedir. İçindeki `anno-list` ek açıklamalar tarafından `expr`adlandırılan nesnesine uygulanır. `anno-list` İçindeki`expr` her ek açıklama için, ek açıklamanın ön koşul olarak yorumlanması durumunda ve ek açıklama koşul sonrası olarak yorumlandığında koşul sonrası olarak yorumlanır.<br /><br /> `iter`, ek açıklamanın (dahil `anno-list`) kapsamına alınmış bir değişkenin adıdır. `iter`örtük bir tür `long`içerir. Herhangi bir kapsayan kapsamda aynı adlandırılmış değişkenler değerlendirmeden gizlenir.<br /><br /> `elem-count`, bir tamsayı değerlendiren bir ifadedir.|
|`_Group_(anno-list)`|İçindeki `anno-list` ek açıklamalar her bir ek açıklama için geçerli olan Grup ek açıklamasına uygulanan herhangi bir niteleyiciye sahip olarak kabul edilir.|
|`_When_(expr, anno-list)`|`expr`, öğesine `bool`dönüştürülebileceği bir ifadedir. Sıfır olmayan (`true`) olduğunda, içinde `anno-list` belirtilen ek açıklamalar geçerli kabul edilir.<br /><br /> Varsayılan olarak, içindeki `anno-list` `expr` her ek açıklama için, ek açıklama bir önkoşulun ise ve ek açıklama bir koşul ise çıktı değerlerini kullanarak giriş değerlerini kullanma olarak yorumlanır. Varsayılan değeri geçersiz kılmak için, giriş değerlerinin kullanılması `_Old_` gerektiğini göstermek üzere bir koşulu değerlendirirken iç öğesini kullanabilirsiniz. **Not:**  Bir değişebilir değerin (örneğin, `_When_` `*pLength`), önkoşul olarak değerlendirilen sonucu `expr` , koşul sonrası tarafından değerlendirilen sonuçtan farklı olabileceğinden, buna dahil olan farklı ek açıklamalar etkinleştirilebilir.|

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Yapıları ve Sınıfları Yorumlama](../code-quality/annotating-structs-and-classes.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [İç İşlevler](../code-quality/intrinsic-functions.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)