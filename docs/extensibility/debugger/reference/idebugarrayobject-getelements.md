---
title: IDebugArrayObject::GetElements | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugArrayObject::GetElements
helpviewer_keywords:
- IDebugArrayObject::GetElements method
ms.assetid: f6a6262f-5183-46ce-8a45-33ef46088b98
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: ec7d2a12360ef41d982fa0f6459ee3533c026358
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53849436"
---
# <a name="idebugarrayobjectgetelements"></a>IDebugArrayObject::GetElements
Dizinin tüm öğelerinin bir numaralandırıcıyı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetElements(   
   IEnumDebugObjects** ppEnum  
);  
```  
  
```csharp  
int GetElements(  
   out IEnumDebugObjects ppEnum  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnum`  
 [out] Döndürür bir [IEnumDebugObjects](../../../extensibility/debugger/reference/ienumdebugobjects.md) tüm öğelerini numaralandırma sağlayan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Alternatif olarak, kullanın [GetCount](../../../extensibility/debugger/reference/idebugarrayobject-getcount.md) ve [GetElement](../../../extensibility/debugger/reference/idebugarrayobject-getelement.md) öğeler boyunca yineleme yapmak için yöntemleri.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)