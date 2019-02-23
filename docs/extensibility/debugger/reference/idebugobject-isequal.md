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
ms.openlocfilehash: 49d909dc0896bcc1b130ce908699c04ad9543c73
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56691117"
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

#### <a name="parameters"></a>Parametreler
 `pObject`

 [in] Bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) karşılaştırma yapılacak nesne temsil eden nesne.

 `pfIsEqual`

 [out] Sıfır olmayan döndürür (`TRUE`) nesnelerin değerler, eşit; Aksi takdirde, sıfır döndürür (`FALSE`).

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Genellikle, bu yöntem tarafından temsil edilen değerleri adresleri karşılaştırabilirsiniz `pObject` parametresi ve bu [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne; adresleri eşitse sonra nesneler eşit kabul edilebilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)