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
ms.openlocfilehash: 025591ffea4d6746f87e5f1240cd226fa291d116
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62905515"
---
# <a name="mixed-code-and-missing-information-in-the-call-stack-window"></a>Çağrı Yığını Penceresinde Karışık Kod ve Eksik Bilgiler
Yönetilen ve yerel kod için çağrı yığınlarını arasındaki farklar nedeniyle, hata ayıklayıcı kod karışımı yazdığında tam çağrı yığınını her zaman gösteremez. Yerel kod yönetilen kodu çağırdığında, aşağıdaki tutarsızlıklar görebilirsiniz **çağrı yığını** penceresi:

- Yönetilen kod hemen üstündeki yerel çerçeve eksik **çağrı yığını** penceresi. Daha fazla bilgi için [nasıl yapılır: Yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına Adımlama](../debugger/how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window.md).

- Karışık mod uygulamaları hata ayıklayıcı dışında tarafından başlatılan **çağrı yığını** pencere, yalnızca yönetilen kod görüntüleyebilir ve yerel çerçeveler hiçbiri görünür olur.

  Her iki durumda oldukça nadir. Yönetilen kod için yerel en çağrılarında doğru çağrı yığınlarını görünür.

## <a name="see-also"></a>Ayrıca Bkz.
- [Nasıl yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)