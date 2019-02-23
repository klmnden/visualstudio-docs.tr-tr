---
title: IDebugProgram2::EnumThreads | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgram2::EnumThreads
helpviewer_keywords:
- IDebugProgram2::EnumThreads
ms.assetid: 0f2a8c51-1315-4c96-8aa1-6a937dc2a769
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 9b261ca6973d938f8530ea75788d6ba6779ea9f0
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56690012"
---
# <a name="idebugprogram2enumthreads"></a>IDebugProgram2::EnumThreads
Bir programda çalışan iş parçacıklarının listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT EnumThreads( 
   IEnumDebugThreads2** ppEnum
);
```

```csharp
int EnumThreads( 
   out IEnumDebugThreads2 ppEnum
);
```

#### <a name="parameters"></a>Parametreler
 `ppEnum`

 [out] Döndürür bir [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md) iş parçacıklarının listesini içeren nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProgram2](../../../extensibility/debugger/reference/idebugprogram2.md)
- [IEnumDebugThreads2](../../../extensibility/debugger/reference/ienumdebugthreads2.md)
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)