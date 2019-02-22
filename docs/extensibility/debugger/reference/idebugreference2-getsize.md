---
title: IDebugReference2::GetSize | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReference2::GetSize
helpviewer_keywords:
- IDebugReference2::GetSize
ms.assetid: a404ddd9-d940-4513-97cd-f52b8ab6a560
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 681cede68a2d649cd9f072b6c10e8476a9625f6e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56683434"
---
# <a name="idebugreference2getsize"></a>IDebugReference2::GetSize
Başvuru değeri bayt cinsinden boyutunu alır. Daha sonraki kullanımlar için ayrılmıştır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetSize ( 
   DWORD* pdwSize
);
```

```csharp
int GetSize ( 
   out uint pdwSize
);
```

#### <a name="parameters"></a>Parametreler
 `pdwSize`

 [out] Başvuru değeri bayt cinsinden boyutunu döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Her zaman döndürür `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)