---
title: IDebugReference2::SetValueAsReference | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugReference2::SetValueAsReference
helpviewer_keywords:
- IDebugReference2::SetValueAsReference
ms.assetid: 94a545d2-16b9-45e9-b2e7-4e49ff90aad0
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 2b14ca1293a709dce35f2e8aa45a7fa22bf29845
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68178191"
---
# <a name="idebugreference2setvalueasreference"></a>IDebugReference2::SetValueAsReference
Başka bir başvuru başvuru değerini ayarlar. Daha sonraki kullanımlar için ayrılmıştır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT SetValueAsReference ( 
   IDebugReference2** rgpArgs,
   DWORD              dwArgCount,
   IDebugReference2*  pValue,
   DWORD              dwTimeout
);
```

```cpp
int SetValueAsReference ( 
   IDebugReference2[] rgpArgs,
   uint               dwArgCount,
   IDebugReference2   pValue,
   uint               dwTimeout
);
```

#### <a name="parameters"></a>Parametreler
 `rgpArgs`

 [in] Bir dizi [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) nasıl başvuru değeri ayarlanacağını belirlemek için kullanılan nesne.

 `dwArgCount`

 [in] Dizi içindeki başvuru sayısı.

 `pValue`

 [in] Bir [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md) özellik değeri ayarlanacağı nesne.

 `dwTimeout`

 [in] Bu yöntemden geri dönmeden önce beklenecek milisaniye cinsinden en uzun süre. Kullanım `INFINITE` süresiz bekleme.

## <a name="return-value"></a>Dönüş Değeri
 Her zaman döndürür `E_NOTIMPL`.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugReference2](../../../extensibility/debugger/reference/idebugreference2.md)