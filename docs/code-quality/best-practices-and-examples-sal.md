---
title: En İyi Yöntemler ve Örnekler (SAL)
ms.date: 11/04/2016
ms.topic: conceptual
author: mikeblome
ms.author: mblome
manager: wpickett
ms.workload:
- multiple
ms.openlocfilehash: 478efc77bd1fb14f6241e026cfe280355a90746a
ms.sourcegitcommit: 5216c15e9f24d1d5db9ebe204ee0e7ad08705347
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/09/2019
ms.locfileid: "68919452"
---
# <a name="best-practices-and-examples-sal"></a>En İyi Yöntemler ve Örnekler (SAL)
Kaynak kodu ek açıklama dilinden (SAL) en iyi şekilde yararlanmak ve bazı yaygın sorunlardan kaçınmak için bazı yollar aşağıda verilmiştir.

## <a name="_in_"></a>\_'Ndaki\_

İşlevin öğesine yazılması gerekiyorsa, `_Inout_` `_In_`yerine kullanın. Bu özellikle, eski makrolardan SAL 'a otomatik dönüştürme gibi durumlar için geçerlidir. Sal 'tan önce birçok programcı, bu adların adı `IN` `IN_OUT`, `OUT`, veya varyantları olarak adlandırılan makrolar açıklama olarak kullanılmıştır. Bu makroları SAL 'a dönüştürmenizi öneririz; ancak, özgün prototip yazıldığı ve eski makro artık kodun ne yaptığını yansıtmadığından, bu makroları dönüştürme işlemi için de dikkatli olabilirsiniz. Genellikle doğru şekilde yerleştirildiğinden ( `OPTIONAL` Örneğin, bir virgülden oluşan yanlış tarafta) yorum makrosu hakkında özellikle dikkatli olun.

```cpp

// Incorrect
void Func1(_In_ int *p1)
{
    if (p1 == NULL)
        return;

    *p1 = 1;
}

// Correct
void Func2(_Inout_ PCHAR p1)
{
    if (p1 == NULL)
        return;

    *p1 = 1;
}
```

## <a name="_opt_"></a>\_et\_

Çağıranın null bir işaretçiye geçmesine izin `_In_` verilmiyorsa, `_In_opt_` veya `_Out_` `_Out_opt_`yerine kullanın. Bu, parametrelerini denetleyen ve olmaması gerektiğinde NULL olduğunda bir hata döndüren bir işlev için de geçerlidir. Bir işleve sahip olmak, parametresini beklenmeyen NULL için kontrol edin ve düzgün bir savunma kodlama uygulaması olsa da, parametre ek açıklamanın isteğe bağlı bir tür (`_*Xxx*_opt_`) olabilir.

```cpp

// Incorrect
void Func1(_Out_opt_ int *p1)
{
    *p = 1;
}

// Correct
void Func2(_Out_ int *p1)
{
    *p = 1;
}
```

## <a name="_pre_defensive_-and-_post_defensive_"></a>\_Ön\_ savunma\_ve gönderi\_savunlayıcı\_\_

Bir işlev güven sınırında görünürse, `_Pre_defensive_` ek açıklamayı kullanmanızı öneririz.  "Savunma" değiştiricisi belirli ek açıklamaları değiştirerek, çağrı noktasında arabirimin kesinlikle denetlenmesi gerektiğini, ancak uygulama gövdesinde yanlış parametrelerin geçirildiğine yönelik olduğunu varsaymalıdır. Bu durumda, `_In_ _Pre_defensive_` bir arayan, null geçirmeye çalışırsa bir hata vereceği için bir güven sınırında tercih edilir, ancak işlev gövdesi parametre null olabilir ve işaretçiye ilk olarak yeniden başvuru yapmaya çalışır. NULL için işaretlemek işaretlenir.  Güvenilen tarafın arayan olarak kabul edildiği ve güvenilmeyen kodun çağrılan kod olduğu geri aramalarda kullanılmak üzere ekaçıklamadakullanılabilir.`_Post_defensive_`

## <a name="_out_writes_"></a>\_Dışarı\_yazma işlemleri\_

Aşağıdaki örnek, öğesinin `_Out_writes_`ortak bir kötüye kullanımını gösterir.

```cpp

// Incorrect
void Func1(_Out_writes_(size) CHAR *pb,
    DWORD size
);
```

Ek açıklama `_Out_writes_` , bir arabelleğe sahip olduğunuz anlamına gelir. Çıkış sırasında `cb` başlatılan ilk bayt ile ayrılmış baytları vardır. Bu ek açıklama kesinlikle yanlış değildir ve ayrılan boyutu ifade etmek faydalı olur. Ancak, işlev tarafından kaç öğe başlatıldığını söylemez.

Sonraki örnekte, arabelleğin başlatılmış bölümünün tam boyutunu tam olarak belirtmek için üç doğru yol gösterilmektedir.

```cpp

// Correct
void Func1(_Out_writes_to_(size, *pCount) CHAR *pb,
    DWORD size,
    PDWORD pCount
);

void Func2(_Out_writes_all_(size) CHAR *pb,
    DWORD size
);

void Func3(_Out_writes_(size) PSTR pb,
    DWORD size
);
```

## <a name="_out_-pstr"></a>\_Çıkış\_ PSTR

Kullanımı `_Out_ PSTR` neredeyse her zaman yanlıştır. Bu, bir karakter arabelleğini işaret eden bir çıkış parametresine sahip olarak yorumlanır ve NULL olarak sonlandırılır.

```cpp

// Incorrect
void Func1(_Out_ PSTR pFileName, size_t n);

// Correct
void Func2(_Out_writes_(n) PSTR wszFileName, size_t n);
```

Benzer `_In_ PCSTR` bir ek açıklama yaygın ve kullanışlı bir seçenektir. Önkoşul `_In_` , null ile sonlandırılmış bir dizenin tanınmasını sağladığından, null sonlandırmasına sahip bir giriş dizesini işaret eder.

## <a name="_in_-wchar-p"></a>\_Wchar * p 'de\_

`_In_ WCHAR* p`bir karakteri işaret eden bir giriş işaretçisi `p` olduğunu söyler. Ancak çoğu durumda bu, amaçlanan belirtim olabilir. Bunun yerine, büyük olasılıkla amaçlanan, NULL ile sonlandırılmış bir dizinin belirtimidir; Bunu yapmak için kullanın `_In_ PWSTR`.

```cpp

// Incorrect
void Func1(_In_ WCHAR* wszFileName);

// Correct
void Func2(_In_ PWSTR wszFileName);
```

NULL sonlandırmanın doğru belirtimi eksik. Aşağıdaki örnekte gösterildiği `STR` gibi, türü değiştirmek için uygun sürümü kullanın.

```cpp

// Incorrect
BOOL StrEquals1(_In_ PCHAR p1, _In_ PCHAR p2)
{
    return strcmp(p1, p2) == 0;
}

// Correct
BOOL StrEquals2(_In_ PSTR p1, _In_ PSTR p2)
{
    return strcmp(p1, p2) == 0;
}
```

## <a name="_out_range_"></a>\_Out\_aralığı\_

Parametresi bir işaretçisiyse ve işaretçi tarafından işaret edilen öğenin değer aralığını ifade etmek istiyorsanız `_Deref_out_range_` `_Out_range_`yerine kullanın. Aşağıdaki örnekte, * Pcbdoldurulmuş aralığı, Pcbdoldurulmuş değil ifade edilir.

```cpp

// Incorrect
void Func1(
    _Out_writes_bytes_to_(cbSize, *pcbFilled) BYTE *pb,
    DWORD cbSize,
    _Out_range_(0, cbSize) DWORD *pcbFilled
);

// Correct
void Func2(
    _Out_writes_bytes_to_(cbSize, *pcbFilled) BYTE *pb,
    DWORD cbSize,
    _Deref_out_range_(0, cbSize) _Out_ DWORD *pcbFilled
);
```

`_Deref_out_range_(0, cbSize)`, ' den `_Out_writes_to_(cbSize,*pcbFilled)`çıkarsanabileceğinden bazı araçlar için kesinlikle gerekli değildir, ancak bu, tamamlanma açısından burada gösterilmiştir.

## <a name="wrong-context-in-_when_"></a>\_Sırasında yanlış bağlam\_

Diğer bir yaygın hata, ön koşullar için durum sonrası değerlendirme kullanmaktır. Aşağıdaki örnekte, `_Requires_lock_held_` önkoşuludur.

```cpp

// Incorrect
_When_(return == 0, _Requires_lock_held_(p->cs))
int Func1(_In_ MyData *p, int flag);

// Correct
_When_(flag == 0, _Requires_lock_held_(p->cs))
int Func2(_In_ MyData *p, int flag);
```

İfade `result` , ön durum ' da kullanılamayan bir durum sonrası değeri ifade eder.

## <a name="true-in-_success_"></a>Başarı durumunda \_doğru\_

Dönüş değeri sıfır olmadığında işlev başarılı olursa, `return != 0` `return == TRUE`yerine başarı koşulu olarak kullanın. Sıfır olmayan değerin, derleyicinin sağladığı `TRUE`gerçek değere eşdeğer olması gerekmez. Parametresi `_Success_` bir ifadedir ve aşağıdaki ifadeler eşdeğer olarak değerlendirilir: `return != 0`, `return != false` `return != FALSE`,, ve `return` parametresiz veya karşılaştırmalar yok.

```cpp

// Incorrect
_Success_(return == TRUE, _Acquires_lock_(*lpCriticalSection))
BOOL WINAPI TryEnterCriticalSection(
  _Inout_ LPCRITICAL_SECTION lpCriticalSection
);

// Correct
_Success_(return != 0, _Acquires_lock_(*lpCriticalSection))
BOOL WINAPI TryEnterCriticalSection(
  _Inout_ LPCRITICAL_SECTION lpCriticalSection
);
```

## <a name="reference-variable"></a>Başvuru değişkeni

Bir başvuru değişkeni için, Sal 'un önceki sürümü, kapsanan işaretçiyi ek açıklama hedefi olarak kullandı ve bir başvuru değişkenine eklenmiş olan ek `__deref` açıklamaların eklenmesini gerektiriyordu. Bu sürüm nesnenin kendisini kullanır ve ek `_Deref_`gerektirmez.

```cpp

// Incorrect
void Func1(
    _Out_writes_bytes_all_(cbSize) BYTE *pb,
    _Deref_ _Out_range_(0, 2) _Out_ DWORD &cbSize
);

// Correct
void Func2(
    _Out_writes_bytes_all_(cbSize) BYTE *pb,
    _Out_range_(0, 2) _Out_ DWORD &cbSize
);
```

## <a name="annotations-on-return-values"></a>Dönüş değerlerinde ek açıklamalar

Aşağıdaki örnek, dönüş değeri ek açıklamalarıyla ilgili yaygın bir sorunu gösterir.

```cpp

// Incorrect
_Out_opt_ void *MightReturnNullPtr1();

// Correct
_Ret_maybenull_ void *MightReturnNullPtr2();
```

Bu örnekte, `_Out_opt_` önkoşulun bir parçası olarak işaretçinin null olabileceğini belirtir. Ancak, Önkoşullar dönüş değerine uygulanamaz. Bu durumda, doğru ek açıklama olur `_Ret_maybenull_`.

## <a name="see-also"></a>Ayrıca bkz.

[Sal ekC++ açıklamalarını](../code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects.md)[, Sal](../code-quality/annotating-function-parameters-and-return-values.md)


açıklama ekleme işlev parametrelerini ve dönüş değerleri[işlev davranışına](../code-quality/annotating-function-behavior.md) [](../code-quality/understanding-sal.md)
Açıklamaolarakanlamakiçinkullanma [Yapı ve sınıflara](../code-quality/annotating-structs-and-classes.md)
açıklama ekleme, bir ek açıklamanın[iç işlevleri](../code-quality/intrinsic-functions.md) [ne zaman ve nerede uygulanacağını](../code-quality/specifying-when-and-where-an-annotation-applies.md)
belirten[kilitleme davranışına](../code-quality/annotating-locking-behavior.md)
açıklama ekleme