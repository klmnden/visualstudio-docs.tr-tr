---
title: Ijsdebugdatatarget::getthreadcontext metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- IJsDebugDataTarget.GetThreadContext
apilocation:
- jscript9diag.dll
ms.assetid: faf2a689-6c49-4a7d-b5a6-2b323e2257a7
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: d7904ef81eb900c6466069267101f30d89e362a1
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62582839"
---
# <a name="ijsdebugdatatargetgetthreadcontext-method"></a>IJsDebugDataTarget::GetThreadContext Yöntemi
Verilen iş parçacığı için bağlamı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
HRESULT GetThreadContext(  
   DWORD threadId,  
   ULONG32 contextFlags,  
   ULONG32 contextSize,  
   void *pContext  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `threadId`  
 [in] Hedef işlemde çalışan iş parçacığı.  
  
 `contextFlags`  
 [in] Bağlam bayraklarını belirtir. Bu, Context'in ContextFlags alanıyla aynıdır (daha fazla bilgi için bkz. winnt.h, context_all öğesini arayın) olarak aynıdır.  
  
 `contextSize`  
 [in] PContext tarafından belirlenen arabellek boyutu.  
  
 `pContext`  
 [out] Platforma özgü CONTEXT yapısını pContext tarafından belirlenen arabelleğine alır.  
  
## <a name="return-value"></a>Dönüş Değeri  
  
## <a name="requirements"></a>Gereksinimler  
 **Başlık:** jscript9diag.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IJsDebugDataTarget Arabirimi](../../winscript/reference/ijsdebugdatatarget-interface.md)