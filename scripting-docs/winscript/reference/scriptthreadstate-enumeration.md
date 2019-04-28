---
title: SCRIPTTHREADSTATE sabit listesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- SCRIPTTHREADSTATE
apilocation:
- scrobj.dll
helpviewer_keywords:
- SCRIPTTHREADSTATE enum
ms.assetid: 975ec66b-c095-40ac-8ba9-631adb97b589
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 906a309b25a1fe606fb37f8cbab70040e5a4c46f
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62840193"
---
# <a name="scriptthreadstate-enumeration"></a>SCRIPTTHREADSTATE Numaralandırması
Bir komut dosyası altyapısı bir iş parçacığı durumunu belirtir. Bu sabit listesi tarafından kullanılan [IActiveScript::GetScriptThreadState](../../winscript/reference/iactivescript-getscriptthreadstate.md) yöntemi.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagSCRIPTTHREADSTATE {  
    SCRIPTTHREADSTATE_NOTINSCRIPT  = 0,  
    SCRIPTTHREADSTATE_RUNNING      = 1  
} SCRIPTTHREADSTATE;  
```  
  
## <a name="enumeration-values"></a>Sabit listesi değerleri  
  
|||  
|-|-|  
|SCRIPTTHREADSTATE_NOTINSCRIPT|Belirtilen iş parçacığı henüz hemen yürütülen işlem komut metni komut dosyalı bir olay hizmet veya çalışan bir betik makrosu.|  
|SCRIPTTHREADSTATE_RUNNING|Belirtilen iş parçacığı etkin olarak komut dosyalı bir olay işleme hemen yürütülen betik metin Bakım veya çalışan bir betik makrosu.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Sabitleri, Sabit Listeleri ve Hata Kodları](../../winscript/reference/active-script-constants-enumerations-and-error-codes.md)