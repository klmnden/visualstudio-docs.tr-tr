---
title: IDebugFunctionObject::CreateObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugFunctionObject::CreateObject
helpviewer_keywords:
- IDebugFunctionObject::CreateObject method
ms.assetid: c4c99dd5-609a-4e7c-8f29-eb728f57e995
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 94ee856f3f1b514fb4d6cb11c448edd102038953
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55031701"
---
# <a name="idebugfunctionobjectcreateobject"></a>IDebugFunctionObject::CreateObject
Bir oluşturucu kullanılarak bir nesne oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT CreateObject(   
   IDebugFunctionObject* pConstructor,  
   DWORD                 dwArgs,  
   IDebugObject*         pArgs[],  
   IDebugObject**        ppObject  
);  
```  
  
```csharp  
int CreateObject(  
   IDebugFunctionObject pConstructor,   
   uint                 dwArgs,   
   IDebugObject[]       pArgs,   
   out IDebugObject     ppObject  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pConstructor`  
 [in] Bir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) Oluşturucusu oluşturulacak nesne, temsil eden nesne.  
  
 `dwArgs`  
 [in] Parametre sayısı `pArg` dizisi. Oluşturucuya geçirilen parametrelerin sayısını temsil eder.  
  
 `pArg`  
 [in] Bir dizi [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) oluşturucuya geçirilen parametreleri temsil eden nesneleri.  
  
 `ppObject`  
 [out] Döndürür bir `IDebugObject` temsil eden yeni oluşturulan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bir sınıf (veya bir oluşturucu gerektiren başka bir karmaşık tür) örneğini temsil eden bir nesne oluşturmak için bu yöntemi çağıran bir parametresi tarafından temsil edilen işlevi için diğer bir deyişle [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.  
  
 Nesne parametresi bir oluşturucu gerektirmiyorsa, çağrı [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)   
 [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)