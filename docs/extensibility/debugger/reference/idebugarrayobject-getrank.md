---
title: IDebugArrayObject::GetRank | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugArrayObject::GetRank
helpviewer_keywords:
- IDebugArrayObject::GetRank method
ms.assetid: 9948551a-e334-4ff6-979c-08dab633b9b6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: a0391030e77e5959fdc28c94f63e099e5c505d77
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62923734"
---
# <a name="idebugarrayobjectgetrank"></a>IDebugArrayObject::GetRank
Dizi boyut sayısını, diğer bir deyişle, boyut sayısını alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetRank( 
   DWORD* pdwRank
);
```

```csharp
int GetRank(
   out uint pdwRank
);
```

#### <a name="parameters"></a>Parametreler
 `pdwRank`

 [out] Derecesini döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılıysa S_OK döndürür; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Kullanım [GetDimensions](../../../extensibility/debugger/reference/idebugarrayobject-getdimensions.md) dizi nesnesinin her boyutunun boyutunu almak için yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)