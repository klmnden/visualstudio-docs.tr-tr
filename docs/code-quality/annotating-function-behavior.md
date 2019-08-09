---
title: İşlev Davranışını Yorumlama
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _On_failure_
- _Return_type_success_
- _Always_
- _Maybe_raises_SEH_exception_
- _Raises_SEH_exception_
- _Called_from_function_class_
- _Function_class_
- _Must_inspect_result_
- _Success_
- _Check_return_
- _Use_decl_annotations_
ms.assetid: c0aa268d-6fa3-4ced-a8c6-f7652b152e61
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: c7ff2551f3a99bf13909f9db3b1659482246e957
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919624"
---
# <a name="annotating-function-behavior"></a>İşlev Davranışını Yorumlama
[İşlev parametrelerine ve dönüş değerlerine](../code-quality/annotating-function-parameters-and-return-values.md)açıklama eklemek için, tüm işlevin özelliklerine ek açıklama ekleyebilirsiniz.

## <a name="function-annotations"></a>İşlev ek açıklamaları
Aşağıdaki ek açıklamalar işlev için bir bütün olarak uygulanır ve nasıl davrandığını veya neyin doğru olmasını beklediğini açıklamaktadır.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Called_from_function_class_(name)`|Tek başına hedeflenmemiştir; Bunun yerine, `_When_` ek açıklamayla birlikte kullanılacak bir koşul vardır. Daha fazla bilgi için bkz. [bir ek açıklamanın ne zaman ve nereye uygulanacağını belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md).<br /><br /> Parametresi, bazı işlevlerin bildirimindeki `_Function_class_` ek açıklamada de görünen rastgele bir dizedir. `name`  `_Called_from_function_class_`Şu anda çözümlenmekte olan işleve aynı değere sahip olan ' i kullanarak `_Function_class_` açıklanmışsa sıfır dışında bir `name`değer döndürür; Aksi takdirde, sıfır döndürür.|
|`_Check_return_`|Bir dönüş değeri ve çağıranın bunu incelemesi gerektiğini belirten bir açıklama. İşlev void bağlamda çağrılırsa, denetleyici bir hata bildirir.|
|`_Function_class_(name)`|`name` Parametresi, Kullanıcı tarafından atanan rastgele bir dizedir.  Diğer ad alanlarından farklı bir ad alanında bulunur. Bir işlev, işlev işaretçisi veya — en çok usetam — bir işlev işaretçisi türü bir veya daha fazla işlev sınıfına ait olarak belirlenebilir.|
|`_Raises_SEH_exception_`|Her zaman yapılandırılmış bir özel durum işleyicisi (SEH) özel durumu, konu `_When_` ve `_On_failure_` koşullara tabi olan bir işlevi annotates. Daha fazla bilgi için bkz. [bir ek açıklamanın ne zaman ve nereye uygulanacağını belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md).|
|`_Maybe_raises_SEH_exception_`|İsteğe bağlı olarak bir seh özel durumu, konu `_When_` ve `_On_failure_` koşullara tabi olabilecek bir işlevi annotates.|
|`_Must_inspect_result_`|Dönüş değeri, parametreler ve Globals 'ler dahil olmak üzere herhangi bir çıkış değerini öğretme.  Açıklamalı nesnede bulunan değer daha sonra incelenemediği çözümleyici bir hata bildirir. "Denetleme", bir koşullu ifadede kullanılıp kullanılmadığını, bir çıkış parametresine veya genel 'e atandığını veya bir parametre olarak geçtiğini içerir.  Dönüş değerleri için, `_Must_inspect_result_` şunu `_Check_return_`gösterir.|
|`_Use_decl_annotations_`|Başlıktaki ek açıklamaların listesi yerine bir işlev tanımında (işlev gövdesi olarak da bilinir) kullanılabilir.  Kullanıldığında, aynı işlev için kapsam içi üst bilgisinde görünen ek açıklamalar, `_Use_decl_annotations_` ek açıklamasına sahip tanımda de mevcuttur gibi kullanılır. `_Use_decl_annotations_`|

## <a name="successfailure-annotations"></a>Başarı/başarısızlık ek açıklamaları
Bir işlev başarısız olabilir ve ne zaman, işlev başarılı olduğunda sonuçları tamamlanmamış veya sonuçlardan farklı olabilir.  Aşağıdaki listedeki ek açıklamalar başarısızlık davranışını ifade etmenin yollarını sağlar.  Bu ek açıklamaları kullanmak için, bunları başarıyı tespit etmek üzere etkinleştirmeniz gerekir. Bu nedenle, `_Success_` ek açıklama gereklidir.  Ve `NTSTATUS` `_Success_` `HRESULT` `NTSTATUS` içinde yerleşik olarak bulunan bir `_Success_` ek açıklamanın zaten olduğunu fark edin; ancak, veya üzerinde kendi ek açıklamanızı belirtirseniz, yerleşik ek açıklamayı geçersiz kılar. `HRESULT`

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Always_(anno_list)`|Eşdeğerdir; diğer bir deyişle, içindeki `anno_list` ek açıklamalar işlevin başarılı olup olmadığını uygular. `anno_list _On_failure_(anno_list)`|
|`_On_failure_(anno_list)`|Yalnızca `_Success_` , bir typedef `_Return_type_success_` üzerinde açıkça veya örtük olarak işlev üzerine eklemek için de kullanıldığında kullanılır. `_When_(!expr, anno)` `anno_list` `_Success_` `expr` Ek açıklama bir işlev parametresi veya dönüş değeri üzerinde olduğunda, (Anno) içindeki her ek açıklama olarak kodlanmış gibi davranır, burada parametre gerekli ek açıklamanın parametresidir. `_On_failure_` Bu, ' nin `_Success_` tüm koşullar için `_On_failure_`geçerli olmadığı anlamına gelir.|
|`_Return_type_success_(expr)`|Bir typedef 'e uygulanabilir. Bu türü döndüren ve açıkça sahip `_Success_` olmayan tüm işlevlere sahip `_Success_(expr)`oldukları gibi açıklama eklenmiş olduğunu gösterir. `_Return_type_success_`bir işlevde veya bir işlev işaretçisi typedef üzerinde kullanılamaz.|
|`_Success_(expr)`|`expr`, rvalue veren bir ifadedir. Ek açıklama bir işlev bildiriminde veya tanımında olduğunda, işlevdeki ve koşul sonrasındaki her ek`anno`açıklama () olarak `_When_(expr, anno)`kodlanmış gibi davranır. `_Success_` Ek `_Success_` açıklama, parametreleri veya dönüş türü üzerinde değil, yalnızca bir işlevde kullanılabilir. Bir işlevde `_Success_` en fazla bir ek açıklama olabilir ve herhangi `_When_`bir, `_At_`veya `_Group_`içinde olamaz. Daha fazla bilgi için bkz. [bir ek açıklamanın ne zaman ve nereye uygulanacağını belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md).|

## <a name="see-also"></a>Ayrıca bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [Yapıları ve Sınıfları Yorumlama](../code-quality/annotating-structs-and-classes.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [İç İşlevler](../code-quality/intrinsic-functions.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)