---
title: IDebugThread2::Suspend | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::Suspend
helpviewer_keywords:
- IDebugThread2::Suspend
ms.assetid: 1e20be85-aa12-48de-bb83-0bf0976e99ae
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: e45cee0acab5fb2b5165e28895ab9a7dcb3ed9c1
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683668"
---
# <a name="idebugthread2suspend"></a>IDebugThread2::Suspend
Bir iş parçacığını askıya alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Suspend ( 
   DWORD *pdwSuspendCount
);
```

```csharp
HRESULT Suspend ( 
   out uint pdwSuspendCount
);
```

#### <a name="parameters"></a>Parametreler
 `pdwSuspendCount`

 [out] Askıya alma işleminden sonra askıya alma sayımı döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem her çağrı, askıya alma sayımı 0 yukarıda artırır. Bu askıya alma sayımı görüntülenir **iş parçacıkları** hata ayıklama penceresine.

 Bu yöntem her çağrı için olmalıdır bir sonraki çağrı [sürdürme](../../../extensibility/debugger/reference/idebugthread2-resume.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [Resume](../../../extensibility/debugger/reference/idebugthread2-resume.md)