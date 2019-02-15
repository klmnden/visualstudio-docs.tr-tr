---
title: IDebugBoundBreakpoint2::GetState | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- IDebugBoundBreakpoint2::GetState
helpviewer_keywords:
- GetState method
- IDebugBoundBreakpoint2::GetState method
ms.assetid: a40a8382-295e-4916-aae6-ffe3a9cd3f2d
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 7cf782a23c630153539f76b66c97af8db15a4d6a
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315969"
---
# <a name="idebugboundbreakpoint2getstate"></a>IDebugBoundBreakpoint2::GetState
Bu bağlı Kesme noktasının durumunu alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetState( 
    BP_STATE* pState
);
```

```csharp
int GetState( 
    out enum_BP_STATE pState
);
```

#### <a name="parameters"></a>Parametreler
`pState`  
[out] Bir değer döndürür [BP_STATE](../../../extensibility/debugger/reference/bp-state.md) Kesme noktasının durumunu açıklayan sabit listesi.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CBoundBreakpoint` gösteren nesne [IDebugBoundBreakpoint2](../../../extensibility/debugger/reference/idebugboundbreakpoint2.md) arabirimi.

```
HRESULT CBoundBreakpoint::GetState(BP_STATE* pState)
{
    HRESULT hr;

    // Check for a valid pointer to pState and assign the local state variable.
    if (pState)
    {
        *pState = m_state;
        hr = S_OK;
    }
    else
    {
        hr = E_INVALIDARG;
    }

    return hr;
}
```

## <a name="see-also"></a>Ayrıca Bkz.
[IDebugBoundBreakpoint2](../../../extensibility/debugger/reference/idebugboundbreakpoint2.md)  
[BP_STATE](../../../extensibility/debugger/reference/bp-state.md)
