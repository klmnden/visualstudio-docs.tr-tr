---
title: IDebugObject::GetManagedDebugObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: 99aa9d4934b6d33890fb69c0564c16ec0706b924
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55007769"
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
  
#### <a name="parameters"></a>Parametreler  
 `ppObject`  
 [out] Döndürür bir [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md) yeni oluşturulan yönetilen nesneyi temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür. Bu E_FAIL döndürür [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) yönetilen değeri sınıfı örneğini temsil etmiyor.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) nesne gerekir temsil eden bir yönetilen değeri sınıf örneği gibi bir `System.Decimal` örneği. Yerel bir kopya arama getirdiği ek yüke sahip [değerlendir](../../../extensibility/debugger/reference/idebugfunctionobject-evaluate.md) ortadan kalkar.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)   
 [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)