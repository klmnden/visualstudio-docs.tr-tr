---
title: Scrıpt_error_debug_exceptıon_thrown_kınd listelemesi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: b3aa4966-e110-4b30-b368-1281a9740dbd
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b9dae0161e3337411a56e316e04cf467a1f05e6a
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58155725"
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