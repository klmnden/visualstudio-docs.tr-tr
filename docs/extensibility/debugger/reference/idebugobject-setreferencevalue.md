---
title: IDebugObject::SetReferenceValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugObject::SetReferenceValue
helpviewer_keywords:
- IDebugObject::SetReferenceValue method
ms.assetid: 08c78a4e-98eb-41cb-8b75-02a6a43d49f7
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 7e861a67ada36bd25b30e08bf8a62163bceea979
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66211307"
---
# <a name="idebugobjectsetreferencevalue"></a>IDebugObject::SetReferenceValue
Bu nesne başvuru değeri ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetReferenceValue( 
   IDebugObject* pObject
);
```

```csharp
int SetReferenceValue(
   [In] IDebugObject pObject
);
```

## <a name="parameters"></a>Parametreler
`pObject`\
[in] Bir [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) yeni başvuru değeri temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem bu sağlar [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md) verilen nesnenin değeri başvuru nesnesi `pObject` herhangi bir önceki başvurusu atmak parametresi. Not Bu `IDebugObject` nesne zaten bir başvuru türü olmalıdır.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugObject](../../../extensibility/debugger/reference/idebugobject.md)
- [GetValue](../../../extensibility/debugger/reference/idebugobject-getvalue.md)