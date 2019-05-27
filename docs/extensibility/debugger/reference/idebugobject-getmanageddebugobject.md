---
title: IDebugObject::GetManagedDebugObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::GetManagedDebugObject
helpviewer_keywords:
- IDebugObject::GetManagedDebugObject method
ms.assetid: cb89692e-7657-47ff-846d-311943521951
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: b0721e8f8a30a8736f6d52ea61e02b9a93821a98
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66203007"
---
# <a name="idebugobjectgetmanageddebugobject"></a>IDebugObject::GetManagedDebugObject
Hata ayıklama altyapısı adres alanında yönetilen nesnesinin bir kopyasını oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetManagedDebugObject( 
   IDebugManagedObject** ppObject
);
```

```csharp
int GetManagedDebugObject(
   out IDebugManagedObject ppObject
);
```

## <a name="parameters"></a>Parametreler
`ppObject`\
[out] Döndürür bir [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md) yeni oluşturulan yönetilen nesneyi temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür. Bu E_FAIL döndürür [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) yönetilen değeri sınıfı örneğini temsil etmiyor.

## <a name="remarks"></a>Açıklamalar
 Bu [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne gerekir temsil eden bir yönetilen değeri sınıf örneği gibi bir `System.Decimal` örneği. Yerel bir kopya arama getirdiği ek yüke sahip [değerlendir](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md) ortadan kalkar.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)