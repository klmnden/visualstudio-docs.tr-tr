---
title: Ijsdebugframe::getstackrange metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 049be8a665dae396d4e92fe847e757b266dc6025
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090291"
---
# <a name="ijsdebugframegetstackrange-method"></a>IJsDebugFrame::GetStackRange Metodu
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