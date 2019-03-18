---
title: BREAKREASON listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- BREAKREASON
apilocation:
- scrobj.dll
helpviewer_keywords:
- BREAKREASON enumeration
ms.assetid: bde07ede-2f9b-4fa2-affc-f9405683f5f7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 939d9f36c9838f02e58bc433d1a7bb9bef43c28d
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58160595"
---
# <a name="breakreason-enumeration"></a>BREAKREASON Listelemesi
Kesilmenin nedenini gösterir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagBREAKREASON {  
   BREAKREASON_STEP,  
   BREAKREASON_BREAKPOINT,  
   BREAKREASON_DEBUGGER_BLOCK,  
   BREAKREASON_HOST_INITIATED,  
   BREAKREASON_LANGUAGE_INITIATED,  
   BREAKREASON_DEBUGGER_HALT,  
   BREAKREASON_ERROR,  
   BREAKREASON_JIT  
} BREAKREASON;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|BREAKREASON_STEP|Dil altyapısı Adımlama modundadır.|  
|BREAKREASON_BREAKPOINT|Dil altyapısı, açık bir kesme noktası karşılaştı.|  
|BREAKREASON_DEBUGGER_BLOCK|Dil altyapısı, başka bir iş parçacığında bir hata ayıklayıcı blok karşılaştı.|  
|BREAKREASON_HOST_INITIATED|Konak, bir kesme istedi.|  
|BREAKREASON_LANGUAGE_INITIATED|Dil altyapısı, bir kesme istedi.|  
|BREAKREASON_DEBUGGER_HALT|IDE hata ayıklayıcı bir kesme istedi.|  
|BREAKREASON_ERROR|Bir yürütme hatası kesilmenin nedenini.|  
|BREAKREASON_JIT|JIT hata ayıklama başlatma işlemi tarafından neden oldu.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)