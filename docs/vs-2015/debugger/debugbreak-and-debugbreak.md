---
title: DebugBreak ve __debugbreak | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- DebugBreak
dev_langs:
- FSharp
- VB
- CSharp
- C++
- C++
helpviewer_keywords:
- debugging [C++], DebugBreak function
- DebugBreak function
- breakpoints, DebugBreak function
ms.assetid: 9787c795-df94-4f48-bc8d-3bf899b67421
caps.latest.revision: 26
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 73b818269695322d06c95e5ae39f5bdfd7059dae
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49281118"
---
# <a name="debugbreak-and-debugbreak"></a>DebugBreak ve __debugbreak
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

DebugBreak Win32 işlevini çağırabilir veya [__debugbreak](http://msdn.microsoft.com/library/1d1e1c0c-891a-4613-ae4b-d790094ba830) kodunuzdaki herhangi bir noktada iç. `DebugBreak` ve `__debugbreak` bu konumda bir kesme noktası ayarlamak aynı etkiye sahiptir.  
  
 Çünkü `DebugBreak` bir sistem işlevi, sistem hata ayıklama sembolleri yüklü, doğru çağrı yığını bilgilerini sonra son görüntülendiğinden emin olmak için bir çağrı gibidir. Aksi takdirde, hata ayıklayıcı tarafından görüntülenen çağrı yığını bilgilerini bir çerçeve tarafından kapalı olması. Kullanırsanız `__debugbreak`, semboller gerekli değildir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Derleyici iç bilgileri](http://msdn.microsoft.com/library/48bb9929-7d78-4fd8-a092-ae3c9f971858)   
 [Hata ayıklayıcısı güvenliği](../debugger/debugger-security.md)   
 [Yerel kodda hata ayıklama](../debugger/debugging-native-code.md)   
 [Simge (.pdb) ve Kaynak Dosyaları Belirtme](../debugger/specify-symbol-dot-pdb-and-source-files-in-the-visual-studio-debugger.md)



