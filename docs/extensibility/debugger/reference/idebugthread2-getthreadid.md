---
title: IDebugThread2::GetThreadId | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::GetThreadId
helpviewer_keywords:
- IDebugThread2::GetThreadId
ms.assetid: db8b1c07-6b86-47f9-b292-bac19c276d36
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 85dd439729763b594076e4fab076a213c10f5a46
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56702089"
---
# <a name="idebugthread2getthreadid"></a>IDebugThread2::GetThreadId
Sistem iş parçacığı tanımlayıcısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetThreadId (
    DWORD* pdwThreadId
);
```

```csharp
int GetThreadId (
    out uint pdwThreadId
);
```

#### <a name="parameters"></a>Parametreler
`pdwThreadId`

 [out] Sistem iş parçacığı tanıtıcısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Bir iş parçacığı kimliği bir iş parçacığı bir işlemdeki diğer iş parçacıkları arasında tanımlamak için kullanılır.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CProgram` uygulayan nesne [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) arabirimi.

```cpp
HRESULT CProgram::GetThreadId(DWORD* pdwThreadId) {
    *pdwThreadId = GetCurrentThreadId();
    return NOERROR;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
