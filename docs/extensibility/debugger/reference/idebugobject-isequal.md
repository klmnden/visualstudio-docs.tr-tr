---
title: IDebugObject::IsEqual | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::IsEqual
helpviewer_keywords:
- IDebugObject::IsEqual method
ms.assetid: 4b76e663-ef2e-41ff-9be1-bf26d666a34a
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 527d0bf7dcc7841516c3ae620130aa346841d0a1
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66202860"
---
# <a name="idebugobjectisequal"></a>IDebugObject::IsEqual
Bu nesne bir nesneyle karşılaştırır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsEqual( 
   IDebugObject* pObject,
   BOOL*         pfIsEqual
);
```

```csharp
int IsEqual(
   IDebugObject pObject,
   out int      pfIsEqual
);
```

## <a name="parameters"></a>Parametreler
`pObject`\
[in] Bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) karşılaştırma yapılacak nesne temsil eden nesne.

`pfIsEqual`\
[out] Sıfır olmayan döndürür (`TRUE`) nesnelerin değerler, eşit; Aksi takdirde, sıfır döndürür (`FALSE`).

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Genellikle, bu yöntem tarafından temsil edilen değerleri adresleri karşılaştırabilirsiniz `pObject` parametresi ve bu [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne; adresleri eşitse sonra nesneler eşit kabul edilebilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)