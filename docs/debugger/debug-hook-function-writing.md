---
title: Hata ayıklama kanca işlevi yazma | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vc.hooks
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], CRT debug support
- debug hook functions
- hooks, debug
- hooks
- debugging [CRT], debug hook functions
ms.assetid: 5510635f-cf69-4907-b72d-ae27af1f19af
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 9218c36f550c61484054d180ecb4dccb1ca53f3d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53947510"
---
# <a name="debug-hook-function-writing"></a>Hata Ayıklama Kanca İşlevi Yazma
Bu bölümde, bir dizi önceden tanımlanmış bazı noktalar normal işleme hata ayıklayıcı'nın içinde kod eklemeye izin veren yazabileceğiniz özel hata ayıklama kanca işlevleri açıklanmaktadır.  
  
## <a name="in-this-section"></a>Bu Bölümde  
 [İstemci Blok Kanca İşlevleri](../debugger/client-block-hook-functions.md)  
 Yönergeler ve bir prototip doğrulamak veya _clıent_block bloklarında depolanan verilerin içeriklerini rapor işlevleri yazmak için sağlar.  
  
 [Atama Kanca İşlevleri](../debugger/allocation-hook-functions.md)  
 Bir ayırma kanca işlevini tanımlayan, farklı kullanımları, kısıtlamalar, noktaları inceler ve bir prototip sağlar.  
  
 [Atama kancaları ve CRT bellek ayırmaları](../debugger/allocation-hooks-and-c-run-time-memory-allocations.md)  
 Kısıtlama açıkça yoksayılıyor, atama kanca işlevleri açıklar `_CRT_BLOCK` iç bellek C çalışma zamanı kitaplık işlevleri çağrıları yaptıkları engeller. Bu konuda, atama kanca değil yoksayarsanız, ayrıca sonuçları listeler `_CRT_BLOCK` bloklarla (örnekler) ve varsayılan ayırma değiştirme kanca işlevini, **CrtDefaultAllocHook**.  
  
 [Kanca İşlevlerini Raporlama](../debugger/report-hook-functions.md)  
 Anlatılmaktadır `_CrtSetReportHook`, ayırmaları belirli türlerde odaklanmak için filtre uygulamak için kullanabileceğiniz raporlar. Bu konu, bir prototip de sağlar.  
  
## <a name="related-sections"></a>İlgili Bölümler  
 [CRT Hata Ayıklama Teknikleri](../debugger/crt-debugging-techniques.md)  
 CRT hata ayıklama kitaplığı, raporlama için makroları kullanma dahil olmak üzere C çalışma zamanı kitaplığı hata ayıklama tekniklerine bağlantılarını farkları arasında `malloc` ve `_malloc_dbg`, hata ayıklama kanca işlevlerini ve CRT hata ayıklama yığın yazma.