---
title: IActiveScriptWinRTErrorDebug::GetRestrictedErrorReference | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptWinRTErrorDebug::GetRestrictedErrorReference
ms.assetid: fcf60971-9518-4b24-a3a6-1e2e30a02cea
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d4696c66ec331c08f3419d79f0f48feb3bf9d80f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63432967"
---
# <a name="iactivescriptwinrterrordebuggetrestrictederrorreference"></a>IActiveScriptWinRTErrorDebug::GetRestrictedErrorReference
Windows çalışma zamanı döndürür, varsa başvuru hatası kısıtlı.  
  
> [!IMPORTANT]
> [Iactivescriptwinrterrordebug arabirimi](../../winscript/reference/iactivescriptwinrterrordebug-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetRestrictedErrorReference([out] BSTR * referenceString);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `referenceString`  
 [out] Başvuru hata dizesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptWinRTErrorDebug Arabirimi](../../winscript/reference/iactivescriptwinrterrordebug-interface.md)