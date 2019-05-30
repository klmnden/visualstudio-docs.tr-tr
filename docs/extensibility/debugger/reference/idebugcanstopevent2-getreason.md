---
title: IDebugCanStopEvent2::GetReason | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugCanStopEvent2::GetReason
helpviewer_keywords:
- IDebugCanStopEvent2::GetReason
ms.assetid: f5de31ca-7b8d-4029-9cf9-ba860ac66af6
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e1b219973e0fced92a588a87ed472cf7a57d312d
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66337266"
---
# <a name="idebugcanstopevent2getreason"></a>IDebugCanStopEvent2::GetReason
Hata ayıklama altyapısı (DE) neden durdurmak ister nedenini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetReason( 
   CANSTOP_REASON* pcr
);
```

```csharp
int GetReason( 
   out enum_CANSTOP_REASON pcr
);
```

## <a name="parameters"></a>Parametreler
`pcr`\
[out] Bir değer döndürür [CANSTOP_REASON](../../../extensibility/debugger/reference/canstop-reason.md) bu olay nedenini açıklayan sabit listesi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Bu yöntem genellikle önce çağrılır [CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md) çağıranın'ın sıfır olmayan geçirmek verilip verilmeyeceğini belirlemek için yöntemi (`TRUE`) için `IDebugCanStopEvent2::CanStop` yöntemi.

 Durdurma nedeni olabilir `CANSTOP_ENTRYPOINT`, DE başka bir deyişle, bir giriş noktası sınırına veya `CANSTOP_STEPIN`, bir işleve kalkan DE anlamına gelir.

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugCanStopEvent2](../../../extensibility/debugger/reference/idebugcanstopevent2.md)
- [CANSTOP_REASON](../../../extensibility/debugger/reference/canstop-reason.md)
- [CanStop](../../../extensibility/debugger/reference/idebugcanstopevent2-canstop.md)