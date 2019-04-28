---
title: IDebugArrayObject2::GetBaseIndices | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- GetBaseIndices
- IDebugArrayObject2::GetBaseIndices
ms.assetid: 882951a2-3da0-49bf-8d1e-7daedd13ffe6
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 5355e85007c04e523efa4030ca0603a01cf88c68
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62923773"
---
# <a name="idebugarrayobject2getbaseindices"></a>IDebugArrayObject2::GetBaseIndices
Dizideki boyutların sayısı verilen her dizin için temel dizin (alt sınırı) alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetBaseIndices (
   DWORD  dwRank,
   DWORD* dwIndices
);
```

```csharp
int GetBaseIndices (
   uint       dwRank,
   out uint[] dwIndices
);
```

#### <a name="parameters"></a>Parametreler
 `dwRank`

 [in] Dizi boyutları (derece) sayısı.

 `dwIndices`

 [out] Dizi için temel dizin (alt sınırı).

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bir örnek olarak, aşağıdaki tarafından oluşturulan dizisi için '5' Bu işlev döndürecekti C# kod:

```
int[] lengths = { 12 };
int[] lowerbounds = { 5 };
Array.CreateInstance(typeof(int), lengths, lowerbounds);
```

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugArrayObject2](../../../extensibility/debugger/reference/idebugarrayobject2.md)