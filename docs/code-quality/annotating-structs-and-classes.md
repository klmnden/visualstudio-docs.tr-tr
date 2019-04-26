---
title: Yapıları ve Sınıfları Yorumlama
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- _Field_size_bytes_part_
- _Field_size_bytes_full_opt_
- _Field_size_bytes_
- _Field_size_opt_
- _Field_size_part_
- _Field_size_bytes_part_opt_
- _Field_range_
- _Field_size_part_opt_
- _Field_size_
- _Field_size_bytes_opt_
- _Struct_size_bytes_
- _Field_size_bytes_full_
- _Field_size_full_
- _Field_size_full_opt_
- _Field_z_
ms.assetid: b8278a4a-c86e-4845-aa2a-70da21a1dd52
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: fa459e3461ef5e58eb1e5b0c675c7e1b408d6f88
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62571426"
---
# <a name="annotating-structs-and-classes"></a>Yapıları ve Sınıfları Yorumlama
Yapı ve sınıf üyeleri okuduğunuzda gibi davranan ek açıklamalar kullanarak açıklama ekleyebilirsiniz; herhangi bir işlev çağrısı veya bir parametre veya bir sonuç değeri kapsayan yapısı gerektirir. işlev girişi/çıkışı en doğru olduğu varsayılmıştır.

## <a name="struct-and-class-annotations"></a>Yapı ve sınıf ek açıklamaları

- `_Field_range_(low, high)`

     Aralık (dahil) gelen alanın bulunduğu `low` için `high`.  Eşdeğer `_Satisfies_(_Curr_ >= low && _Curr_ <= high)` uygun önceki veya sonraki koşullarını kullanarak ek açıklamalı nesneye uygulanan.

- `_Field_size_(size)`, `_Field_size_opt_(size)`, `_Field_size_bytes_(size)`, `_Field_size_bytes_opt_(size)`

     Öğeleri (veya bayt) belirtilen bir yazılabilir boyut sahip bir alan `size`.

- `_Field_size_part_(size, count)`, `_Field_size_part_opt_(size, count)`,         `_Field_size_bytes_part_(size, count)`, `_Field_size_bytes_part_opt_(size, count)`

     Öğeleri (veya bayt) belirtilen bir yazılabilir boyut sahip bir alan `size`ve `count` okunabilir bu öğelerin (bayt).

- `_Field_size_full_(size)`, `_Field_size_full_opt_(size)`, `_Field_size_bytes_full_(size)`, `_Field_size_bytes_full_opt_(size)`

     Readable ve writable öğeleri (veya boyutunu bayt) tarafından belirtilen sahip bir alan `size`.

- `_Field_z_`

     Null ile sonlandırılmış bir dize sahip bir alan.

- `_Struct_size_bytes_(size)`

     Yapı ya da sınıf bildirimi için geçerlidir.  Geçerli bir nesne türü tarafından belirtilen bayt sayısı ile bildirilen türünden daha büyük olabileceğini gösterir `size`.  Örneğin:

    ```cpp

    typedef _Struct_size_bytes_(nSize)
    struct MyStruct {
        size_t nSize;
        ...
    };

    ```

     Arabellek boyutu parametresinin bayt `pM` türü `MyStruct *` olmasını alınır:

    ```cpp
    min(pM->nSize, sizeof(MyStruct))
    ```

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [İç İşlevler](../code-quality/intrinsic-functions.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)