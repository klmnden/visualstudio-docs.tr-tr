---
title: IDebugCustomAttribute::GetName | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugCustomAttribute::GetName
helpviewer_keywords:
- IDebugCustomAttribute::GetName
ms.assetid: ba509cc5-5816-4925-a094-4c72d88c360c
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 753964c19c27709af1adf7b38e92555a46559776
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53944703"
---
# <a name="idebugcustomattributegetname"></a>IDebugCustomAttribute::GetName
Özel özniteliğin adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT GetName(   
   BSTR* bstrName  
);  
```  
  
```csharp  
int GetName(  
   out string bstrName  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `bstrName`  
 [out] Özel özniteliğin adını içeren bir dize döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem tarafından döndürülen adlandırılmış bir öznitelik bildirmek için kullanılan sınıf adına karşılık gelir. C# bir bildiriminde kullanıldığında bir özel öznitelik adı kesilmesini "Özniteliği" soneki sağladığından, bu tam olarak bir özel öznitelik sınıfı adını karşılık gelebilir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugCustomAttribute](../../../extensibility/debugger/reference/idebugcustomattribute.md)