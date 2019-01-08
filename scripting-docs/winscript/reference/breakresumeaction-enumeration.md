---
title: BREAKRESUMEACTION listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- BREAKRESUMEACTION
apilocation:
- scrobj.dll
helpviewer_keywords:
- BREAKRESUMEACTION enumeration
ms.assetid: b39fcc82-7776-4caa-8155-b398de68df03
caps.latest.revision: 9
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 3186ac39353d11f327f7940ae5fc03ae2238ddd9
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090474"
---
# <a name="breakresumeaction-enumeration"></a>BREAKRESUMEACTION Listelemesi
Bir kesme noktasından devam etmek için yöntemleri açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagBREAKRESUME_ACTION {  
   BREAKRESUMEACTION_ABORT,  
   BREAKRESUMEACTION_CONTINUE,  
   BREAKRESUMEACTION_STEP_INTO,  
   BREAKRESUMEACTION_STEP_OVER,  
   BREAKRESUMEACTION_STEP_OUT,  
   BREAKRESUMEACTION_IGNORE,  
   BREAKRESUMEACTION_STEP_DOCUMENT,  
} BREAKRESUMEACTION;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|BREAKRESUMEACTION_ABORT|Uygulamayı durdurur.|  
|BREAKRESUMEACTION_CONTINUE|Çalışmaya devam eder.|  
|BREAKRESUMEACTION_STEP_INTO|Bir yordam adımlamayla girin.|  
|BREAKRESUMEACTION_STEP_OVER|Adım bir yordam boyunca.|  
|BREAKRESUMEACTION_STEP_OUT|Adımları güncel süreçte dışında.|  
|BREAKRESUMEACTION_IGNORE|Durumuna sahip çalışmaya devam eder.|  
|BREAKRESUMEACTION_STEP_DOCUMENT|Sonraki belge için adımlar.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)