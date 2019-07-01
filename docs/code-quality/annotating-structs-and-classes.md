---
title: Yapıları ve Sınıfları Yorumlama
ms.date: 06/28/2019
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
ms.openlocfilehash: 35be465064c9524eb0e1339794b6a19b7a595da1
ms.sourcegitcommit: d2b234e0a4a875c3cba09321cdf246842670d872
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2019
ms.locfileid: "67493631"
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

## <a name="example"></a>Örnek

```cpp
#include <sal.h>
// For FIELD_OFFSET macro
#include <windows.h>

// This _Struct_size_bytes_ is equivalent to what below _Field_size_ means.
_Struct_size_bytes_(FIELD_OFFSET(MyBuffer, buffer) + bufferSize * sizeof(int))
struct MyBuffer
{
    static int MaxBufferSize;
    
    _Field_z_
    const char* name;
    
    int firstField;

    // ... other fields

    _Field_range_(1, MaxBufferSize)
    int bufferSize;
    _Field_size_(bufferSize)        // Prefered way - easier to read and maintain.
    int buffer[0];
};
```

Bu örnek için Notlar:

- `_Field_z_` eşdeğerdir `_Null_terminated_`.  `_Field_z_` için ad alanı ad alanı null ile sonlandırılmış bir dize belirtir.
- `_Field_range_` için `bufferSize` belirten değeri `bufferSize` içinde 1 olmalıdır ve `MaxBufferSize` (her ikisi de dahil).
- Son sonuçları `_Struct_size_bytes_` ve `_Field_size_` ek açıklamaları eşdeğerdir. Yapılar veya benzer bir düzen sahip sınıflar için `_Field_size_` daha az başvurular ve eşdeğer hesaplamalar olduğundan okunması ve düzenlenmesi, daha kolay olan `_Struct_size_bytes_` ek açıklama. `_Field_size_` bayt boyutu dönüştürme gerektirmez. Bayt boyutu tek seçenek, örneğin, bir void işaretçisine alan için ise `_Field_size_bytes_` kullanılabilir. Her iki `_Struct_size_bytes_` ve `_Field_size_` var, her ikisi de araçlar kullanılabilir olur. Bu aracın en fazla iki ek açıklamalar katılmıyorum durumunda ne yapacaklarını nedir?

## <a name="see-also"></a>Ayrıca Bkz.

- [C/C++ Kod Hatalarını Azaltmak için SAL Ek Açıklamalarını Kullanma](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)
- [SAL'yi Anlama](../code-quality/understanding-sal.md)
- [İşlev Parametrelerini ve Dönüş Değerlerini Açıklama](../code-quality/annotating-function-parameters-and-return-values.md)
- [İşlev Davranışını Yorumlama](../code-quality/annotating-function-behavior.md)
- [Kilitlenme Davranışını Yorumlama](../code-quality/annotating-locking-behavior.md)
- [Açıklamanın Ne Zaman ve Nereye Uygulanacağını Belirtme](../code-quality/specifying-when-and-where-an-annotation-applies.md)
- [İç İşlevler](../code-quality/intrinsic-functions.md)
- [En İyi Yöntemler ve Örnekler](../code-quality/best-practices-and-examples-sal.md)