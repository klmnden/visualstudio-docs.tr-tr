---
title: Hata ayıklama yığın ayırma işlevleri sürümleri | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.crt
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- _CRTDBG_MAP_ALLOC macro
- debugging [CRT], heap allocation functions
- debugging memory leaks, CRT debug library functions
- malloc function
- memory leaks, CRT debug library functions
- heap allocation, debug
- _malloc_dbg function
ms.assetid: 91748bdc-f4cd-4d8b-ab98-0493dab7ed0d
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f7df6a0ebc161d794a39e9e16b3b73abe42c6ec7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53862415"
---
# <a name="debug-versions-of-heap-allocation-functions"></a>Öbek Atama İşlevleri Hata Ayıklama Sürümleri
C çalışma zamanı kitaplığı, özel öbek atama işlevleri hata ayıklama sürümlerini içerir. Bu işlevler sürümle aynı ada sahip sürümleri _dbg eklenir. Bu konuda bir CRT işlevini sürümü _dbg sürümü arasındaki farkları açıklar kullanarak `malloc` ve `_malloc_dbg` örnekler.  
  
 Zaman [_DEBUG](/cpp/c-runtime-library/debug) olan tanımlanan, CRT tüm eşler [malloc](/cpp/c-runtime-library/reference/malloc) çağrılar [_malloc_dbg](/cpp/c-runtime-library/reference/malloc-dbg). Bu nedenle, kodu kullanarak yeniden gerekmez `_malloc_dbg` yerine `malloc` hata ayıklama sırasında avantajlardan yararlanabilir.  
  
 Çağırmak isteyebilirsiniz `_malloc_dbg` açıkça ancak. Çağırma `_malloc_dbg` açıkça bazı avantajları eklemiştir:  
  
- İzleme `_CLIENT_BLOCK` ayırmaları yazın.  
  
- Ayırma isteği gerçekleştiği kaynak dosya ve satır numarası depolama.  
  
  Dönüştürmek istemiyorsanız, `malloc` çağrılar `_malloc_dbg`, tanımlayarak, kaynak dosya bilgileri edinebilirsiniz [_CRTDBG_MAP_ALLOC](/cpp/c-runtime-library/crtdbg-map-alloc), tüm çağrıları doğrudan önişlemci harita neden `malloc` için`_malloc_dbg` çevresinde bir sarmalayıcı güvenmek yerine `malloc`.  
  
  İstemci bloklarında ayırmaları ayrı türlerini izlemek için çağırmalıdır `_malloc_dbg` doğrudan ve `blockType` parametresi `_CLIENT_BLOCK`.  
  
  _DEBUG tanımlı değil, çağrılar `malloc` değil etkilenir, çağrılar `_malloc_dbg` için çözümlendiği `malloc`, tanımını [_CRTDBG_MAP_ALLOC](/cpp/c-runtime-library/crtdbg-map-alloc) göz ardı edilir ve kaynak dosya bilgileri saklamanıza ayırma isteği belirtilmedi. Çünkü `malloc` blok türü parametresi yok, için istekleri `_CLIENT_BLOCK` türler standart ayırmaları kabul edilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [CRT Hata Ayıklama Teknikleri](../debugger/crt-debugging-techniques.md)