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
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 82145d39adc519bfd1324cc36805cea7b97b1664
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62563379"
---
# <a name="debug-hook-function-writing"></a>Hata Ayıklama Kanca İşlevi Yazma
Bu bölümde, bir dizi önceden tanımlanmış bazı noktalar normal işleme hata ayıklayıcı'nın içinde kod eklemeye izin veren yazabileceğiniz özel hata ayıklama kanca işlevleri açıklanmaktadır.

## <a name="in-this-section"></a>Bu Bölümde
 [İstemci blok kanca işlevleri](../debugger/client-block-hook-functions.md) sağlayan yönergeler ve bir prototip doğrulamak veya _clıent_block bloklarında depolanan verilerin içeriklerini raporun işlevler yazma için.

 [Atama kanca işlevleri](../debugger/allocation-hook-functions.md) bir ayırma kanca işlevini tanımlayan, farklı kullanımları inceler, kısıtlamaları noktaları ve bir prototip sağlar.

 [Atama kancaları ve CRT bellek ayırmaları](../debugger/allocation-hooks-and-c-run-time-memory-allocations.md) kısıtlama açıkça yoksayılıyor, atama kanca işlevleri açıklar `_CRT_BLOCK` iç bellek C çalışma zamanı kitaplık işlevleri çağrıları yaptıkları engeller. Bu konuda, atama kanca değil yoksayarsanız, ayrıca sonuçları listeler `_CRT_BLOCK` bloklarla (örnekler) ve varsayılan ayırma değiştirme kanca işlevini, **CrtDefaultAllocHook**.

 [Kanca işlevlerini rapor](../debugger/report-hook-functions.md) Discusses `_CrtSetReportHook`, ayırmaları belirli türlerde odaklanmak için filtre uygulamak için kullanabileceğiniz raporlar. Bu konu, bir prototip de sağlar.

## <a name="related-sections"></a>İlgili Bölümler

- [CRT hata ayıklama teknikleri](../debugger/crt-debugging-techniques.md) -bağlantılar için CRT hata ayıklama kitaplığı, raporlama için makroları kullanma dahil olmak üzere C çalışma zamanı kitaplığı hata ayıklama tekniklerine farkları arasında `malloc` ve `_malloc_dbg`, hata ayıklama kanca işlevlerini ve CRT yazma hata ayıklama yığını'nı tıklatın.