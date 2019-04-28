---
title: IDebugBoundBreakpoint2::SetHitCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBoundBreakpoint2::SetHitCount
helpviewer_keywords:
- SetHitCount method
- IDebugBoundBreakpoint2::SetHitCount method
ms.assetid: 8145d875-26b1-4049-a2a2-e7d3d7f4735f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: ac7cbfa337bfdcf54d213b299badc9ca56d8dcba
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62877295"
---
# <a name="idebugboundbreakpoint2sethitcount"></a>IDebugBoundBreakpoint2::SetHitCount
Bağlı kesme noktası isabet sayısını ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetHitCount( 
   DWORD dwHitCount
);
```

```csharp
int SetHitCount( 
   uint dwHitCount
);
```

#### <a name="parameters"></a>Parametreler
 `dwHitCount`

 [in] Ayarlanacak isabet sayısı.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_BP_DELETED` bağlı Kesme noktasının nesnenin durumu ayarlanırsa `BPS_DELETED` (parçası [BP_STATE](../../../extensibility/debugger/reference/bp-state.md) sabit listesi).

## <a name="remarks"></a>Açıklamalar
 İsabet sayısı bu Kesme noktasının harekete geçirilen oturumun geçerli çalıştırma sırasında sayısıdır.

 Bu yöntem, genellikle geçerli isabet sayısı bu kesme noktasında güncelleştirmek için hata ayıklama altyapısı tarafından çağrılır.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugBoundBreakpoint2](../../../extensibility/debugger/reference/idebugboundbreakpoint2.md)
- [BP_STATE](../../../extensibility/debugger/reference/bp-state.md)