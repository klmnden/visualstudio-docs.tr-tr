---
title: IDebugApplication::DebugOutput | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IDebugApplication.DebugOutput
apilocation:
- pdm.dll
helpviewer_keywords:
- IDebugApplication::DebugOutput
ms.assetid: 6c02939c-3c2d-474a-ab15-49a37e22b4a7
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a67a16e3fd4868726087df6f2596571d14630f80
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62990976"
---
# <a name="idebugapplicationdebugoutput"></a>IDebugApplication::DebugOutput
Hata ayıklayıcı tümleşik geliştirme ortamı (IDE) tarafından görüntülenecek verilen dize neden olur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT DebugOutput(  
   LPCOLESTR  pstr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pstr`  
 [in] Hata Ayıklayıcısı'nda görüntülenecek dize.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, dile özgü hata ayıklama çıktı desteği uygulamak bir dil altyapısı sağlar. Dize, genellikle hata ayıklayıcının çıkış penceresinde görüntülenir.  
  
 Bu yöntem neden `IApplicationDebugger::onDebugOutput` çağrılabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idebugapplication arabirimi](../../winscript/reference/idebugapplication-interface.md)   
 [IApplicationDebugger::onDebugOutput](../../winscript/reference/iapplicationdebugger-ondebugoutput.md)