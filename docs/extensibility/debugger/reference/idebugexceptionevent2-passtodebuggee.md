---
title: IDebugExceptionEvent2::PassToDebuggee | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugExceptionEvent2::PassToDebuggee
helpviewer_keywords:
- IDebugExceptionEvent2::PassToDebuggee
ms.assetid: a20d0f0b-2ca0-4437-bd22-9213c81d2738
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 338127784a7ea4ee474edf1bfc58a75c5df7704d
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53945619"
---
# <a name="idebugexceptionevent2passtodebuggee"></a>IDebugExceptionEvent2::PassToDebuggee
Özel durum yürütme devam ettiğinde ayıklanan programa geçirilmelidir olup olmadığını ya da özel durum atılmalı belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT PassToDebuggee(  
   BOOL fPass  
);  
```  
  
```csharp  
int PassToDebuggee(  
   int fPass  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fPass`  
 [in] Sıfır olmayan (`TRUE`) özel durum yürütme devam ettiğinde ayıklanan programa veya sıfır geçirilmelidir varsa (`FALSE`) varsa özel durumun atılması gerekir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemin çağrılması gerçekten ayıklanan programa yürütülecek herhangi bir kodu neden olmaz. Çağrı yalnızca sonraki kod yürütme için durum ayarlamaktır. Örneğin, çağrılar [CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md) yöntemi döndürebilir `S_OK` ile [EXCEPTION_INFO](../../../extensibility/debugger/reference/exception-info.md).`dwState` alanın ayarlanacağı `EXCEPTION_STOP_SECOND_CHANCE`.  
  
 IDE alabilirsiniz [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md) olay ve arama [devam](../../../extensibility/debugger/reference/idebugprogram2-continue.md) yöntemi. Hata ayıklama altyapısı (DE) büyük/küçük harf ise işlemek için bir varsayılan davranışı olması gereken `PassToDebuggee` yöntemi çağrılmadı.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugExceptionEvent2](../../../extensibility/debugger/reference/idebugexceptionevent2.md)   
 [CanPassToDebuggee](../../../extensibility/debugger/reference/idebugexceptionevent2-canpasstodebuggee.md)   
 [Continue](../../../extensibility/debugger/reference/idebugprogram2-continue.md)