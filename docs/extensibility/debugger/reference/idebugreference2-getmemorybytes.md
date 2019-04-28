---
title: IDebugReference2::GetMemoryBytes | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReference2::GetMemoryBytes
helpviewer_keywords:
- IDebugReference2::GetMemoryBytes
ms.assetid: 2006cb2b-1dfa-4a2d-8e3e-db2ce0302e0d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 20e08fdd59bd519358342c9cb8abbc1516d8637e
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62916392"
---
# <a name="idebugreference2getmemorybytes"></a>IDebugReference2::GetMemoryBytes
Fiziksel olarak bir başvuru değeri içeren bellek bayt alır. Daha sonraki kullanımlar için ayrılmıştır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetMemoryBytes ( 
   IDebugMemoryBytes2** ppMemoryBytes
);
```

```csharp
int GetMemoryBytes ( 
   out IDebugMemoryBytes2 ppMemoryBytes
);
```

#### <a name="parameters"></a>Parametreler
 `ppMemoryBytes`

 [out] Döndürür bir [IDebugMemoryBytes2](../../../extensibility/debugger/reference/idebugmemorybytes2.md) başvuru değeri içeren belleği almak için kullanılan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Her zaman döndürür `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)
- [IDebugMemoryBytes2](../../../extensibility/debugger/reference/idebugmemorybytes2.md)