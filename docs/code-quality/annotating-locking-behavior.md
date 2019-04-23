---
title: Kilitlenme Davranışını Yorumlama
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _Releases_nonreentrant_lock_
- _Lock_kind_mutex_
- _Lock_kind_critical_section_
- _Acquires_lock_
- _Releases_lock_
- _Has_lock_kind_
- _Releases_exclusive_lock_
- _Post_same_lock_
- _Requires_exclusive_lock_held_
- _Requires_shared_lock_held_
- _Lock_kind_semaphore_
- _Requires_lock_held_
- _Acquires_exclusive_lock_
- _Create_lock_level_
- _Acquires_nonreentrant_lock_
- _Releases_shared_lock_
- _Has_lock_level_
- _Lock_kind_spin_lock_
- _Requires_lock_not_held_
- _Acquires_shared_lock_
- _Requires_no_locks_held_
- _Lock_level_order_
- _Lock_kind_event_
ms.assetid: 07769c25-9b97-4ab7-b175-d1c450308d7a
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 6590a07ec7fc67bef5f1b1cfd96e80105fa325ce
ms.sourcegitcommit: 1fc6ee928733e61a1f42782f832ead9f7946d00c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/22/2019
ms.locfileid: "60053735"
---
# <a name="annotating-locking-behavior"></a>Kilitlenme Davranışını Yorumlama
Çoklu iş parçacığı kullanan programınızda eşzamanlılık hataları önlemek için her zaman uygun kilitleme uzmanlık alanı izleyin ve SAL ek açıklamalarını kullanma.

 Eşzamanlılık yeniden, tanılama ve belirleyici olmadığından hata ayıklama öğesinin zor hatalardır. İş parçacığı Interleaving hakkında mantık en iyi zordur ve fazla sayıda iş parçacığı olan kod gövdesinin tasarlarken pratik hale gelir. Bu nedenle, bir kilitleme disiplini, çok iş parçacıklı programlarda izleyin iyi bir uygulamadır. Örneğin, birden çok kilit alınırken kilitlenmeleri önlemek yardımcı olurken bir kilit sırası obeying ve paylaşılan bir kaynağa erişmeden önce doğru guarding kilit alınırken yarış durumlarını engellemeye yardımcı olur.

 Ne yazık ki görünüşte basit kilitleme kuralları uygulamada izleyin yayımladım zor olabilir. Bir temel günümüzün programlama dilleri ve derleyiciler bunlar doğrudan belirtimi ve eşzamanlılık gereksinimleri analizini desteklemiyor sınırlamasıdır. Kilitleri nasıl kullandıkları hakkında kendi amaçları ifade etmek için resmi olmayan kod açıklamaları kullanan programcılar gerekir.

 Eşzamanlılık SAL ek açıklamaları, sorumluluk, veri guardianship, kilit sırası hiyerarşi ve diğer beklenen kilitlenme davranışını kilitleme Kilitleme yan etkileri belirlemenize yardımcı olmak için tasarlanmıştır. Örtük kuralları açık hale getirerek SAL eşzamanlılık ek açıklamaları, kodunuzu kilitleme kuralları nasıl kullandığını belge tutarlı bir yol sağlar. Eşzamanlılık ek açıklamaları da yarış durumlarını, kilitlenmeleri, eşleşmeyen eşitleme işlemleri ve diğer hafif eşzamanlılık hataları bulmak için kod çözümleme araçları yeteneğini geliştirin.

## <a name="general-guidelines"></a>Genel Yönergeler
 Ek açıklamalar kullanarak uygulamaları (çağrılanlar) ve istemciler (arayanlar) arasındaki işlev tanımları tarafından kapsanan sözleşmeleri durum ve analiz express okuduğunuzda ve daha ileri düzeyde programın diğer özelliklerini geliştirmek.

 SAL kilitleme temelleri birçok farklı türde destekler; Örneğin, kritik bölüm, mutex'leri, döndürme kilit ve diğer kaynak nesneleri. Birçok eşzamanlılık ek açıklamaları, parametre olarak bir kilit ifadesi alır. Kural gereği, kilit temel kilit nesnenin yol ifadesi tarafından belirtilir.

 Aklınızda tutmanız gereken bazı iş parçacığı sahipliği kuralları:

- Döndürme kilitlerini Temizle iş parçacığı sahipliğine uncounted kilitleri.

- NET iş parçacığı sahipliğine kilitleri Mutex'leri ve kritik bölüm sayılır.

- Semafor ve olayları Temizle iş parçacığı sahipliği olmayan kilitleri sayılır.

## <a name="locking-annotations"></a>Kilitleme ek açıklamaları
 Aşağıdaki tabloda, kilitleme ek açıklamalar listelenmektedir.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Acquires_exclusive_lock_(expr)`|Bir işlev açıklama ekler ve gönderisinde durumu işlev bir özel bir kilit tarafından adlandırılan kilit nesnesi sayısı artırır olduğunu gösteren `expr`.|
|`_Acquires_lock_(expr)`|Bir işlev açıklama ekler ve gönderisinde durumu işlevi bir kilit nesnenin tarafından adlandırılan kilit sayacını artırır olduğunu gösteren `expr`.|
|`_Acquires_nonreentrant_lock_(expr)`|Tarafından adlandırılan kilit `expr` alınır.  Kilidi açık tutulduğu zaten varsa, bir hata bildirilir.|
|`_Acquires_shared_lock_(expr)`|Bir işlev açıklama ekler ve gönderisinde durumu işlevi bir tarafından adlandırılan kilit nesnesinin paylaşılan kilit sayacını artırır olduğunu gösteren `expr`.|
|`_Create_lock_level_(name)`|Simgenin bildiren bir deyim `name` ek açıklamalarda kullanılabilir kilit düzeyi olmasını `_Has_Lock_level_` ve `_Lock_level_order_`.|
|`_Has_lock_kind_(kind)`|Bir kaynak nesnesinin türü bilgileri geliştirmek için herhangi bir nesne açıklama ekler. Bazen, ortak tür farklı türde kaynakların için kullanılır ve aşırı yüklenmiş türü anlam gereksinimleri çeşitli kaynaklar arasında ayrım yapmak yeterli değil. İşte bir listesi, önceden tanımlanmış `kind` parametreleri:<br /><br /> `_Lock_kind_mutex_`<br /> Kilit mutex'leri için tür kimliği.<br /><br /> `_Lock_kind_event_`<br /> Kilit olaylar için tür kimliği.<br /><br /> `_Lock_kind_semaphore_`<br /> Kilit semaforları için tür kimliği.<br /><br /> `_Lock_kind_spin_lock_`<br /> Kilit döndürme kilide tür kimliği.<br /><br /> `_Lock_kind_critical_section_`<br /> Kritik bölümler için kilit tür kimliği.|
|`_Has_lock_level_(name)`|Nesnesi kilitlenemedi açıklama ekler ve kilit düzeyi sunar `name`.|
|`_Lock_level_order_(name1, name2)`|Arasında sıralama kilit sağlayan bir ifade `name1` ve `name2`.|
|`_Post_same_lock_(expr1, expr2)`|Bir işlev açıklama ekler ve gönderisinde iki kilitler durumunu gösteren `expr1` ve `expr2`, aynı nesnesi kilitlenemedi oldukları gibi değerlendirilir.|
|`_Releases_exclusive_lock_(expr)`|Bir işlev açıklama ekler ve postasında tek tarafından adlandırılan kilit nesnenin özel bir kilit sayısı işlevi azaltır durumunu gösteren `expr`.|
|`_Releases_lock_(expr)`|Bir işlev açıklama ekler ve postasında tek kilit sayacını tarafından adlandırılan kilit nesnenin işlevi azaltır durumunu gösteren `expr`.|
|`_Releases_nonreentrant_lock_(expr)`|Tarafından adlandırılan kilit `expr` serbest bırakılır. Kilit şu anda tutulmadı varsa bir hata bildirilir.|
|`_Releases_shared_lock_(expr)`|Bir işlev açıklama ekler ve postasında tek tarafından adlandırılan kilit nesnesinin paylaşılan kilit sayacını işlevi azaltır durumunu gösteren `expr`.|
|`_Requires_lock_held_(expr)`|Bir işlev açıklama ekler ve öncesi içinde kilit sayacını tarafından adlandırılan nesnenin durumunu gösteren `expr` en az biri.|
|`_Requires_lock_not_held_(expr)`|Bir işlev açıklama ekler ve öncesi içinde kilit sayacını tarafından adlandırılan nesnenin durumunu gösteren `expr` sıfırdır.|
|`_Requires_no_locks_held_`|Bir işlev açıklama ekler ve denetleyicisi için bilinen tüm kilitleri kilit sayısı sıfır olduğunu gösterir.|
|`_Requires_shared_lock_held_(expr)`|Bir işlev açıklama ekler ve öncesi içinde paylaşılan kilit sayacını tarafından adlandırılan nesnenin durumunu gösteren `expr` en az biri.|
|`_Requires_exclusive_lock_held_(expr)`|Bir işlev açıklama ekler ve öncesi içinde özel bir kilit sayısı tarafından adlandırılan nesnenin durumunu gösteren `expr` en az biri.|

## <a name="sal-intrinsics-for-unexposed-locking-objects"></a>Gösterilmeyen kilitleme nesneler için SAL iç bilgileri
 Belirli nesneleri Kilitle ilişkili kilitleme işlevleri uygulaması tarafından sunulmaz.  Aşağıdaki tabloda bu gösterilmeyen kilit nesneler üzerinde çalışan işlevler ek açıklamalar sağlayan SAL iç değişkenleri listeler.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Global_cancel_spin_lock_`|İptal döndürme kilit açıklar.|
|`_Global_critical_region_`|Kritik bölge açıklar.|
|`_Global_interlock_`|Birbirine kenetlenmiş işlemler açıklanmaktadır.|
|`_Global_priority_region_`|Öncelik bölge açıklar.|

## <a name="shared-data-access-annotations"></a>Paylaşılan veri erişim ek açıklamaları
 Aşağıdaki tabloda, paylaşılan veri erişimi için ek açıklamalar listelenmektedir.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Guarded_by_(expr)`|Bir değişken açıklama ekler ve her değişkenin eriştiğinden, gösterir tarafından adlandırılan kilit nesnenin kilit sayacını `expr` en az biri.|
|`_Interlocked_`|Bir değişken açıklama ekler ve eşdeğerdir `_Guarded_by_(_Global_interlock_)`.|
|`_Interlocked_operand_`|Çeşitli birbirine kenetlenmiş işlevlerden biri hedef işleneni ek açıklamalı işlevi parametredir.  Bu işlenenlerin özgü ek özellikleri olmalıdır.|
|`_Write_guarded_by_(expr)`|Bir değişken açıklama ekler ve her değişkenin değiştirilmişse, tarafından adlandırılan kilit nesnenin kilit sayacını gösterir `expr` en az biri.|

## <a name="smart-lock-and-raii-annotations"></a>Akıllı kilitleme ve RAII ek açıklamaları
 Akıllı kilitlere, genellikle yerel kilitleri kaydırma ve kendi ömürlerine yönetin. Akıllı kilit ve RAII desenleri desteğiyle kodlama ile kullanılabilecek ek açıklamaları aşağıdaki tabloda `move` semantiği.

|Ek Açıklama|Açıklama|
|----------------|-----------------|
|`_Analysis_assume_smart_lock_acquired_`|Akıllı kilit alınmış varsaymak Çözümleyicisi söyler. Bu ek açıklama, parametre olarak başvuru kilit türü bekleniyor.|
|`_Analysis_assume_smart_lock_released_`|Akıllı kilit serbest bırakıldığını varsaymak Çözümleyicisi söyler. Bu ek açıklama, parametre olarak başvuru kilit türü bekleniyor.|
|`_Moves_lock_(target, source)`|Açıklar `move constructor` kilitleme durumu aktarır işlemi `source` nesnesini `target`. `target` Herhangi önce olduğundan kaybolur ve değiştirilen durum için yeni oluşturulan bir nesne olarak kabul edilir `source` durumu. `source` Olduğunu da hiçbir kilidi sayıları ve diğer ad kullanımı hedef ancak işaret diğer adlar ile temiz bir duruma Sıfırla değişmeden kalır.|
|`_Replaces_lock_(target, source)`|Açıklar `move assignment operator` semantiği burada hedef kilidi serbest kaynak durumu aktarmadan önce. Bu bir birleşimi olarak görülebilir `_Moves_lock_(target, source)` önünde bir `_Releases_lock_(target)`.|
|`_Swaps_locks_(left, right)`|Standart açıklar `swap` nesneleri varsayan davranışı `left` ve `right` durumlarına exchange. Değiştirilen durum sayısı ve diğer ad kullanımı hedef kilit, varsa içerir. İşaret eden diğer adlar `left` ve `right` nesneleri değişmeden kalır.|
|`_Detaches_lock_(detached, lock)`|Bir kilit sarmalayıcı türü dağılımı ile onun içerdiği kaynak sağlayan bir senaryo açıklanır. Bu nasıl benzer `std::unique_ptr` kendi iç işaretçi ile çalışır: işaretçisini ayıklayın ve akıllı işaretçi kapsayıcısı temiz bir durumda bırakır programcılar sağlar. Tarafından desteklenen benzer bir mantık `std::unique_lock` ve özel bir kilit sarmalayıcılar uygulanabilir. Durumuna (kilit sayısı ve diğer ad kullanımı hedef, eğer varsa), ayrılmış kilidi tutan sarmalayıcı kendi diğer adlar korurken sıfır kilit sayacını ve hiçbir diğer ad kullanımı hedef içeren sıfırlanarak sırada. Kilit sayıları (serbest bırakma ve alma) hiçbir işlem yok. Bu ek açıklama tam olarak davranır `_Moves_lock_` ayrılmış bağımsız değişkeni olmalıdır dışında `return` yerine `this`.|

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Yapıları ve Sınıfları Yorumlama](../code-quality/annotating-structs-and-classes.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [İç İşlevler](../code-quality/intrinsic-functions.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)
- [Kod Analizi ekip blogu](http://go.microsoft.com/fwlink/p/?LinkId=251197)