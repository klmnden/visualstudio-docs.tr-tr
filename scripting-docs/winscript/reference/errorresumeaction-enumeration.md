---
title: ERRORRESUMEACTION listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- ERRORRESUMEACTION
apilocation:
- scrobj.dll
helpviewer_keywords:
- ERRORRESUMEACTION enumeration
ms.assetid: a68293c8-056b-439f-83e7-69e4a38f4976
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d78852a05226f5112447dd142c06a2ba55ddba5a
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54347235"
---
# <a name="errorresumeaction-enumeration"></a>ERRORRESUMEACTION Listelemesi
Bir çalışma zamanı hatasından nasıl devam edileceğini açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef enum tagERRORRESUMEACTION {  
   ERRORRESUMEACTION_ReexecuteErrorStatement,  
   ERRORRESUMEACTION_AbortCallAndReturnErrorToCaller,  
   ERRORRESUMEACTION_SkipErrorStatement,  
} ERRORRESUMEACTION;  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Açıklama|  
|------------|-----------------|  
|ERRORRESUMEACTION_ReexecuteErrorStatement|Yeniden hataya neden deyimi yürütür.|  
|ERRORRESUMEACTION_AbortCallAndReturnErrorToCaller|Hata işleme dil altyapısı sağlar.|  
|ERRORRESUMEACTION_SkipErrorStatement|Hataya neden olan deyimden sonraki kod yürütmeyi devam ettirir.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)