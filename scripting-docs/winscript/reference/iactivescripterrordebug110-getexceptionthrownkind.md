---
title: Iactivescripterrordebug110::getexceptionthrownkind | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
helpviewer_keywords:
- IActiveScriptErrorDebug110::QueryIsFirstChance
ms.assetid: ecc16e54-93e4-4322-ae13-afa7cd860032
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a58add60560f22681f18225d844814e3547b671f
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63436066"
---
# <a name="iactivescripterrordebug110getexceptionthrownkind"></a>IActiveScriptErrorDebug110::GetExceptionThrownKind
Oluşan özel durumun türünü gösteren bir değeri döndürür.  
  
> [!IMPORTANT]
> [Iactivescripterrordebug110 arabirimi](../../winscript/reference/iactivescripterrordebug110-interface.md) PDM sürümü 11.0 ve daha sonraki sürümleri tarafından uygulanır. activdbg100.h içinde bulunur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetExceptionThrownKind(  
   SCRIPT_ERROR_DEBUG_EXCEPTION_THROWN_KIND*  pExceptionKind  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pExceptionKind`  
 [out] (Örneğin, ilk şans veya işlenmemiş), oluşturulan özel durum türünü temsil ettiği bir [scrıpt_error_debug_exceptıon_thrown_kınd listelemesi](../../winscript/reference/script-error-debug-exception-thrown-kind-enumeration.md) numaralandırma değeri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptErrorDebug110 Arabirimi](../../winscript/reference/iactivescripterrordebug110-interface.md)