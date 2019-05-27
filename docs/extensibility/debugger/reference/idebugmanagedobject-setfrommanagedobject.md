---
title: IDebugManagedObject::SetFromManagedObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugManagedObject::SetFromManagedObject
helpviewer_keywords:
- IDebugManagedObject::SetFromManagedObject method
ms.assetid: 8700ee8d-2704-4580-bccc-046837a24edd
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: dbaaf27222754d4a68d7de6367a2c0d7a1a8be73
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66210624"
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