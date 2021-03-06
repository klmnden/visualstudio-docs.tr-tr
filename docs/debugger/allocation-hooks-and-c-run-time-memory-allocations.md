---
title: Atama kancaları ve C çalışma zamanı bellek ayırmaları | Microsoft Docs
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
- debugging [C++], hook functions
- memory allocation, troubleshooting allocation hooks
- allocation hooks
- hooks, allocation
ms.assetid: cc34ee96-3d91-41bd-a019-aa3759139e7e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 1840f6f5650b3491cf7898c1d8d6a6fcae19f906
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62564980"
---
# <a name="allocation-hooks-and-c-run-time-memory-allocations"></a>Atama Kancaları ve C Çalışma Zamanı Bellek Ayırmaları
Atama kanca işlevleri çok önemli bir kısıtlama bunlar açıkça yoksayması gereken olduğu `_CRT_BLOCK` engeller. Bu, iç bellek C çalışma zamanı kitaplık işlevleri yapılan her çağrı yaparsanız C çalışma zamanı kitaplığı işlevleri tarafından dahili olarak yapılan bellek ayırmaları taşlarıdır. Yoksayabilirsiniz `_CRT_BLOCK` , ayrılan başına aşağıdaki kodu ekleyerek blok kanca işlevini:

```cpp
if ( nBlockUse == _CRT_BLOCK )
    return( TRUE );
```

Varsa, atama kanca yoksaymaz `_CRT_BLOCK` , içindeki kanca adlı tüm C çalışma zamanı kitaplığı işlevi sonsuz bir döngünün program yakalayabilir sonra engeller. Örneğin, `printf` iç ayırma sağlar. Kanca kodunuzu çağırırsa `printf`, ortaya çıkan ayırma, kanca yeniden çağrılacak olan çağıracak neden olmaz **printf** yeniden, vb. kadar yığın taşıyor. Rapora ihtiyacınız varsa `_CRT_BLOCK` ayırma işlemleri, bu kısıtlama aşmak için bir yol olan biçimlendirmek için C çalışma zamanı işlevleri yerine Windows API işlevlerini kullanın ve çıkacağını. Windows API'ları C çalışma zamanı kitaplığı yığın kullanmayın çünkü, atama kanca sonsuz bir döngüde tuzak olmaz.

Çalışma zamanı kitaplığı kaynak dosyaları incelerseniz göreceğiniz işlevi, varsayılan ayırma kanca olduğunu **CrtDefaultAllocHook** (yalnızca döndüren **TRUE**), kendine ait, ayrı bir dosyada bulunan DBGHOOK. C. Bile, uygulamanızın önce yürütülen çalışma zamanı başlatma kodu tarafından yapılan ayırmaları çağrılmasına, atama kanca isteyip istemediğinizi **ana** işlevi, bir kendi yerine bu varsayılan işlev değiştirebilirsiniz kullanarak [_CrtSetAllocHook](/cpp/c-runtime-library/reference/crtsetallochook).

## <a name="see-also"></a>Ayrıca Bkz.
- [Hata Ayıklama Kanca İşlevi Yazma](../debugger/debug-hook-function-writing.md)
