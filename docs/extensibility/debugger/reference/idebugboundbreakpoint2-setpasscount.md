---
title: IDebugBoundBreakpoint2::SetPassCount | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBoundBreakpoint2::SetPassCount
helpviewer_keywords:
- SetPassCount method
- IDebugBoundBreakpoint2::SetPassCount method
ms.assetid: b32c12f9-b34d-43bd-a1b9-61af6cf8e51b
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 273735feeca633a1104a072c0e4d37c520d9de23
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56712183"
---
# <a name="idebugboundbreakpoint2setpasscount"></a>IDebugBoundBreakpoint2::SetPassCount
Bu bağlı Kesme noktasının ile ilişkili parola sayısı değiştirir veya ayarlar.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetPassCount( 
   BP_PASSCOUNT bpPassCount
);
```

```csharp
int SetPassCount( 
   BP_PASSCOUNT bpPassCount
);
```

#### <a name="parameters"></a>Parametreler
 `bpPassCount`

 [in] [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md) yapısını parola sayısını belirtir.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür. Döndürür `E_BP_DELETED` bağlı Kesme noktasının nesnenin durumu ayarlanırsa `BPS_DELETED` (parçası [BP_STATE](../../../extensibility/debugger/reference/bp-state.md) sabit listesi).

## <a name="remarks"></a>Açıklamalar
 Kesme noktasının ne zaman tetiklenir parola sayısını belirler. İsabet sayısı ve geçerli geçişi çağrılarak alınabilir [GetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-gethitcount.md) yöntemi.

 Daha önce bu kesme noktası ile ilişkili tüm geçiş sayısı kaybolur.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugBoundBreakpoint2](../../../extensibility/debugger/reference/idebugboundbreakpoint2.md)
- [GetHitCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-gethitcount.md)
- [BP_PASSCOUNT](../../../extensibility/debugger/reference/bp-passcount.md)
- [BP_STATE](../../../extensibility/debugger/reference/bp-state.md)