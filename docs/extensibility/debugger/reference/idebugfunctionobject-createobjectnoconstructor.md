---
title: IDebugFunctionObject::CreateObjectNoConstructor | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor
helpviewer_keywords:
- IDebugFunctionObject::CreateObjectNoConstructor method
ms.assetid: 4e2bd6d5-f4bd-4c10-a998-3db451c9a0c8
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 9e6225099b3b88cbbbb73884cbd93be4f7976e50
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66200833"
---
# <a name="idebugfunctionobjectcreateobjectnoconstructor"></a>IDebugFunctionObject::CreateObjectNoConstructor
Bir nesne ile hiçbir oluşturucu oluşturur.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT CreateObjectNoConstructor( 
   IDebugField*   pClassObject,
   IDebugObject** ppObject
);
```

```csharp
int CreateObjectNoConstructor(
   IDebugField      pClassField,
   out IDebugObject ppObject
);
```

## <a name="parameters"></a>Parametreler
`pClassObject`\
[in] Bir [IDebugField](../../../extensibility/debugger/reference/idebugfield.md) oluşturulacak nesne türünü temsil eden nesne.

`ppObject`\
[out] Döndürür bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) temsil eden yeni oluşturulan nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir yapı veya, tarafından temsil edilen bir işlev parametresi olan (yani bir oluşturucu gerektirmez) karmaşık türün bir örneği temsil eden bir nesne oluşturmak için bu yöntemi çağırın [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md) arabirimi.

 Nesne parametresi bir oluşturucu gerektiriyorsa, çağrı [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md) yöntemi.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugField](../../../extensibility/debugger/reference/idebugfield.md)
- [IDebugFunctionObject](../../../extensibility/debugger/reference/idebugfunctionobject.md)
- [CreateObject](../../../extensibility/debugger/reference/idebugfunctionobject-createobject.md)