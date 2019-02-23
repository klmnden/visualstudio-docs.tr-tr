---
title: IDebugBinder::Bind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBinder::Bind
helpviewer_keywords:
- IDebugBinder::Bind method
ms.assetid: 15a11ad7-0fcc-4e80-ae34-8a7dd7bae3c3
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: bcb3535a2ace5818664a34a5d7b818d7dfd8b025
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56704949"
---
# <a name="idebugbinderbind"></a>IDebugBinder::Bind
Bu yöntem, bellek bağlamı veya sembolün geçerli değerini içeren nesneyi alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT Bind( 
   IDebugObject*  pContainer,
   IDebugField*   pField,
   IDebugObject** ppObject
);
```

```csharp
int Bind(
   IDebugObject     pContainer,
   IDebugField      pField,
   out IDebugObject ppObject
);
```

#### <a name="parameters"></a>Parametreler
 `pContainer`

 [in] [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) tarafından başvurulan alt içeren `pField`.

 `pField`

 [in] [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) temsil eden bir simge.

 `ppObject`

 [out] Döndürür `IDebugObject` sembol örneğini temsil eden.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)