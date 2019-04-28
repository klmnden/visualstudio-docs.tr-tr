---
title: Ijsdebugstackwalker::GetNext metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugStackWalker.GetNext
apilocation:
- jscript9diag.dll
ms.assetid: 0b124768-50d3-4a69-876c-1aa337839a4e
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: ba8931a01f3afe05f791f4d89da60a9354868215
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62977880"
---
# <a name="ijsdebugstackwalkergetnext-method"></a>IJsDebugStackWalker::GetNext Metodu
Sonraki çerçeveyi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetNext(  
   IJsDebugFrame **ppFrame  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppFrame`  
 [out] Yığın çerçevesini temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="remarks"></a>Açıklamalar  
 Numaralandırılacak daha fazla yığın çerçeve olmadığında e_jsdebug_outsıde_of_vm döndürür.  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugStackWalker Arabirimi](../../winscript/reference/ijsdebugstackwalker-interface.md)