---
title: IDebugPendingBreakpoint2::Bind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugPendingBreakpoint2::Bind
helpviewer_keywords:
- Bind method
- IDebugPendingBreakpoint2::Bind method
ms.assetid: 46e3f307-219d-40cd-a929-d41399c60ecf
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ea73240d6797daaee2cb51796800282bf5b60008
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54933769"
---
# <a name="idebugpendingbreakpoint2bind"></a>IDebugPendingBreakpoint2::Bind
Bu bekleyen kesme noktasının bir veya daha fazla kod konumlara bağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Bind(   
   void   
);  
```  
  
```csharp  
int Bind();  
```  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_BP_DELETED` kesme noktası silinmiş olması durumunda.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem çağrıldığında bu bekleyen kesme noktasının eşleşen tüm kod konumlara bağlamak hata ayıklama altyapısı (DE) denemelidir.  
  
 Çağıranın bu yöntemin dönüşünün ardından çağrılar bekleyen kesme noktasının bağlı veya varsayılarak önce hata olduğunu gösteren olaylar için beklemesi gereken [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md) veya [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md).methods numaralandırır tüm bağımlı veya hata kesme noktaları, sırasıyla.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugPendingBreakpoint2](../../../extensibility/debugger/reference/idebugpendingbreakpoint2.md)   
 [IDebugBreakpointBoundEvent2](../../../extensibility/debugger/reference/idebugbreakpointboundevent2.md)   
 [IDebugBreakpointErrorEvent2](../../../extensibility/debugger/reference/idebugbreakpointerrorevent2.md)   
 [EnumBoundBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumboundbreakpoints.md)   
 [EnumErrorBreakpoints](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-enumerrorbreakpoints.md)