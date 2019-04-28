---
title: IActiveScriptWinRTErrorDebug::GetRestrictedErrorString | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptWinRTErrorDebug::GetRestrictedErrorString
ms.assetid: d901e049-fb1b-4101-a04a-1395d657f1cf
caps.latest.revision: 5
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 154909183e044267053a04ebc489de6dddd55788
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63425868"
---
# <a name="iactivescriptwinrterrordebuggetrestrictederrorstring"></a>IActiveScriptWinRTErrorDebug::GetRestrictedErrorString
Varsa, döndürür Windows çalışma zamanı hata dizesi kısıtlı.  
  
> [!IMPORTANT]
> [Iactivescriptwinrterrordebug arabirimi](../../winscript/reference/iactivescriptwinrterrordebug-interface.md) PDM v11.0 tarafından uygulanan ve büyük. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetRestrictedErrorString([out] BSTR * errorString);   
```  
  
#### <a name="parameters"></a>Parametreler  
 `errorString`  
 [out] Yasak hata dizesi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptWinRTErrorDebug Arabirimi](../../winscript/reference/iactivescriptwinrterrordebug-interface.md)