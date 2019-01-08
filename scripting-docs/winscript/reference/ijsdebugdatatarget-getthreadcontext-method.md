---
title: Ijsdebugdatatarget::getthreadcontext metodu | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.prod: windows-script-interfaces
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
ms.openlocfilehash: 50e2bdb7b8720549aac5e5b3c4cebffc4b7ae892
ms.sourcegitcommit: 116e9614867e0b3c627ce9001012a4c39435a42b
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/08/2019
ms.locfileid: "54090070"
---
# <a name="ijsdebugdatatargetgetthreadcontext-method"></a>IJsDebugDataTarget::GetThreadContext Metodu
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