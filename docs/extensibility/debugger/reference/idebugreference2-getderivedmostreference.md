---
title: IDebugReference2::GetDerivedMostReference | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReference2::GetDerivedMostReference
helpviewer_keywords:
- IDebugReference2::GetDerivedMostReference
ms.assetid: 07253b74-7d39-48e0-8e85-ac8dfd919f6e
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 4b9534c144ae08a6fa5791518fea7d463819140b
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66212951"
---
# <a name="idebugreference2getderivedmostreference"></a>IDebugReference2::GetDerivedMostReference
Bir başvuru türetilmiş çoğu referansını alır. Daha sonraki kullanımlar için ayrılmıştır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDerivedMostReference( 
   IDebugReference2** ppDerivedMost
);
```

```csharp
int GetDerivedMostReference( 
   out IDebugReference2 ppDerivedMost
);
```

## <a name="parameters"></a>Parametreler
`ppDerivedMost`\
[out] Döndürür bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) türetilmiş çoğu özelliği temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Her zaman döndürür `E_NOTIMPL`.

## <a name="remarks"></a>Açıklamalar
 Örneğin, bu özelliği uygulayan bir nesne tanımlar `ClassRoot` ancak aslında örneklemesi olduğu `ClassDerived` sınıfından türetilen `ClassRoot`, sonra da bu yöntemi döndürür bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) nesnesi başvuruyu temsil eden `ClassDerived` nesne.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)