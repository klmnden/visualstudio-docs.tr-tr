---
title: IDebugProperty2::GetDerivedMostProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugProperty2::GetDerivedMostProperty
helpviewer_keywords:
- IDebugProperty2::GetDerivedMostProperty
ms.assetid: cc86b461-62d1-4340-8209-c65037fd8b02
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 2c2a895e73393739fc2aa6c44d809647c9ccbb3b
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53988141"
---
# <a name="idebugproperty2getderivedmostproperty"></a>IDebugProperty2::GetDerivedMostProperty
Bir özelliğin türetilmiş çoğu özelliği alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetDerivedMostProperty (   
   IDebugProperty2** ppDerivedMost  
);  
```  
  
```csharp  
int GetDerivedMostProperty (   
   out IDebugProperty2 ppDerivedMost  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppDerivedMost`  
 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) türetilmiş çoğu özelliği temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür. Döndürür `S_GETDERIVEDMOST_NO_DERIVED_MOST` almak için türetilmiş çoğu özelliği yok ise.  
  
## <a name="remarks"></a>Açıklamalar  
 Örneğin, bu özelliği uygulayan bir nesne tanımlar `ClassRoot` ancak aslında örneklemesi olduğu `ClassDerived` sınıfından türetilen `ClassRoot`, sonra da bu yöntemi döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) nesnesi açıklayan `ClassDerived` nesne.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)