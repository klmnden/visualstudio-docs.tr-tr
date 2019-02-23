---
title: IDebugArrayObject::GetElements | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugArrayObject::GetElements
helpviewer_keywords:
- IDebugArrayObject::GetElements method
ms.assetid: f6a6262f-5183-46ce-8a45-33ef46088b98
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 611759c8dc184888b14e2ee1cd88be81324dff30
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712339"
---
# <a name="idebugarrayobjectgetelements"></a>IDebugArrayObject::GetElements
Dizinin tüm öğelerinin bir numaralandırıcıyı alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetElements( 
   IEnumDebugObjects** ppEnum
);
```

```csharp
int GetElements(
   out IEnumDebugObjects ppEnum
);
```

#### <a name="parameters"></a>Parametreler
 `ppEnum`

 [out] Döndürür bir [IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md) tüm öğelerini numaralandırma sağlayan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Alternatif olarak, kullanın [GetCount](../../../extensibility/debugger/reference/idebugarrayobject-getcount.md) ve [GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md) öğeler boyunca yineleme yapmak için yöntemleri.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)