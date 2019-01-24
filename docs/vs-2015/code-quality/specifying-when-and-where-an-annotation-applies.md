---
title: Açıklamanın ne zaman ve nereye uygulanacağını belirtme | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: conceptual
f1_keywords:
- _Group_
- _At_
- _When_
- _At_buffer_
ms.assetid: 8e4f4f9c-5dfa-4835-87df-ecd1698fc650
caps.latest.revision: 9
author: mikeblome
ms.author: mblome
manager: jillfra
ms.openlocfilehash: ba14fdbc23968fcaf10355f73517ab6cd54f8797
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54764676"
---
# <a name="specifying-when-and-where-an-annotation-applies"></a>Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Bir ek açıklama koşullu olduğunda, diğer ek açıklamalar Çözümleyicisi belirtmek için gerekli olabilir.  Örneğin, bir işlevi zaman uyumlu veya zaman uyumsuz bir değişken varsa, işlev gibi davranır: Zaman uyumlu durumunda her zaman sonunda başarılı, ancak bunu hemen başarısız zaman uyumsuz durumda, bir hata bildirir. İşlevi zaman uyumlu olarak çağrıldığında değil döndüğünüzü çünkü sonuç değeri denetimi için kod Çözümleyicisi hiçbir değer sağlar.  Bununla birlikte, işlev zaman uyumsuz olarak adlandırılır ve işlev sonucu işaretli olduğunda, ciddi bir hata oluşabilir. Bu örnekte, bir durum kullanma gösterilmektedir `_When_` ek açıklama: Bu makalenin sonraki bölümlerinde açıklanan — denetimini etkinleştirmek için.  
  
## <a name="structural-annotations"></a>Yapısal ek açıklamaları  
 Ne zaman ve nerede ek açıklamaları uygulayın denetlemek için aşağıdaki yapısal ek açıklamaları kullanın.  
  
|Ek Açıklama|Açıklama|  
|----------------|-----------------|  
|`_At_(expr, anno-list)`|`expr` lvalue döndüren bir ifadedir. Ek açıklamalarda `anno-list` tarafından adlandırılan bir nesneye uygulanan `expr`. Her ek açıklaması için `anno-list`, `expr` ek açıklama ön koşul yorumlanır ve sonrası koşul ise ek açıklama sonrası koşul olarak yorumlanır ön koşul yorumlanır.|  
|`_At_buffer_(expr, iter, elem-count, anno-list)`|`expr` lvalue döndüren bir ifadedir. Ek açıklamalarda `anno-list` tarafından adlandırılan bir nesneye uygulanan `expr`. Her ek açıklaması için `anno-list`, `expr` ek açıklama önkoşulu yorumlanır ve sonrası koşul ise ek açıklama sonrası koşul olarak yorumlanır ön koşul yorumlanır.<br /><br /> `iter` ek açıklama için kapsamlı bir değişken adıdır (inclusive, `anno-list`). `iter` örtük bir türe sahip `long`. Tüm kapsayan kapsam içinde aynı adlı değişkenlere değerlendirmesinden gelen gizlidir.<br /><br /> `elem-count` bir tamsayı döndüren bir ifadedir.|  
|`_Group_(anno-list)`|Ek açıklamalarda `anno-list` tüm her bir ek açıklama için uygulanan Grup ek açıklama uygulandığı herhangi niteleyicisi olduğu kabul edilir.|  
|`_When_(expr, anno-list)`|`expr` dönüştürülebilir bir ifadedir `bool`. Sıfır dışında olduğunda (`true`), belirtilen ek açıklamalar `anno-list` geçerli olarak kabul edilir.<br /><br /> Varsayılan olarak her eklenti için `anno-list`, `expr` ek açıklama bir önkoşul, ve ek açıklama sonrası bir koşul ise, çıktı değerleri kullanarak olarak giriş değerleri kullanarak olarak yorumlanır. Varsayılanı geçersiz kılmak için kullanabilirsiniz `_Old_` giriş değerleri kullanılması gerektiğini belirtmek için sonrası bir koşul değerlendirdiğinde iç. **Not:**  Farklı ek açıklamalar kullanarak söz konusu kümelerdeki etkinleştirilmesi `_When_` değişebilir bir değer — Örneğin, `*pLength`— çünkü söz konusu değerlendirilen sonucunu `expr` önkoşulu değerlendirilen sonucunu sonrası koşulunda farklılık gösterebilir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [C/C++ kod hatalarını azaltmak için SAL ek açıklamalarını kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)   
 [SAL'yi anlama](../code-quality/understanding-sal.md)   
 [İşlev parametrelerini ve dönüş değerlerini açıklama](../code-quality/annotating-function-parameters-and-return-values.md)   
 [İşlev davranışını yorumlama](../code-quality/annotating-function-behavior.md)   
 [Yapıları ve sınıfları yorumlama](../code-quality/annotating-structs-and-classes.md)   
 [Kilitlenme davranışını yorumlama](../code-quality/annotating-locking-behavior.md)   
 [İç işlevleri](../code-quality/intrinsic-functions.md)   
 [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)
