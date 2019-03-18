---
title: IActiveScriptSite::OnEnterScript | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptSite.OnEnterScript
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptSite_OnEnterScript
ms.assetid: 1ed9178c-fe80-41c4-b74d-23b85f9cddbf
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 5505b30bbfd4e1cbc33022d38d7b7170ffd37dd3
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58150407"
---
# <a name="iactivescriptsiteonenterscript"></a>IActiveScriptSite::OnEnterScript
Konak, komut dosyası altyapısı betik kodu yürüten başlatıldığını bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT OnEnterScript(void);  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa.  
  
## <a name="remarks"></a>Açıklamalar  
 Komut dosyası altyapısı, bu yöntem her girdi veya deðiþiklik komut dosyası altyapısı çağırmalıdır. Örneğin, betik, bir nesne çağırır, ardından komut dosyası altyapısı tarafından işlenen bir olayı tetikler, komut dosyası altyapısı çağırmalıdır `IActiveScriptSite::OnEnterScript` önce olay yürütme ile çağırmalısınız [IActiveScriptSite::OnLeaveScript](../../winscript/reference/iactivescriptsite-onleavescript.md) Olay yürütülürken sonra ancak olayı tetikleyen nesne döndürmeden önce yöntemi. Bu yönteme çağrıları yuvalanabilir. Bu yöntem yapılan her çağrı bir çağrı ile gerektirir `IActiveScriptSite::OnLeaveScript`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptSite](../../winscript/reference/iactivescriptsite.md)