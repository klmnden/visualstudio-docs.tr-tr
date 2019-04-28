---
title: IDebugThread2::Resume | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::Resume
helpviewer_keywords:
- IDebugThread2::Resume
ms.assetid: 36aad682-b0b9-40a2-b3fc-f0e61d41cdbc
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4997b8c711a67a3bb45529627e81e70b786acf00
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62915515"
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
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [Suspend](../../../extensibility/debugger/reference/idebugthread2-suspend.md)