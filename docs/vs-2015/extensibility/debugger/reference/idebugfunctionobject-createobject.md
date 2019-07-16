---
title: IDebugFunctionObject::CreateObject | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-sdk
ms.topic: reference
f1_keywords:
- IDebugFunctionObject::CreateObject
helpviewer_keywords:
- IDebugFunctionObject::CreateObject method
ms.assetid: c4c99dd5-609a-4e7c-8f29-eb728f57e995
caps.latest.revision: 10
ms.author: gregvanl
manager: jillfra
ms.openlocfilehash: 08483d5f015af7088eb5968a5bf6358ce5065579
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68179468"
---
# <a name="idebugfunctionobjectcreateobject"></a>IDebugFunctionObject::CreateObject
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Bir oluşturucu kullanılarak bir nesne oluşturur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
