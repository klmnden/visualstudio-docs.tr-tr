---
title: Atama kanca işlevleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- memory allocation, logging allocation information
- insufficient memory
- debugging [C++], hook functions
- _CrtSetAllocHook function
- allocation hooks
- hooks, allocation
ms.assetid: 6bfbdb65-8cb1-4c21-8c45-7194a2b77c1e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 406647ae086285df8dfdfc00daf4b62be66e74a2
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63402682"
---
# <a name="allocation-hook-functions"></a>Atama Kanca İşlevleri
Kullanarak yüklü bir ayırma kanca işlevini [_CrtSetAllocHook](/cpp/c-runtime-library/reference/crtsetallochook), bellek tahsis, bırakılan veya serbest her zaman çağrılır. Bu tür bir kanca birçok farklı amaçlar için kullanabilirsiniz. Daha sonra çözümlemek için ayırma bilgileri günlüğe kaydetmek veya nasıl bir uygulama yetersiz bellek durumları gibi ayırma desenlerini incelenmesi işleme test kullanın.

> [!NOTE]
> Kısıtlama C çalışma zamanı kitaplık işlevleri açıklandığı bir ayırma kanca işlevini kullanma hakkında bilmeniz [ayırma kancaları ve C çalışma zamanı bellek ayırmaları](../debugger/allocation-hooks-and-c-run-time-memory-allocations.md).

 Bir ayırma kanca işlevini, aşağıdaki örnekte olduğu gibi bir prototipe sahip olmalıdır:

```cpp
int YourAllocHook(int nAllocType, void *pvData,
        size_t nSize, int nBlockUse, long lRequest,
        const unsigned char * szFileName, int nLine )
```

 Geçirdiğiniz işaretçiyi [_CrtSetAllocHook](/cpp/c-runtime-library/reference/crtsetallochook) türünde **_CRT_ALLOC_HOOK**CRTDBG içinde tanımlanan gibi. Y:

```cpp
typedef int (__cdecl * _CRT_ALLOC_HOOK)
    (int, void *, size_t, int, long, const unsigned char *, int);
```

 Çalışma zamanı kitaplığı, kanca çağırdığında *nAllocType* bağımsız değişkeni hangi ayırma gösterir işlemdir hakkında yapılacak (**_HOOK_ALLOC**, **_HOOK_REALLOC**, veya **_HOOK_FREE**). Ücretsiz veya bir reallocation `pvData` kullanıcı makaleyi serbest bırakılacak bloğunun bir işaretçiye sahiptir. Ancak bir ayırma için ayırma oluştuğundan henüz Bu işaretçi null. Kalan bağımsız değişkenleri ayırmanın boyutu söz konusu, blok türü ve dosya adı için bir işaretçi ile ilişkili ardışık istek numarasını içerir. Varsa, bağımsız değişkenler de ayırma yapıldığı satır numarasını içerir. Hangi analizi kanca işlevini gerçekleştirir ve diğer görevler, yazar istediği sonra ya da döndürmelidir **TRUE**, ayırma işlemi devam edebilir, gösteren veya **FALSE**gösteren, işlem başarısız olmalıdır. Bu tür bir basit kanca şimdiye ayrılan bellek miktarını denetleyin ve dönüş **FALSE** bu kadar küçük bir sınır aşılırsa. Uygulama türü yalnızca kullanılabilir bellek düşük olduğunda, normalde oluşacak ayırma hatalarının ardından deneyimleyeceği. Daha karmaşık kancaları ayırma desenlerini izlemek, bellek kullanımını analiz etme veya özel durumlar oluştuğunda bildirin.

## <a name="see-also"></a>Ayrıca Bkz.

- [Atama Kancaları ve C Çalışma Zamanı Bellek Ayırmaları](../debugger/allocation-hooks-and-c-run-time-memory-allocations.md)
- [Hata Ayıklama Kanca İşlevi Yazma](../debugger/debug-hook-function-writing.md)