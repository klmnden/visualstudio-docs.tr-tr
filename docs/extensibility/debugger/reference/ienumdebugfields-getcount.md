---
title: IEnumDebugFields::GetCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugFields::GetCount
helpviewer_keywords:
- IEnumDebugFields::GetCount method
ms.assetid: 3f471b40-4db3-49f7-b504-58b2476eef74
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 2459275854f0df2b58b4f88a0828ee86953d1a19
ms.sourcegitcommit: 19ec963ed6d585719cb83ba677434ea6580e0d1f
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/24/2019
ms.locfileid: "66208080"
---
# <a name="ienumdebugfieldsgetcount"></a>IEnumDebugFields::GetCount
Bu yöntem numaralandırmada öğelerin sayısını döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetCount(
   [out] ULONG* pcelt
);
```

```csharp
int GetCount(
   out uint pcelt
);
```

## <a name="parameters"></a>Parametreler
`pcelt`\
[out] Numaralandırmada öğelerin sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem yalnızca ileri, kopyalama, atlama ve sıfırlama uygulanması gerektiğini belirten geleneksel COM numaralandırma arabiriminin bir parçası değil.

## <a name="see-also"></a>Ayrıca bkz.
- [IEnumDebugFields](../../../extensibility/debugger/reference/ienumdebugfields.md)