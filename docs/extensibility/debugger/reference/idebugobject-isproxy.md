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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: c38e8f9b6774f5b96f4d0243171b7521841b2dee
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66211797"
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

## <a name="parameters"></a>Parametreler
`pfIsProxy`\
[out] `TRUE` saydam proxy; nesne ise, aksi takdirde, `FALSE`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem varsayılan C++ hata ayıklama altyapısı tarafından gerçekleştirilir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)