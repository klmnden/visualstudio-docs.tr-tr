---
title: IDebugFunctionObject::CreateObject | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
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
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 5877f43402d2bac8284be8d24d0c94cd2052a313
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66200851"
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

## <a name="parameters"></a>Parametreler
`pConstructor`\
[in] Bir [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) Oluşturucusu oluşturulacak nesne, temsil eden nesne.

`dwArgs`\
[in] Parametre sayısı `pArg` dizisi. Oluşturucuya geçirilen parametrelerin sayısını temsil eder.

`pArg`\
[in] Bir dizi [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) oluşturucuya geçirilen parametreleri temsil eden nesneleri.

`ppObject`\
[out] Döndürür bir `IDebugObject` temsil eden yeni oluşturulan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir sınıf (veya bir oluşturucu gerektiren başka bir karmaşık tür) örneğini temsil eden bir nesne oluşturmak için bu yöntemi çağıran bir parametresi tarafından temsil edilen işlevi için diğer bir deyişle [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.

 Nesne parametresi bir oluşturucu gerektirmiyorsa, çağrı [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)
- [CreateObjectNoConstructor](../../../extensibility/debugger/reference/idebugfunctionobject-createobjectnoconstructor.md)