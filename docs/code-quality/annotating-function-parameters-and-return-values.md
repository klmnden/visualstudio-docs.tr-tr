---
title: İşlev Parametrelerini ve Dönüş Değerlerini Açıklama
ms.date: 07/11/2019
ms.topic: conceptual
f1_keywords:
- _Outptr_opt_result_bytebuffer_to_
- _Inout_updates_all_opt_
- _Post_equal_to_
- _Outptr_opt_result_maybenull_
- _Out_writes_bytes_all_
- _Out_writes_all_opt_
- _In_opt_
- _Outptr_
- _Outptr_result_maybenull_
- _Outref_result_bytebuffer_all_maybenull_
- _Inout_updates_opt_z_
- _Inout_updates_z_
- _Out_writes_
- _Out_writes_to_ptr_opt_z_
- _In_reads_to_ptr_opt_
- _Ret_writes_to_maybenull_
- _Outref_result_maybenull_
- _Ret_writes_bytes_
- _Outptr_result_bytebuffer_
- _Out_writes_opt_
- _Inout_updates_bytes_opt_
- _In_z_
- _Inout_updates_to_
- _Ret_maybenull_
- _Ret_writes_bytes_to_
- _Ret_z_
- _COM_Outptr_
- _Ret_maybenull_z_
- _Out_opt_
- _In_reads_opt_z_
- _Outptr_result_bytebuffer_to_
- _Ret_notnull_
- _COM_Outptr_opt_result_maybenull_
- _Inout_updates_to_opt_
- _Inout_updates_
- _Outptr_opt_result_buffer_
- _Outptr_result_buffer_to_
- _Out_writes_to_ptr_opt_
- _Out_writes_bytes_all_opt_
- _Inout_updates_all_
- _Deref_inout_range_
- _Ret_writes_
- _Out_writes_z_
- _Ret_writes_to_
- _Out_writes_to_ptr_z_
- _Out_writes_bytes_to_opt_
- _In_reads_or_z_
- _Inout_updates_bytes_to_
- _In_reads_z_
- _In_opt_z_
- _Outref_result_buffer_maybenull_
- _Ret_range_
- _COM_Outptr_opt_
- _Ouptr_opt_result_maybenull_z_
- _In_reads_opt_
- _Inout_
- _Field_range_
- _Ret_writes_z_
- _Out_writes_to_
- _Out_writes_to_ptr_
- _Inout_opt_z_
- _Outref_
- _Deref_out_range_
- _Outref_result_buffer_
- _Outref_result_buffer_to_
- _Outref_result_bytebuffer_to_maybenull_
- _In_reads_bytes_
- _Outptr_opt_result_buffer_to_
- _Outref_result_buffer_all_
- _Out_writes_bytes_to_
- _Result_zeroonfailure_
- _In_reads_bytes_opt_
- _Outref_result_buffer_to_maybenull_
- _Outref_result_bytebuffer_all_
- _Outref_result_buffer_all_maybenull_
- _Ret_writes_maybenull_z_
- _In_range_
- _Inout_updates_bytes_all_opt_
- _Outref_result_bytebuffer_to_
- _Inout_updates_bytes_to_opt_
- _Pre_equal_to_
- _Ret_writes_bytes_maybenull_
- _COM_Outptr_result_maybenull_
- _Ret_writes_maybenull_
- _Out_writes_bytes_
- _Outptr_opt_
- _Out_writes_opt_z_
- _Outref_result_nullonfailure_
- _Outptr_opt_result_z_
- _Inout_opt_
- _Deref_in_range_
- _Outptr_result_z_
- _In_reads_to_ptr_opt_z_
- _Struct_size_bytes_
- _Outptr_result_nullonfailure_
- _In_
- _Inout_updates_bytes_
- _In_reads_to_ptr_z_
- _Ret_writes_bytes_to_maybenull
- _Outptr_opt_result_nullonfailure_
- _In_reads_to_ptr_
- _Outptr_result_buffer_
- _Out_
- _Outref_result_bytebuffer_maybenull_
- _Outptr_result_maybenull_z_
- _In_reads_
- _Inout_updates_opt_
- _Out_writes_to_opt_
- _Outptr_opt_result_bytebuffer_
- _Out_writes_all_
- _Out_range_
- _Inout_updates_bytes_all_
- _Inout_z_
- _Outref_result_bytebuffer_
- _Result_nullonfailure_
- _Ret_null_
- _Scanf_format_string_
- _Scanf_s_format_string_
- _Printf_format_string_
ms.assetid: 82826a3d-0c81-421c-8ffe-4072555dca3a
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 8f07650e47398b028460776f41557a3f853eaad3
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919622"
---
# <a name="annotating-function-parameters-and-return-values"></a>İşlev Parametrelerini ve Dönüş Değerlerini Açıklama
Bu makalede basit işlev parametreleri için ek açıklamaların tipik kullanımları ve yapı ve sınıf işaretçileri ve birçok arabellek türü açıklanmaktadır.  Bu makalede ayrıca ek açıklamalar için ortak kullanım desenleri gösterilmektedir. İşlevlerle ilgili ek ek açıklamalar için bkz. [Işlev davranışına açıklama ekleme](../code-quality/annotating-function-behavior.md).

## <a name="pointer-parameters"></a>İşaretçi parametreleri
Aşağıdaki tablodaki ek açıklamalar için, işaretçi parametresine açıklama eklendiğinde, işaretçi null ise çözümleyici bir hata bildirir.  Bu, işaretçiler için ve işaret edilen tüm veri öğeleri için geçerlidir.

**Ek açıklamalar ve açıklamalar**

- `_In_`

     Yapılar, yapılar, yapılara yönelik işaretçiler ve benzeri bir giriş parametresi olan annotates.  Açıkça basit dolandırıcıklar üzerinde kullanılabilir.  Parametrenin ön durumunda geçerli olması ve değiştirilmeyecektir.

- `_Out_`

     Yapıları, yapıları, yapılara yönelik işaretçileri ve benzeri bir çıkış parametresi olan annotates.  Bunu değer döndürmeyen bir nesneye uygulamayın — Örneğin, değere göre geçirilmiş bir skaler.  Parametrenin ön durumunda geçerli olması gerekmez, ancak durum sonrası için geçerli olmalıdır.

- `_Inout_`

     İşlev tarafından değiştirilecek bir parametreyi annotates.  Hem ön durum hem de durum durumunda geçerli olmalıdır, ancak çağrıdan önce ve sonra farklı değerlere sahip olduğu varsayılır. Değiştirilebilir bir değere uygulamanız gerekir.

- `_In_z_`

     Giriş olarak kullanılan null ile sonlandırılmış bir dize işaretçisi.  Dize, ön durumunda geçerli olmalıdır.  `PSTR`Zaten doğru ek açıklamaların bulunduğu varyantlar tercih edilir.

- `_Inout_z_`

     Değiştirilecek, null ile sonlandırılmış bir karakter dizisine yönelik bir işaretçi.  Çağrıdan önce ve sonra geçerli olmalıdır, ancak değer değişmiş olarak kabul edilir.  Null Sonlandırıcı taşınabilir, ancak yalnızca orijinal null sonlandırıcısına kadar olan öğelere erişilebilir.

- `_In_reads_(s)`

     `_In_reads_bytes_(s)`

     İşlev tarafından okunan dizi için bir işaretçi.  Dizi, hepsi geçerli olması `s` gereken boyut öğeleridir.

     `_bytes_` Değişken, boyutu öğeler yerine bayt olarak verir. Bunu yalnızca boyut öğe olarak ifade edilemez ' i kullanın.  Örneğin, `char` dizeler yalnızca kullanan `wchar_t` benzer bir `_bytes_` işlev ise değişkeni kullanır.

- `_In_reads_z_(s)`

     Null sonlandırılmış ve bilinen bir boyuta sahip dizi için bir işaretçi. Null sonlandırıcısına sahip öğeler — veya `s` null Sonlandırıcı yoksa, ön durumunda geçerli olmalıdır.  Boyut bayt olarak biliniyorsa öğe boyutuna göre ölçeklendirin `s` .

- `_In_reads_or_z_(s)`

     Null sonlandırılmış veya bilinen bir boyut veya her ikisi içeren bir dizi işaretçisi. Null sonlandırıcısına sahip öğeler — veya `s` null Sonlandırıcı yoksa, ön durumunda geçerli olmalıdır.  Boyut bayt olarak biliniyorsa öğe boyutuna göre ölçeklendirin `s` .  ( `strn` Aile için kullanılır.)

- `_Out_writes_(s)`

     `_Out_writes_bytes_(s)`

     İşlev tarafından yazılacak `s` öğe (yanıt. bayt) dizisine yönelik bir işaretçi.  Dizi öğelerinin ön durumunda geçerli olması gerekmez ve durum sonrası için geçerli olan öğe sayısı belirtilmemiş olur.  Parametre türünde ek açıklamalar varsa, bunlar durum sonrası ' a uygulanır. Örneğin, aşağıdaki kodu göz önünde bulundurun.

     `typedef _Null_terminated_ wchar_t *PWSTR; void MyStringCopy(_Out_writes_ (size) PWSTR p1,    _In_ size_t size,    _In_ PWSTR p2);`

     Bu örnekte, çağıran `size` öğesi için `p1`bir arabellek sağlar.  `MyStringCopy`Bu öğelerin bazılarını geçerli hale getirir. Daha da önemlisi, `_Null_terminated_` üzerindeki `PWSTR` ek açıklama, `p1` durum sonrası için null olarak sonlandırılmış anlamına gelir.  Bu şekilde, geçerli öğe sayısı hala iyi tanımlanmış, ancak belirli bir öğe sayısı gerekli değildir.

     `_bytes_` Değişken, boyutu öğeler yerine bayt olarak verir. Bunu yalnızca boyut öğe olarak ifade edilemez ' i kullanın.  Örneğin, `char` dizeler yalnızca kullanan `wchar_t` benzer bir `_bytes_` işlev ise değişkeni kullanır.

- `_Out_writes_z_(s)`

     `s` Öğe dizisine yönelik bir işaretçi.  Öğelerin ön durumunda geçerli olması gerekmez.  Durum sonrası 'de, mevcut olması gereken null Sonlandırıcı aracılığıyla bulunan öğeler geçerli olmalıdır.  Boyut bayt olarak biliniyorsa öğe boyutuna göre ölçeklendirin `s` .

- `_Inout_updates_(s)`

     `_Inout_updates_bytes_(s)`

     Bir dizi için, hem okunan hem de işlevine yazılan bir işaretçi.  Bu, bir boyut `s` öğeleridir ve ön durum ve durum sonrası için geçerlidir.

     `_bytes_` Değişken, boyutu öğeler yerine bayt olarak verir. Bunu yalnızca boyut öğe olarak ifade edilemez ' i kullanın.  Örneğin, `char` dizeler yalnızca kullanan `wchar_t` benzer bir `_bytes_` işlev ise değişkeni kullanır.

- `_Inout_updates_z_(s)`

     Null sonlandırılmış ve bilinen bir boyuta sahip dizi için bir işaretçi. Mevcut olması gereken null Sonlandırıcı aracılığıyla bulunan öğeler, hem ön durum hem de durum sonrası için geçerli olmalıdır.  Durum sonrası değeri, ön durumundaki değerden farklı olacak şekilde belirlenir; Bu, null Sonlandırıcı konumunu içerir. Boyut bayt olarak biliniyorsa öğe boyutuna göre ölçeklendirin `s` .

- `_Out_writes_to_(s,c)`

     `_Out_writes_bytes_to_(s,c)`

     `_Out_writes_all_(s)`

     `_Out_writes_bytes_all_(s)`

     `s` Öğe dizisine yönelik bir işaretçi.  Öğelerin ön durumunda geçerli olması gerekmez.  Durum sonrası, `c`-TH öğesine kadar olan öğelerin geçerli olması gerekir.  Boyut bayt cinsinden bilindiğinde, `s` `_bytes_` öğe boyutuna göre ve `c` , ölçeği kullanın veya şu şekilde tanımlanan değişkeni kullanın:

     `_Out_writes_to_(_Old_(s), _Old_(s))    _Out_writes_bytes_to_(_Old_(s), _Old_(s))`

     Diğer bir deyişle, ön durumunda olan arabellekte `s` bulunan her öğe, son durum durumunda geçerlidir.  Örneğin:

     `void *memcpy(_Out_writes_bytes_all_(s) char *p1,    _In_reads_bytes_(s) char *p2,    _In_ int s); void * wordcpy(_Out_writes_all_(s) DWORD *p1,     _In_reads_(s) DWORD *p2,    _In_ int s);`

- `_Inout_updates_to_(s,c)`

     `_Inout_updates_bytes_to_(s,c)`

     İşlev tarafından hem okunan hem yazılan dizi için bir işaretçi.  Bu, tümünün ön `s` durumunda geçerli olması gereken bir boyut öğeleridir ve `c` öğelerin durum sonrası geçerli olması gerekir.

     `_bytes_` Değişken, boyutu öğeler yerine bayt olarak verir. Bunu yalnızca boyut öğe olarak ifade edilemez ' i kullanın.  Örneğin, `char` dizeler yalnızca kullanan `wchar_t` benzer bir `_bytes_` işlev ise değişkeni kullanır.

- `_Inout_updates_z_(s)`

     Null sonlandırılmış ve bilinen bir boyuta sahip dizi için bir işaretçi. Mevcut olması gereken null Sonlandırıcı aracılığıyla bulunan öğeler, hem ön durum hem de durum sonrası için geçerli olmalıdır.  Durum sonrası değeri, ön durumundaki değerden farklı olacak şekilde belirlenir; Bu, null Sonlandırıcı konumunu içerir. Boyut bayt olarak biliniyorsa öğe boyutuna göre ölçeklendirin `s` .

- `_Out_writes_to_(s,c)`

     `_Out_writes_bytes_to_(s,c)`

     `_Out_writes_all_(s)`

     `_Out_writes_bytes_all_(s)`

     `s` Öğe dizisine yönelik bir işaretçi.  Öğelerin ön durumunda geçerli olması gerekmez.  Durum sonrası, `c`-TH öğesine kadar olan öğelerin geçerli olması gerekir.  Boyut bayt cinsinden bilindiğinde, `s` `_bytes_` öğe boyutuna göre ve `c` , ölçeği kullanın veya şu şekilde tanımlanan değişkeni kullanın:

     `_Out_writes_to_(_Old_(s), _Old_(s))    _Out_writes_bytes_to_(_Old_(s), _Old_(s))`

     Diğer bir deyişle, ön durumunda olan arabellekte `s` bulunan her öğe, son durum durumunda geçerlidir.  Örneğin:

     `void *memcpy(_Out_writes_bytes_all_(s) char *p1,    _In_reads_bytes_(s) char *p2,    _In_ int s); void * wordcpy(_Out_writes_all_(s) DWORD *p1,     _In_reads_(s) DWORD *p2,    _In_ int s);`

- `_Inout_updates_to_(s,c)`

     `_Inout_updates_bytes_to_(s,c)`

     İşlev tarafından hem okunan hem yazılan dizi için bir işaretçi.  Bu, tümünün ön `s` durumunda geçerli olması gereken bir boyut öğeleridir ve `c` öğelerin durum sonrası geçerli olması gerekir.

     `_bytes_` Değişken, boyutu öğeler yerine bayt olarak verir. Bunu yalnızca boyut öğe olarak ifade edilemez ' i kullanın.  Örneğin, `char` dizeler yalnızca kullanan `wchar_t` benzer bir `_bytes_` işlev ise değişkeni kullanır.

- `_Inout_updates_all_(s)`

     `_Inout_updates_bytes_all_(s)`

     Boyut `s` öğelerinin işlevi tarafından hem okunan hem yazılan dizi için bir işaretçi. Eşdeğer olarak tanımlanan:

     `_Inout_updates_to_(_Old_(s), _Old_(s))    _Inout_updates_bytes_to_(_Old_(s), _Old_(s))`

     Diğer bir deyişle, ön durumunda olan arabellekte `s` bulunan her öğe, ön durum ve sonrası durumunda geçerlidir.

     `_bytes_` Değişken, boyutu öğeler yerine bayt olarak verir. Bunu yalnızca boyut öğe olarak ifade edilemez ' i kullanın.  Örneğin, `char` dizeler yalnızca kullanan `wchar_t` benzer bir `_bytes_` işlev ise değişkeni kullanır.

- `_In_reads_to_ptr_(p)`

     İfadenin `p` ( - yani eksi)`_Curr_`uygun dil standardı tarafından tanımlandığı diziye yönelik bir işaretçi. `p` `_Curr_`  Öncesindeki öğelerin ön durumunda `p` geçerli olması gerekir.

- `_In_reads_to_ptr_z_(p)`

     İfadenin `p` ( - yani eksi)`_Curr_`uygun dil standardı tarafından tanımlandığı, null ile sonlandırılmış dizi için bir işaretçi. `p` `_Curr_`  Öncesindeki öğelerin ön durumunda `p` geçerli olması gerekir.

- `_Out_writes_to_ptr_(p)`

     İfadenin `p` ( - yani eksi)`_Curr_`uygun dil standardı tarafından tanımlandığı diziye yönelik bir işaretçi. `p` `_Curr_`  ' Den önceki `p` öğelerin ön durumunda geçerli olması gerekmez ve durum sonrası için geçerli olmalıdır.

- `_Out_writes_to_ptr_z_(p)`

     İfadenin `p` ( - yani eksi)`_Curr_`uygun dil standardı tarafından tanımlandığı, null ile sonlandırılmış dizi için bir işaretçi. `p` `_Curr_`  ' Den önceki `p` öğelerin ön durumunda geçerli olması gerekmez ve durum sonrası için geçerli olmalıdır.

## <a name="optional-pointer-parameters"></a>İsteğe bağlı Işaretçi parametreleri

Bir işaretçi parametresi ek açıklaması içerdiğinde `_opt_`, parametrenin null olabileceğini gösterir. Aksi takdirde, ek açıklama dahil `_opt_`olmayan sürümle aynı şekilde gerçekleştirilir. Bu, işaretçi parametresi ek açıklamaların `_opt_` türevlerini listeler:

||||
|-|-|-|
|`_In_opt_`<br /><br /> `_Out_opt_`<br /><br /> `_Inout_opt_`<br /><br /> `_In_opt_z_`<br /><br /> `_Inout_opt_z_`<br /><br /> `_In_reads_opt_`<br /><br /> `_In_reads_bytes_opt_`<br /><br /> `_In_reads_opt_z_`|`_Out_writes_opt_`<br /><br /> `_Out_writes_opt_z_`<br /><br /> `_Inout_updates_opt_`<br /><br /> `_Inout_updates_bytes_opt_`<br /><br /> `_Inout_updates_opt_z_`<br /><br /> `_Out_writes_to_opt_`<br /><br /> `_Out_writes_bytes_to_opt_`<br /><br /> `_Out_writes_all_opt_`<br /><br /> `_Out_writes_bytes_all_opt_`|`_Inout_updates_to_opt_`<br /><br /> `_Inout_updates_bytes_to_opt_`<br /><br /> `_Inout_updates_all_opt_`<br /><br /> `_Inout_updates_bytes_all_opt_`<br /><br /> `_In_reads_to_ptr_opt_`<br /><br /> `_In_reads_to_ptr_opt_z_`<br /><br /> `_Out_writes_to_ptr_opt_`<br /><br /> `_Out_writes_to_ptr_opt_z_`|

## <a name="output-pointer-parameters"></a>Çıkış Işaretçisi parametreleri
Çıkış işaretçisi parametreleri, parametre ve işaret konumu üzerinde null olma durumunu belirsizliğini ortadan kaldırmak için özel bir gösterim gerektirir.

**Ek açıklamalar ve açıklamalar**

- `_Outptr_`

   Parametre null olamaz ve durum son durumunda, işaret edilen konum null olamaz ve geçerli olmalıdır.

- `_Outptr_opt_`

   Parametre null olabilir, ancak durum sonrası, noktadan sonra gelen konum null olamaz ve geçerli olmalıdır.

- `_Outptr_result_maybenull_`

   Parametre null olamaz ve durum son durumunda, işaret edilen konum null olabilir.

- `_Outptr_opt_result_maybenull_`

   Parametre null olabilir ve durum son durumunda, işaret edilen konum null olabilir.

  Aşağıdaki tabloda ek alt dizeler, ek açıklamanın anlamını daha fazla nitelemek için ek bir açıklama adına eklenir.  `_z`Çeşitli alt dizeler ,`_bytebuffer_` ,,`_to_`ve ' dir. `_COM_` `_buffer_`

> [!IMPORTANT]
> Not ettiğiniz arabirim COM ise, bu ek açıklamaların COM formunu kullanın. Diğer tür arabirimlerle COM ek açıklamalarını kullanmayın.

**Ek açıklamalar ve açıklamalar**

- `_Outptr_result_z_`

   `_Outptr_opt_result_z_`

   `_Outptr_result_maybenull_z_`

   `_Ouptr_opt_result_maybenull_z_`

   Döndürülen işaretçinin `_Null_terminated_` ek açıklaması vardır.

- `_COM_Outptr_`

   `_COM_Outptr_opt_`

   `_COM_Outptr_result_maybenull_`

   `_COM_Outptr_opt_result_maybenull_`

   Döndürülen işaretçinin com semantiği vardır ve bu nedenle döndürülen işaretçinin null `_On_failure_` olduğunu belirten bir koşul taşır.

- `_Outptr_result_buffer_(s)`

   `_Outptr_result_bytebuffer_(s)`

   `_Outptr_opt_result_buffer_(s)`

   `_Outptr_opt_result_bytebuffer_(s)`

   Döndürülen işaretçi, öğe veya bayt boyutundaki `s` geçerli bir arabelleğe işaret ediyor.

- `_Outptr_result_buffer_to_(s, c)`

   `_Outptr_result_bytebuffer_to_(s, c)`

   `_Outptr_opt_result_buffer_to_(s,c)`

   `_Outptr_opt_result_bytebuffer_to_(s,c)`

   Döndürülen işaretçi, öğe veya bayt boyutlu `s` bir arabelleğe işaret eder. Bu, ilki `c` geçerli olur.

  Belirli arabirim kuralları, hata durumunda çıkış parametrelerinin null olduğunu varsayar.  Açık COM kodu hariç, aşağıdaki tablodaki formlar tercih edilir.  COM kodu için, önceki bölümde listelenen ilgili COM formlarını kullanın.

  **Ek açıklamalar ve açıklamalar**

- `_Result_nullonfailure_`

   Diğer ek açıklamaları değiştirir. İşlev başarısız olursa sonuç null olarak ayarlanır.

- `_Result_zeroonfailure_`

   Diğer ek açıklamaları değiştirir. İşlev başarısız olursa sonuç sıfır olarak ayarlanır.

- `_Outptr_result_nullonfailure_`

   Döndürülen işaretçi, işlev başarılı olursa geçerli bir arabelleğe işaret eder veya işlev başarısız olursa null olur. Bu ek açıklama isteğe bağlı olmayan bir parametre içindir.

- `_Outptr_opt_result_nullonfailure_`

   Döndürülen işaretçi, işlev başarılı olursa geçerli bir arabelleğe işaret eder veya işlev başarısız olursa null olur. Bu ek açıklama isteğe bağlı bir parametre içindir.

- `_Outref_result_nullonfailure_`

   Döndürülen işaretçi, işlev başarılı olursa geçerli bir arabelleğe işaret eder veya işlev başarısız olursa null olur. Bu ek açıklama bir başvuru parametresi içindir.

## <a name="output-reference-parameters"></a>Çıkış başvurusu parametreleri

Başvuru parametresinin ortak kullanımı çıkış parametrelerine yöneliktir.  Basit çıkış başvuru parametreleri için — örneğin, `int&`—`_Out_` doğru semantiği sağlar.  Ancak, çıkış değeri bir işaretçisiyse — örneğin `int *&`, benzer `_Outptr_ int **` işaretçi ek açıklamaları doğru anlambilimi sağlamaz.  İşaretçi türleri için çıkış başvurusu parametrelerinin semantiğini öz için, bu bileşik ek açıklamaları kullanın:

**Ek açıklamalar ve açıklamalar**

- `_Outref_`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz.

- `_Outref_result_maybenull_`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak durum sonrası null olabilir.

- `_Outref_result_buffer_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz. Geçerli boyut `s` öğeleri arabelleğini işaret eder.

- `_Outref_result_bytebuffer_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz. Geçerli boyut `s` baytları arabelleğini işaret eder.

- `_Outref_result_buffer_to_(s, c)`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz. `s` İlk`c` geçerli olan öğe arabelleğini işaret eder.

- `_Outref_result_bytebuffer_to_(s, c)`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz. `s` İlk`c` geçerli olan bayt arabelleğini işaret eder.

- `_Outref_result_buffer_all_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz. Geçerli öğelerin boyutunu `s` geçerli arabelleğe işaret eder.

- `_Outref_result_bytebuffer_all_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır ve null olamaz. Geçerli öğe `s` baytlarının geçerli arabelleğini işaret eder.

- `_Outref_result_buffer_maybenull_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak durum sonrası null olabilir. Geçerli boyut `s` öğeleri arabelleğini işaret eder.

- `_Outref_result_bytebuffer_maybenull_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak durum sonrası null olabilir. Geçerli boyut `s` baytları arabelleğini işaret eder.

- `_Outref_result_buffer_to_maybenull_(s, c)`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak durum sonrası null olabilir. `s` İlk`c` geçerli olan öğe arabelleğini işaret eder.

- `_Outref_result_bytebuffer_to_maybenull_(s,c)`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak post durumunda null olabilir. `s` İlk`c` geçerli olan bayt arabelleğini işaret eder.

- `_Outref_result_buffer_all_maybenull_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak post durumunda null olabilir. Geçerli öğelerin boyutunu `s` geçerli arabelleğe işaret eder.

- `_Outref_result_bytebuffer_all_maybenull_(s)`

     Sonuç, durum sonrası için geçerli olmalıdır, ancak post durumunda null olabilir. Geçerli öğe `s` baytlarının geçerli arabelleğini işaret eder.

## <a name="return-values"></a>Dönüş Değerleri

Bir işlevin dönüş değeri `_Out_` parametreye benzer, ancak farklı bir de başvuru düzeyindedir ve işaretçi kavramını sonuca düşünmek zorunda kalmazsınız.  Aşağıdaki ek açıklamalar için, dönüş değeri, bir skalar, bir struct işaretçisi veya bir arabelleğin işaretçisi olan açıklamalı nesnedir. Bu ek açıklamalar, ilgili `_Out_` ek açıklamayla aynı semantiğe sahiptir.

|||
|-|-|
|`_Ret_z_`<br /><br /> `_Ret_writes_(s)`<br /><br /> `_Ret_writes_bytes_(s)`<br /><br /> `_Ret_writes_z_(s)`<br /><br /> `_Ret_writes_to_(s,c)`<br /><br /> `_Ret_writes_maybenull_(s)`<br /><br /> `_Ret_writes_to_maybenull_(s)`<br /><br /> `_Ret_writes_maybenull_z_(s)`|`_Ret_maybenull_`<br /><br /> `_Ret_maybenull_z_`<br /><br /> `_Ret_null_`<br /><br /> `_Ret_notnull_`<br /><br /> `_Ret_writes_bytes_to_`<br /><br /> `_Ret_writes_bytes_maybenull_`<br /><br /> `_Ret_writes_bytes_to_maybenull_`|

## <a name="format-string-parameters"></a>Biçim dizesi parametreleri

- `_Printf_format_string_`Parametrenin bir `printf` ifadede kullanılmak üzere bir biçim dizesi olduğunu gösterir.

     **Örnek**

    ```cpp
    int MyPrintF(_Printf_format_string_ const wchar_t* format, ...)
    {
           va_list args;
           va_start(args, format);
           int ret = vwprintf(format, args);
           va_end(args);
           return ret;
    }
    ```

- `_Scanf_format_string_`Parametrenin bir `scanf` ifadede kullanılmak üzere bir biçim dizesi olduğunu gösterir.

     **Örnek**

    ```cpp
    int MyScanF(_Scanf_format_string_ const wchar_t* format, ...)
    {
           va_list args;
           va_start(args, format);
           int ret = vwscanf(format, args);
           va_end(args);
           return ret;
    }
    ```

- `_Scanf_s_format_string_`Parametrenin bir `scanf_s` ifadede kullanılmak üzere bir biçim dizesi olduğunu gösterir.

     **Örnek**

    ```cpp
    int MyScanF_s(_Scanf_s_format_string_ const wchar_t* format, ...)
    {
           va_list args;
           va_start(args, format);
           int ret = vwscanf_s(format, args);
           va_end(args);
           return ret;
    }
    ```

## <a name="other-common-annotations"></a>Diğer yaygın ek açıklamalar

**Ek açıklamalar ve açıklamalar**

- `_In_range_(low, hi)`

     `_Out_range_(low, hi)`

     `_Ret_range_(low, hi)`

     `_Deref_in_range_(low, hi)`

     `_Deref_out_range_(low, hi)`

     `_Deref_inout_range_(low, hi)`

     `_Field_range_(low, hi)`

     Parametresi, alanı veya sonucu, ile `low` `hi`arasında (dahil) aralığıdır.  Buna eşdeğer, ilgili biröndurumveyadurumsonrasıkoşullarıilebirlikteaçıklamalınesneyeuygulanır.`_Satisfies_(_Curr_ >= low && _Curr_ <= hi)`

    > [!IMPORTANT]
    > Adlar "ın" ve "Out" içerse de, `_In_` ve `_Out_` anlamları bu ek açıklamalar için geçerlidir.

- `_Pre_equal_to_(expr)`

     `_Post_equal_to_(expr)`

     Açıklamalı değer tam olarak `expr`.  Buna eşdeğer, ilgili biröndurumveyadurumsonrasıkoşullarıilebirlikteaçıklamalınesneyeuygulanır.`_Satisfies_(_Curr_ == expr)`

- `_Struct_size_bytes_(size)`

     Bir struct veya Class bildirimi için geçerlidir.  Bu türdeki geçerli bir nesnenin, tarafından `size`verilen bayt sayısıyla, belirtilen tür ile daha büyük olabileceğini gösterir.  Örneğin:

     `typedef _Struct_size_bytes_(nSize) struct MyStruct {    size_t nSize;    ... };`

     Daha sonra, türündeki `pM` `MyStruct *` bir parametrenin bayt cinsinden arabellek boyutu şu şekilde alınır:

     `min(pM->nSize, sizeof(MyStruct))`

## <a name="related-resources"></a>İlgili Kaynaklar

[Kod Analizi ekip blogu](http://go.microsoft.com/fwlink/?LinkId=251197)

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Yapıları ve Sınıfları Yorumlama](../code-quality/annotating-structs-and-classes.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [İç İşlevler](../code-quality/intrinsic-functions.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)