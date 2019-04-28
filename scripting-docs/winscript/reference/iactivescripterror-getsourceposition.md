---
title: IActiveScriptError::GetSourcePosition | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IActiveScriptError.GetSourcePosition
apilocation:
- scrobj.dll
helpviewer_keywords:
- IActiveScriptError_GetSourcePosition
ms.assetid: ae9b26b1-82a7-4645-9686-3261d8248664
caps.latest.revision: 7
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4446235a9584bc45fad84b6f92ecc02592e554f3
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63009630"
---
# <a name="iactivescripterrorgetsourceposition"></a>IActiveScriptError::GetSourcePosition
Komut dosyası altyapısı bir betik çalıştırılırken bir hata oluştuğu konum kaynak kodundaki alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetSourcePosition(  
    DWORD *pdwSourceContext,  // context cookie  
    ULONG *pulLineNumber,     // line number of error  
    LONG *pichCharPosition    // character position of error  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdwSourceContext`  
 [out] Bağlam tanımlayan bir çerez alan değişkenin adresi. Bu parametrenin yorumu konak uygulamaya bağlıdır.  
  
 `pulLineNumber`  
 [out] Hatanın oluştuğu kaynak dosyadaki satır numarası alan değişkenin adresi.  
  
 `pichCharPosition`  
 [out] Hatanın oluştuğu satırın içinde karakterin konumu alan değişkenin adresi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Döndürür `S_OK` başarılı olursa veya `E_FAIL` konumu değil almışsa.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IActiveScriptError](../../winscript/reference/iactivescripterror.md)