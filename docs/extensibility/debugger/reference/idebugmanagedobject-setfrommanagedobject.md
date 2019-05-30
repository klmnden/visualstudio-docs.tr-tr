---
title: IDebugManagedObject::SetFromManagedObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugManagedObject::SetFromManagedObject
helpviewer_keywords:
- IDebugManagedObject::SetFromManagedObject method
ms.assetid: 8700ee8d-2704-4580-bccc-046837a24edd
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: bf82275bf3375098cc8a8bcbeb200846252d2cec
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66349370"
---
# <a name="idebugmanagedobjectsetfrommanagedobject"></a>IDebugManagedObject::SetFromManagedObject
Bir parametre olarak sağlanan değer sınıfının örneğini değer sınıf nesnesini örneğinin değerini ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetFromManagedObject( 
   IUnknown* pManagedObject
);
```

```csharp
int SetFromManagedObject(
   object pManagedObject
);
```

## <a name="parameters"></a>Parametreler
`pManagedObject`\
[in] Yeni değer içeren yönetilen nesneyi temsil eden arabirim.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem tarafından temsil edilen yönetilen nesneyi değiştirmek için kullanılan [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md) nesne.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)