---
title: IDebugBinder::ResolveRuntimeType | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBinder::ResolveRuntimeType
helpviewer_keywords:
- IDebugBinder::ResolveRuntimeType method
ms.assetid: 6456ab3e-1c03-4f3c-91f9-16797ab7f5e7
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: f9224314d1417f08bbf025d774c1ecc8ac706e05
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53852524"
---
# <a name="idebugbinderresolveruntimetype"></a>IDebugBinder::ResolveRuntimeType
Bu yöntem, bir nesnenin çalışma zamanı türünü belirler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT ResolveRuntimeType(   
   IDebugObject* pObject,  
   IDebugField** ppResolved  
);  
```  
  
```csharp  
int ResolveRuntimeType(  
   IDebugObject     pObject,   
   out IDebugField  ppResolved  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pObject`  
 [in] [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) çözümlenecek.  
  
 `ppResolved`  
 [out] Olarak nesne türünü döndüren bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md).  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir nesnenin çalışma zamanı türü derleme zamanında her zaman bilinmiyor. Örneğin, çok biçimlilik kullanarak, bağımsız değişken bir işleve bir button sınıfı gibi temel sınıf olarak geçirilebilir. Gerçek bağımsız değişken bir radyo düğmesi sınıfı gibi türetilmiş bir sınıf olabilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugBinder](../../../extensibility/debugger/reference/idebugbinder.md)   
 [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)   
 [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)