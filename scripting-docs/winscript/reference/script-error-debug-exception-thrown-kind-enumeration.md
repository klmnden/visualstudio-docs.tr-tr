---
title: Scrıpt_error_debug_exceptıon_thrown_kınd listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: b3aa4966-e110-4b30-b368-1281a9740dbd
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 997c5149467591a7612e6ff10b0efcc3efbc91bf
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54087808"
---
# <a name="scripterrordebugexceptionthrownkind-enumeration"></a>SCRIPT_ERROR_DEBUG_EXCEPTION_THROWN_KIND Listelemesi
Oluşan özel durumun türünü gösterir. Bu sabit listesi tarafından kullanılan [Iactivescripterrordebug110::getexceptionthrownkind](../../winscript/reference/iactivescripterrordebug110-getexceptionthrownkind.md) yöntemi.  
  
> [!IMPORTANT]
>  Bu sabitler PDM sürüm 11.0 ve daha sonraki sürümleri tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef SCRIPT_ERROR_DEBUG_EXCEPTION_THROWN_KIND  
```  
  
## <a name="members"></a>Üyeler  
  
|Üye|Değer|Açıklama|  
|------------|-----------|-----------------|  
|ETK_FIRST_CHANCE|0x00000000|Özel durum bir ilk şans özel durumudur.|  
|ETK_USER_UNHANDLED|0x00000001|Özel durum kullanıcı kodunda işlenmez.|  
|ETK_UNHANDLED|0x00000002|Özel durum kodda işlenmez.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptErrorDebug110 Arabirimi](../../winscript/reference/iactivescripterrordebug110-interface.md)