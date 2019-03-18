---
title: Ijsdebugframe::getstackrange metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugFrame.GetStackRange
apilocation:
- jscript9diag.dll
ms.assetid: a6d1d8be-efc0-442d-9756-1959c8f102bd
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 52dd6114d3ec462f91f8bce5e76f73c5487746ed
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58147442"
---
# <a name="ijsdebugframegetstackrange-method"></a>IJsDebugFrame::GetStackRange Yöntemi
Mantıksal JavaScript yığın çerçevesinin mutlak adres aralığını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetStackRange(  
   UINT64 *pStart,  
   UINT64 *pEnd  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pStart`  
 [out] Çerçevenin yığın işaretçisinin en altı.  
  
 `pEnd`  
 [out] Çoğu çerçevenin yığın işaretçisinin en iyi.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, birden çok çalışma zamanından toplanan Aralanmış yığın izlemelerini birbirine eklemekten için kullanışlıdır. Başlangıç, bitiş yığın işaretçileri, birden fazla fiziksel makine yığın çerçevesini (yorumlanan JavaScript çalışma zamanı çerçeveleri) kapsayabilir. Başlangıç > bitiş yığın yüksek adresten düşük adrese büyüdükçe gibi.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugFrame Arabirimi](../../winscript/reference/ijsdebugframe-interface.md)