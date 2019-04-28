---
title: BREAKRESUMEACTION listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
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
ms.openlocfilehash: e5c79aacc64eb57282bf09f7e4673980396b37ea
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62955295"
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