---
title: Ijsdebugprocess arabirimi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: a7ad5525-55b7-4c68-a4f7-c508f7877712
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 411679a03daf27046fdcede7ff48e76212bbd2fd
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58158925"
---
# <a name="ijsdebugprocess-interface"></a>IJsDebugProcess Arabirimi
İncelemek ve hedef işlem denetleme için yordamlar sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
IJsDebugProcess : public IUnknown;  
```  
  
## <a name="members"></a>Üyeler  
  
### <a name="public-methods"></a>Ortak Yöntemler  
  
|Ad|Açıklama|  
|----------|-----------------|  
|[IJsDebugProcess::CreateBreakPoint Metodu](../../winscript/reference/ijsdebugprocess-createbreakpoint-method.md)|Belge belirtilen konumda bir kesme noktası ayarlar.|  
|[IJsDebugProcess::CreateStackWalker Metodu](../../winscript/reference/ijsdebugprocess-createstackwalker-method.md)|Yığın değişkeni için fabrika yöntemi.|  
|[IJsDebugProcess::PerformAsyncBreak Metodu](../../winscript/reference/ijsdebugprocess-performasyncbreak-method.md)|Komut dosyası altyapısı sonraki komut dosyası yönergesi üzerinde kesmesine neden, kesme moduna koyar.|  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Windows Betik Arabirimleri Başvurusu](../../winscript/reference/windows-script-interfaces-reference.md)