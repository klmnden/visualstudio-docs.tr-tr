---
title: IDebugCanStopEvent2::GetReason | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCanStopEvent2::GetReason
helpviewer_keywords:
- IDebugCanStopEvent2::GetReason
ms.assetid: f5de31ca-7b8d-4029-9cf9-ba860ac66af6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: b6b58e1a7a1f3595084a92f8db41d13875e47c0d
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55041782"
---
# <a name="idebugcanstopevent2getreason"></a>IDebugCanStopEvent2::GetReason
Hata ayıklama altyapısı (DE) neden durdurmak ister nedenini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetReason(   
   CANSTOP_REASON* pcr  
);  
```  
  
```csharp  
int GetReason(   
   out enum_CANSTOP_REASON pcr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pcr`  
 [out] Bir değer döndürür [CANSTOP_REASON](../../../extensibility/debugger/reference/canstop-reason.md) bu olay nedenini açıklayan sabit listesi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem genellikle önce çağrılır [CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md) çağıranın'ın sıfır olmayan geçirmek verilip verilmeyeceğini belirlemek için yöntemi (`TRUE`) için `IDebugCanStopEvent2::CanStop` yöntemi.  
  
 Durdurma nedeni olabilir `CANSTOP_ENTRYPOINT`, DE başka bir deyişle, bir giriş noktası sınırına veya `CANSTOP_STEPIN`, bir işleve kalkan DE anlamına gelir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)   
 [CANSTOP_REASON](../../../extensibility/debugger/reference/canstop-reason.md)   
 [CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md)