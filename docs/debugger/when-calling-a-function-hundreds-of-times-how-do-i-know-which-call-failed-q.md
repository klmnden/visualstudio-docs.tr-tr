---
title: Bir işlevi birçok kez çağırırken başarısız çağrı bulun | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.functions
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- conditional breakpoints
- errors [debugger], function calls
- breakpoints, troubleshooting
- errors [debugger], finding which function call failed
- failures
- location breakpoint call failures
- errors [Visual Studio], function calls
- hit counts
- function calls, failure
- functions [debugger]
- Skip Count
ms.assetid: 66cfac86-f5be-4d3a-9329-d44cd74bc586
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: fa6fb9613df5f5bffb50c9a161eaa0a0254f26dd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62901007"
---
# <a name="when-calling-a-function-hundreds-of-times-how-do-i-know-which-call-failed"></a>İşlevi Yüzlerce Kere Çağırırken Hangi Çağrının Başarısız Olduğunu Nasıl Bilebilirim?
## <a name="problem-description"></a>Sorun açıklaması
 Kendi programımı belirli bir işlev çağrısı başarısız `CnvtV`. Bu başarısız olmadan önce programı büyük olasılıkla bu işlev birkaç yüzlerce kez çağırır. Ben bir konum kesme noktası ayarlarsanız, `CnvtV`, söz konusu işleve yapılan her çağrıda programı durdurur ve bu istemiyorum. Koşullu kesme noktası olarak ayarlanamıyor için hangi koşullar çağrının başarısız olmasına neden bilmiyorum. Ne yapabilirim?

## <a name="solution"></a>Çözüm
 İşlevi ile bir kesme noktası ayarlayabilirsiniz **Hit Count** , hiçbir zaman ulaşılacak kadar yüksek bir değer alanı. Bu durumda, işlev düşünüyorsanız çünkü `CnvtV` birkaç çağrılır, yüzlerce kez ayarlayabilirsiniz **isabet sayısı** 1000 veya daha fazla. Ardından programı çalıştırın ve başarısız çağrının tamamlanmasını bekleyin. Bu başarısız olduğunda, kesme noktaları penceresi açın ve kesme noktalarının listesine bakın. Üzerinde ayarladığınız kesme noktası `CnvtV` görünür, ardından isabet sayısı ve kalan yineleme sayısı:

```cpp
CnvtV(int) (no condition) when hit count is equal to 1000 (currently 101)
```

 İşlev 101st çağrıda başarısız olduğunu biliyorsunuz. Kesme noktası isabet sayısını 101 ile sıfırlama ve programı yeniden çalıştırın, program çağrısı durakları `CnvtV` , başarısız olmasına neden.

## <a name="see-also"></a>Ayrıca Bkz.
- [Yerel Kodda Hata Ayıklama SSS](../debugger/debugging-native-code-faqs.md)
- [Kesme noktaları ayarlama](https://msdn.microsoft.com/library/fe4eedc1-71aa-4928-962f-0912c334d583)
- [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)
