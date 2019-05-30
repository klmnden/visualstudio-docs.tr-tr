---
title: IEnumDebugObjects::Reset | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugObjects::Reset
helpviewer_keywords:
- IEnumDebugObjects::Reset method
ms.assetid: 4a245e47-cc39-4177-b83d-083ea0e3190f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: c5a9e8e08c19e7d4f2a8b47ad0124115743522a8
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66339545"
---
# <a name="ienumdebugobjectsreset"></a>IEnumDebugObjects::Reset
Bu yöntem, ilk öğe için sabit sıfırlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Reset(void);
```

```csharp
int Reset();
```

## <a name="parameters"></a>Parametreler
 Yok.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem çağrıldığında sonra yapılan sonraki çağrıda [sonraki](../../../extensibility/debugger/reference/ienumdebugobjects-next.md) numaralandırma ilk öğeyi döndürür.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md)
- [Next](../../../extensibility/debugger/reference/ienumdebugobjects-next.md)