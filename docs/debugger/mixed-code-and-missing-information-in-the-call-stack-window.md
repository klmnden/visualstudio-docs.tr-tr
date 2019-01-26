---
title: Kod ve eksik bilgiler çağrı yığını penceresinde karışık | Microsoft Docs
ms.date: 11/04/2016
ms.topic: troubleshooting
dev_langs:
- CSharp
- VB
- FSharp
- C++
- JScript
- SQL
helpviewer_keywords:
- managed code, stepping
- Call Stack window, mixed-mode debugging
- Call Stack window, troubleshooting
- native frames
- managed call stacks
- mixed-mode debugging, call stack
- stepping, out of managed code
ms.assetid: dd628427-e8d6-4fc2-b524-9d6393ea5376
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: dc43ba24e821c00adb4efb64e4785e02dae31f28
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992561"
---
# <a name="mixed-code-and-missing-information-in-the-call-stack-window"></a>Çağrı Yığını Penceresinde Karışık Kod ve Eksik Bilgiler
Yönetilen ve yerel kod için çağrı yığınlarını arasındaki farklar nedeniyle, hata ayıklayıcı kod karışımı yazdığında tam çağrı yığınını her zaman gösteremez. Yerel kod yönetilen kodu çağırdığında, aşağıdaki tutarsızlıklar görebilirsiniz **çağrı yığını** penceresi:  
  
- Yönetilen kod hemen üstündeki yerel çerçeve eksik **çağrı yığını** penceresi. Daha fazla bilgi için [nasıl yapılır: Yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına Adımlama](../debugger/how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window.md).  
  
- Karışık mod uygulamaları hata ayıklayıcı dışında tarafından başlatılan **çağrı yığını** pencere, yalnızca yönetilen kod görüntüleyebilir ve yerel çerçeveler hiçbiri görünür olur.  
  
  Her iki durumda oldukça nadir. Yönetilen kod için yerel en çağrılarında doğru çağrı yığınlarını görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)