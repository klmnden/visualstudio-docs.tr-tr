---
title: IDebugObject::IsNullReference | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::IsNullReference
helpviewer_keywords:
- IDebugObject::IsNullReference method
ms.assetid: 6dbfcdb0-954f-4486-8fac-7ea8d003e3a9
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 25de5fdde9e0d834b98f09d2f5c9e2444f8a9d0e
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706905"
---
# <a name="idebugobjectisnullreference"></a>IDebugObject::IsNullReference
Bu nesne bir null başvuru olup olmadığını sınar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsNullReference( 
   BOOL* pfIsNull
);
```

```csharp
int IsNullReference(
   out int pfIsNull
);
```

#### <a name="parameters"></a>Parametreler
 `pfIsNull`

 [out] Sıfır olmayan döndürür (`TRUE`) varsa bu nesne bir null başvuru; Aksi takdirde, sıfır döndürür (`FALSE`).

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir null başvuru boş bir nesneye veya nesnenin için atanmadı anlamına gelir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)