---
title: IDebugObject::IsProxy | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugObject::IsProxy
- IsProxy
ms.assetid: 06c66b87-db95-4400-ab26-5d33e743a439
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 037245524446ded2ec250f1d4a04e21bf5924a61
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56678429"
---
# <a name="idebugobjectisproxy"></a>IDebugObject::IsProxy
Nesnenin saydam bir ara sunucu olup olmadığını belirler.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT IsProxy (
   BOOL* pfIsProxy
);
```

```csharp
int IsProxy (
   out bool pfIsProxy
);
```

#### <a name="parameters"></a>Parametreler
 `pfIsProxy`

 [out] `TRUE` saydam proxy; nesne ise, aksi takdirde, `FALSE`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem varsayılan C++ hata ayıklama altyapısı tarafından gerçekleştirilir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)