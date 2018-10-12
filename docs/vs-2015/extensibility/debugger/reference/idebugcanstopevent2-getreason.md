---
title: IDebugCanStopEvent2::GetReason | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugCanStopEvent2::GetReason
helpviewer_keywords:
- IDebugCanStopEvent2::GetReason
ms.assetid: f5de31ca-7b8d-4029-9cf9-ba860ac66af6
caps.latest.revision: 12
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: c94a54f93cd9e7eb62e2b7cd1ff8aa8f17cd3cdd
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49302685"
---
# <a name="idebugcanstopevent2getreason"></a>IDebugCanStopEvent2::GetReason
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Hata ayıklama altyapısı (DE) neden durdurmak ister nedenini alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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

