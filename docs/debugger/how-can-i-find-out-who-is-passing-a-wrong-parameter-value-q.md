---
title: Yanlış parametre değeri geçirdiğini bulun | Microsoft Docs
ms.custom: seodec18
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.debug.parameters
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], parameters
- parameters [debugger]
- passing parameters, troubleshooting wrong values
- functions [debugger], detecting wrong parameter values
- parameter values, troubleshooting
ms.assetid: 1f1ae455-0e25-4e9d-b33f-53908f5bd6ce
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 548851a4e5811864e60d3a14368d6380f14f9e7e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62894885"
---
# <a name="how-can-i-find-out-who-is-passing-a-wrong-parameter-value"></a>Kimin Yanlış Parametre Değeri Geçirdiğini Nasıl Bulabilirim?
## <a name="problem-description"></a>Sorun açıklaması
 Benim birine yanlış parametre değeri geçirilir. Bu işlev her yerden çağrılır. Nasıl öğrenebilirim kullanıma neyin yanlış değer geçiyor?

## <a name="solution"></a>Çözüm

#### <a name="to-resolve-this-problem"></a>Bu sorunu gidermek için

1. İşlevin başında bir konum kesme noktası ayarlayın.

2. Kesme noktasına sağ tıklayıp **koşul**.

3. İçinde **kesme noktası koşulu** iletişim kutusu, tıklayarak **koşul** onay kutusu. Bkz: [kesme noktalarının Gelişmiş](../debugger/using-breakpoints.md#BKMK_Specify_a_breakpoint_condition_using_a_code_expression).

4. Gibi bir ifade girin `Var==3`, metin kutusuna, burada `Var` hatalı değeri içeren parametrenin adıdır ve `3` ona iletilen hatalı değer.

5. Seçin **true'dur** radyo düğmesini tıklatıp tıklayın **Tamam** düğmesi.

6. Şimdi programı yeniden çalıştırın. Kesme noktası programın işlevin başında durdurulmasına neden olduğunda `Var` parametresinin değeri `3`.

7. Çağıran işlevi bulmak ve kaynak koduna gitmek için çağrı yığını penceresini kullanın. Daha fazla bilgi için [nasıl yapılır: Çağrı yığını penceresini kullanma](../debugger/how-to-use-the-call-stack-window.md).

## <a name="see-also"></a>Ayrıca Bkz.
- [Yerel Kodda Hata Ayıklama SSS](../debugger/debugging-native-code-faqs.md)
- [Kesme Noktaları](https://msdn.microsoft.com/library/fe4eedc1-71aa-4928-962f-0912c334d583)
- [Yerel Kodda Hata Ayıklama](../debugger/debugging-native-code.md)