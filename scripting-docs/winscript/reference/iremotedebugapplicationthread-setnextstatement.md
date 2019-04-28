---
title: IRemoteDebugApplicationThread::SetNextStatement | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IRemoteDebugApplicationThread.SetNextStatement
apilocation:
- pdm.dll
helpviewer_keywords:
- IRemoteDebugApplicationThread::SetNextStatement
ms.assetid: 356766da-f7b7-4e8d-b4f3-2ab8da0609b8
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 0c4b19322a15e92adcf2609c479af6b21e2078bd
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62788152"
---
# <a name="iremotedebugapplicationthreadsetnextstatement"></a>IRemoteDebugApplicationThread::SetNextStatement
Verilen kod bağlamı için mümkün olduğunca yakın verilen çerçevesi bağlamında devam etmek için yürütme zorlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT SetNextStatement(  
   IDebugStackFrame*   pStackFrame,  
   IDebugCodeContext*  pCodeContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pStackFrame`  
 [in] Yığın çerçeve nesnesi. Bu bağımsız değişken, geçerli yığın çerçevesi kullanılmalıdır gelir NULL olabilir.  
  
 `pCodeContext`  
 [in] Kod bağlamı. Bu bağımsız değişken, geçerli kod bağlamı kullanılmalıdır gelir NULL olabilir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Yöntem döndürür bir `HRESULT`. Olası değerler aşağıdaki tablodakileri içerir, ancak bunlarla da sınırlı değildir:  
  
|Değer|Açıklama|  
|-----------|-----------------|  
|`S_OK`|Yöntem başarılı oldu.|  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem tarafından belirtilen kod bağlamı için mümkün olduğunca yakın devam etmek için yürütme zorlar `pCodeContext`, çerçeve tarafından belirtilen bağlamında `pStackFrame`. Bu bağımsız değişken olabilir `NULL`, geçerli çerçeve veya bağlamını temsil eder.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IRemoteDebugApplicationThread Arabirimi](../../winscript/reference/iremotedebugapplicationthread-interface.md)