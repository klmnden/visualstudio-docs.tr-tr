---
title: IDebugBinder3::GetTypeArgumentCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBinder3::GetTypeArgumentCount
helpviewer_keywords:
- IDebugBinder3::GetTypeArgumentCount method
ms.assetid: caf68de6-6f7c-4efd-b803-121347a5032e
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 3ffe64b5977ce57130d2c97720442a4b030c1ac4
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53986186"
---
# <a name="idebugbinder3gettypeargumentcount"></a>IDebugBinder3::GetTypeArgumentCount
Bu yöntem, bu nesneyle ilişkili bağımsız değişken türleri sayısını döndürür.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetTypeArgumentCount(  
   UINT* uCount  
);  
```  
  
```csharp  
int GetTypeArgumentCount(  
   out uint uCount  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `uCount`  
 [out] Bu nesneyle ilişkili bağımsız değişken türleri sayısı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem tarafından döndürülen değer ile kullanmak için bir dizi ayırmak için kullanılan [GetTypeArguments](../../../extensibility/debugger/reference/idebugbinder3-gettypearguments.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugBinder3](../../../extensibility/debugger/reference/idebugbinder3.md)   
 [GetTypeArguments](../../../extensibility/debugger/reference/idebugbinder3-gettypearguments.md)