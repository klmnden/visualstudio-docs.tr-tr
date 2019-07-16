---
title: IDebugModOpt::GetModOpts | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- IDebugModOpt::GetModOpts
- GetModOpts
ms.assetid: cb513fa9-d521-4a65-b968-f55f53a368df
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 319e059116e46d532a7c199ab863538d2154999a
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68162526"
---
# <a name="idebugmodoptgetmodopts"></a>IDebugModOpt::GetModOpts
İsteğe bağlı değiştiricilere listesini alır.

## <a name="syntax"></a>Sözdizimi

```cpp
HRESULT GetModOpts(
   ULONG  celt,
   BSTR*  rgelt,
   ULONG* pceltFetched
);
```

```csharp
int GetModOpts(
   uint         celt,
   out string[] rgelt,
   ref uint     pceltFetched
);
```

#### <a name="parameters"></a>Parametreler
 `celt`

 [in] Döndürülecek öğe sayısı.

 `rgelt`

 [out] Seçenekleri içeren bir dizi döndürür.

 `pceltFetched`

 [out içinde] Döndürülen öğe sayısını `rgelt` dizisi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDebugModOpt](../../../extensibility/debugger/reference/idebugmodopt.md)