---
title: IActiveScriptError::GetSourcePosition | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: fb5adfe508b7b5d3de0cf7f508d8c801a36adf1f
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54097376"
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