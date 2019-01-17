---
title: IActiveScriptSite::OnLeaveScript | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.OnLeaveScript
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_OnLeaveScript
ms.assetid: 79af0e22-fbe3-4fae-8a5f-7af8b857678d
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 7d08d58fc788d2d10ed044808ca40a5f4ea929c3
ms.sourcegitcommit: 8bf9e51c77a5a602fab9513b9187e59e57dfebad
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2019
ms.locfileid: "54348301"
---
# <a name="iactivescriptsiteonleavescript"></a>IActiveScriptSite::OnLeaveScript
Konak, komut dosyası altyapısı betik kodu yürütülmesini döndürdüğünü bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnLeaveScript(void);  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa.  
  
## <a name="remarks"></a>Açıklamalar  
 Komut dosyası altyapısı, komut dosyası altyapısı girilen çağıran bir uygulama denetimi döndürmeden önce bu yöntemi çağırmanız gerekir. Örneğin, betik, bir nesne çağırır, ardından komut dosyası altyapısı tarafından işlenen bir olayı tetikler, komut dosyası altyapısı çağırmalıdır [IActiveScriptSite::OnEnterScript](../../winscript/reference/iactivescriptsite-onenterscript.md) olay yürütmeden önce yöntemi ve çağırmalıdır`IActiveScriptSite::OnLeaveScript`sonra olay, olayı tetikleyen nesne döndürmeden önce yürütülüyor. Bu yönteme çağrıları yuvalanabilir. Yapılan her çağrı `IActiveScriptSite::OnEnterScript` bu yönteme yapılan çağrı gerektirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)