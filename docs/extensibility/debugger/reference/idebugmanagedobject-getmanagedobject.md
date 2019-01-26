---
title: IDebugManagedObject::GetManagedObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugManagedObject::GetManagedObject
helpviewer_keywords:
- IDebugManagedObject::GetManagedObject method
ms.assetid: 6abe1402-6aad-41e6-8ec1-ae12d5945992
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2be150d3ce1103f8f47438af7ac8fcfcba8519da
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54922918"
---
# <a name="idebugmanagedobjectgetmanagedobject"></a>IDebugManagedObject::GetManagedObject
Yönetilen nesneyi temsil eden bir arabirim döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetManagedObject(   
   IUnknown** ppManagedObject  
);  
```  
  
```cpp  
int GetManagedObject(  
   out object ppManagedObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppManagedObject`  
 [out] Yönetilen nesneyi temsil eden bir arabirim döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntemin döndürdüğü arabirimi yöntemlerinin çağrılması izin verme yönetilen sınıfı tarafından uygulanan herhangi bir arabirim için sorgulanabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugManagedObject](../../../extensibility/debugger/reference/idebugmanagedobject.md)