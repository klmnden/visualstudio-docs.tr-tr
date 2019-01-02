---
title: IDebugThread2::Resume | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugThread2::Resume
helpviewer_keywords:
- IDebugThread2::Resume
ms.assetid: 36aad682-b0b9-40a2-b3fc-f0e61d41cdbc
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: bad2daaa21607194504923db8e896237298c75d5
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53824593"
---
# <a name="idebugthread2resume"></a>IDebugThread2::Resume
Bir iş parçacığının yürütülmesini sürdürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT Resume (   
   DWORD *pdwSuspendCount  
);  
```  
  
```csharp  
int Resume (   
   out uint pdwSuspendCount  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pdwSuspendCount`  
 [out] Sonra devam et işlemi askıya alma sayımı döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Askıya alma sayımı her çağrı için bu yöntemi azaltır zaman 0 ulaşana kadar yürütme gerçekten sürdürülür. Bu askıya alma sayımı görüntülenir **iş parçacıkları** hata ayıklama penceresine.  
  
 Bu yöntem her çağrı için olmalıdır önceki bir çağrı [askıya alma](../../../extensibility/debugger/reference/idebugthread2-suspend.md) yöntemi. Askıya alma sayımı kaç kez belirler `IDebugThread2::Suspend` yönteminin çağrılıp çağrılmadığını kadar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)   
 [Suspend](../../../extensibility/debugger/reference/idebugthread2-suspend.md)