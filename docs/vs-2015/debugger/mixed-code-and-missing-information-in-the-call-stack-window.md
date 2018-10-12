---
title: Kod ve eksik bilgiler çağrı yığını penceresinde karışık | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- FSharp
- VB
- CSharp
- C++
- JScript
- SQL
- VB
- CSharp
- C++
helpviewer_keywords:
- managed code, stepping
- Call Stack window, mixed-mode debugging
- Call Stack window, troubleshooting
- native frames
- managed call stacks
- mixed-mode debugging, call stack
- stepping, out of managed code
ms.assetid: dd628427-e8d6-4fc2-b524-9d6393ea5376
caps.latest.revision: 23
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 03277af5f1cca5c3ded7b43a82ca6bbe74c5e756
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49212218"
---
# <a name="mixed-code-and-missing-information-in-the-call-stack-window"></a>Çağrı Yığını Penceresinde Karışık Kod ve Eksik Bilgiler
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Yönetilen ve yerel kod için çağrı yığınlarını arasındaki farklar nedeniyle, hata ayıklayıcı kod karışımı yazdığında tam çağrı yığınını her zaman gösteremez. Yerel kod yönetilen kodu çağırdığında, aşağıdaki tutarsızlıklar görebilirsiniz **çağrı yığını** penceresi:  
  
-   Yönetilen kod hemen üstündeki yerel çerçeve eksik **çağrı yığını** penceresi. Daha fazla bilgi için [nasıl yapılır: yerel çerçeveler eksik çağrı yığını penceresinde olmadığında yönetilen kodların dışına Adımlama](../debugger/how-to-step-out-of-managed-code-when-native-frames-are-missing-from-the-call-stack-window.md).  
  
-   Karışık mod uygulamaları hata ayıklayıcı dışında tarafından başlatılan **çağrı yığını** pencere, yalnızca yönetilen kod görüntüleyebilir ve yerel çerçeveler hiçbiri görünür olur.  
  
 Her iki durumda oldukça nadir. Yönetilen kod için yerel en çağrılarında doğru çağrı yığınlarını görünür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Nasıl Yapılır: Çağrı Yığını Penceresini Kullanma](../debugger/how-to-use-the-call-stack-window.md)





