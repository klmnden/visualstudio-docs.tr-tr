---
title: Ijsdebugbreakpoint::IsEnabled yöntemi | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJSDebugBreakPoint.IsEnabled
apilocation:
- jscript9diag.dll
ms.assetid: 39b63f49-2a0d-41b7-a2ba-75dcb06251a9
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b99df17f73896b4dd04481315b04e1672a56285a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62583099"
---
# <a name="ijsdebugbreakpointisenabled-method"></a>IJsDebugBreakPoint::IsEnabled Yöntemi
Kesme noktasının etkinleştirilip etkinleştirilmeyeceğini belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT IsEnabled(  
   BOOL *pIsEnabled  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pIsEnabled`  
 [out] Kesme noktası etkinleştirildiğinde true döndürür; Aksi takdirde false döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Silinen bir kesme noktasına çağrılırsa E_UNEXPECTED döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugBreakPoint Arabirimi](../../winscript/reference/ijsdebugbreakpoint-interface.md)