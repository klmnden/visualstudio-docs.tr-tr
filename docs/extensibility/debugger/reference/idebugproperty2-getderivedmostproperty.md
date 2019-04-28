---
title: IDebugProperty2::GetDerivedMostProperty | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProperty2::GetDerivedMostProperty
helpviewer_keywords:
- IDebugProperty2::GetDerivedMostProperty
ms.assetid: cc86b461-62d1-4340-8209-c65037fd8b02
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1227cb697dc78a8833e304d775fb4b1af85a2a69
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62916638"
---
# <a name="idebugproperty2getderivedmostproperty"></a>IDebugProperty2::GetDerivedMostProperty
Bir özelliğin türetilmiş çoğu özelliği alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetDerivedMostProperty ( 
   IDebugProperty2** ppDerivedMost
);
```

```csharp
int GetDerivedMostProperty ( 
   out IDebugProperty2 ppDerivedMost
);
```

#### <a name="parameters"></a>Parametreler
 `ppDerivedMost`

 [out] Döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) türetilmiş çoğu özelliği temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde hata kodu döndürür. Döndürür `S_GETDERIVEDMOST_NO_DERIVED_MOST` almak için türetilmiş çoğu özelliği yok ise.

## <a name="remarks"></a>Açıklamalar
 Örneğin, bu özelliği uygulayan bir nesne tanımlar `ClassRoot` ancak aslında örneklemesi olduğu `ClassDerived` sınıfından türetilen `ClassRoot`, sonra da bu yöntemi döndürür bir [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) nesnesi açıklayan `ClassDerived` nesne.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)