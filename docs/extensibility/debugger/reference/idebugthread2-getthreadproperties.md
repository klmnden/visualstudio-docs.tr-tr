---
title: IDebugThread2::GetThreadProperties | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugThread2::GetThreadProperties
helpviewer_keywords:
- IDebugThread2::GetThreadProperties
ms.assetid: 304403fd-f4f8-4096-ac2c-bd3b59663aad
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: a325e8798f54d8ec78ad0ec5318e9162b16774b1
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66320109"
---
# <a name="idebugthread2getthreadproperties"></a>IDebugThread2::GetThreadProperties
Bu iş parçacığı tanımlayan özellikleri alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetThreadProperties (
    THREADPROPERTY_FIELDS dwFields,
    THREADPROPERTIES*     ptp
);
```

```csharp
int GetThreadProperties (
    enum_THREADPROPERTY_FIELDS dwFields,
    THREADPROPERTIES[]         ptp
);
```

## <a name="parameters"></a>Parametreler
`dwFields`\
[in] Bayraklarının bir birleşimi [THREADPROPERTY_FIELDS](../../../extensibility/debugger/reference/threadproperty-fields.md) hangi alanlarının belirleyen sabit listesi `ptp` doldurulacak olan.

`ptp`\
[out içinde] A [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md) iş parçacığı özelliklerini oturum girilir yapısının.

## <a name="return-value"></a>Dönüş Değeri
Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
Bu yöntemle döndürülen bilgileri genellikle gösterilen **iş parçacıkları** hata ayıklama penceresine.

## <a name="example"></a>Örnek
Aşağıdaki örnek, bu yöntem için basit bir uygulama gösterilmektedir `CProgram` uygulayan nesne [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md) arabirimi.

```cpp
HRESULT CProgram::GetThreadProperties(THREADPROPERTY_FIELDS dwFields,
                                      THREADPROPERTIES *ptp)
{
    HRESULT hr = E_FAIL;

    // Check for valid argument.
    if (ptp)
    {
        // Create an array of buffers at ptp the size of the
        // THREADPROPERTIES structure and set all of the
        // buffers at ptp to 0.
        memset(ptp, 0, sizeof (THREADPROPERTIES));

        // Check if there is a valid THREADPROPERTY_FIELDS and the TPF_ID flag is set.
        if (dwFields & TPF_ID)
        {
            // Check for successful assignment of the current thread ID to
            // the dwThreadId of the passed THREADPROPERTIES.
            if (GetThreadId(&(ptp->dwThreadId)) == S_OK)
            {
                // Set the TPF_ID flag in the THREADPROPERTY_FIELDS enumerator
                // of the passed THREADPROPERTIES.
                ptp->dwFields |= TPF_ID;
            }
        }

        hr = S_OK;
    }
    else
        hr = E_INVALIDARG;

    return hr;
}
```

## <a name="see-also"></a>Ayrıca bkz.
- [IDebugThread2](../../../extensibility/debugger/reference/idebugthread2.md)
- [THREADPROPERTY_FIELDS](../../../extensibility/debugger/reference/threadproperty-fields.md)
- [THREADPROPERTIES](../../../extensibility/debugger/reference/threadproperties.md)
