---
title: IDebugCanStopEvent2::CanStop | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCanStopEvent2::CanStop
helpviewer_keywords:
- IDebugCanStopEvent2::CanStop
ms.assetid: 7d61adbe-6b3d-41f3-86a1-45d9cc01a7f8
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ab2078a655062e67c7db8c2fe2be7d5472b31dcf
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53854318"
---
# <a name="idebugcanstopevent2canstop"></a>IDebugCanStopEvent2::CanStop
Hata ayıklama altyapısı (DE) geçerli kod konumda durdurma veya yalnızca yürütme devam gerekip gerekmediğini size bildirir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CanStop (   
   BOOL fCanStop  
);  
```  
  
```csharp  
int CanStop (   
   int fCanStop  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `fCanStop`  
 [in] Sıfır olmayan (`TRUE`) DE geçerli kod konumda; durdurmanız gerekir, aksi takdirde, sıfır (`FALSE`).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu olay alıcısı genellikle çağrıları [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md) yöntemi DE istediği durdurmak için nedenini belirlemek için ve çağrıları `IDebugCanStopEvent2::CanStop` uygun yanıtı ile yöntemi.  
  
 DE durursa, durdurma nedenini açıklayan bir olay gönderir. Tarafından temsil edilen bir kullanıcı veya sinyal sonu gönderilir iki olay vardır [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md) arabirimi ve tarafından temsil edilen bir kesme noktası olayının [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md) arabirimi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)   
 [IDebugBreakEvent2](../../../extensibility/debugger/reference/idebugbreakevent2.md)   
 [IDebugBreakpointEvent2](../../../extensibility/debugger/reference/idebugbreakpointevent2.md)   
 [GetReason](../../../extensibility/debugger/reference/idebugcanstopevent2-getreason.md)