---
title: IDebugThread2::GetLogicalThread | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::GetLogicalThread
helpviewer_keywords:
- IDebugThread2::GetLogicalThread
ms.assetid: bce6230e-41d4-49b7-a050-2dde5efb6805
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 1e8c1543383b3d0df0166b50359caf0f80a8b3ef
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66320233"
---
# <a name="idebugthread2getlogicalthread"></a>IDebugThread2::GetLogicalThread
Hata ayıklama altyapısı, bu yöntemi uygulaması değil.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetLogicalThread( 
   IDebugStackFrame2*     pStackFrame,
   IDebugLogicalThread2** ppLogicalThread
);
```

```csharp
int GetLogicalThread( 
   IDebugStackFrame2        pStackFrame,
   out IDebugLogicalThread2 ppLogicalThread
);
```

## <a name="parameters"></a>Parametreler
`pStackFrame`\
[in] Bir [IDebugStackFrame2](../../../extensibility/debugger/reference/idebugstackframe2.md) yığın çerçevesini temsil eden nesne.

`ppLogicalThread`\
[out] Döndürür bir `IDebugLogicalThread2` ilişkili mantıksal iş parçacığını temsil eden arabirim. Hata ayıklama altyapısı uygulama bu null bir değere ayarlamanız gerekir.

## <a name="return-value"></a>Dönüş Değeri
 Hata ayıklama altyapısı uygulamaları her zaman dönüş `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)