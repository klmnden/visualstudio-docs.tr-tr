---
title: IEnumDebugBoundBreakpoints2::GetCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IEnumDebugBoundBreakpoints2::GetCount
helpviewer_keywords:
- IEnumDebugBoundBreakpoints2::GetCount
ms.assetid: 5a572eeb-beb7-4fc7-8259-792d277069be
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 38ad4f947577d24e62ba50e530e783c5fc5ecc98
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56682728"
---
# <a name="ienumdebugboundbreakpoints2getcount"></a>IEnumDebugBoundBreakpoints2::GetCount
Numaralandırmada öğelerin sayısını döndürür.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetCount(
   ULONG* pcelt
);
```

```csharp
int GetCount(
   out uint pcelt
);
```

#### <a name="parameters"></a>Parametreler
 `pcelt`

 [out] Numaralandırmada öğelerin sayısını döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem yalnızca belirten geleneksel COM numaralandırma arabiriminin bir parçası değil `Next`, `Clone`, `Skip`, ve `Reset` yöntemleri uygulanması gerekir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IEnumDebugBoundBreakpoints2](../../../extensibility/debugger/reference/ienumdebugboundbreakpoints2.md)