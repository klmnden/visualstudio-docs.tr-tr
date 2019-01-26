---
title: DebugBreak ve __debugbreak | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- DebugBreak
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging [C++], DebugBreak function
- DebugBreak function
- breakpoints, DebugBreak function
ms.assetid: 9787c795-df94-4f48-bc8d-3bf899b67421
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: cb05c054ffc5dd273b532f72afe0ca046adbe606
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55041730"
---
# <a name="debugbreak-and-debugbreak"></a>DebugBreak ve __debugbreak
DebugBreak Win32 işlevini çağırabilir veya [__debugbreak](/cpp/intrinsics/debugbreak) kodunuzdaki herhangi bir noktada iç. `DebugBreak` ve `__debugbreak` bu konumda bir kesme noktası ayarlamak aynı etkiye sahiptir.  
  
 Çünkü `DebugBreak` bir sistem işlevi, sistem hata ayıklama sembolleri yüklü, doğru çağrı yığını bilgilerini sonra son görüntülendiğinden emin olmak için bir çağrı gibidir. Aksi takdirde, hata ayıklayıcı tarafından görüntülenen çağrı yığını bilgilerini bir çerçeve tarafından kapalı olması. Kullanırsanız `__debugbreak`, semboller gerekli değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derleyici iç bilgileri](/cpp/intrinsics/compiler-intrinsics)   
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)   
 [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)