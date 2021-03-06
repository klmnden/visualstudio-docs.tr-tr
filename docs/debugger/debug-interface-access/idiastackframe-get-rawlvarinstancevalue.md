---
title: Idiastackframe::get_rawlvarınstancevalue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackFrame::get_rawLVarInstanceValue method
ms.assetid: ce526259-85a6-475b-9274-0b3a21d95db2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a8ad236307360a96f64999313764424305980fc9
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62838125"
---
# <a name="idiastackframegetrawlvarinstancevalue"></a>IDiaStackFrame::get_rawLVarInstanceValue
Bu yöntem, ham bayt olarak belirlenen yerel değişkenin değerini alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_rawLVarInstanceValue(
   IDiaLVarInstance* pInstance,
   DWORD             cbDataMax,
   DWORD*            pcbData,
   BYTE*             pbData
);
```

#### <a name="parameters"></a>Parametreler
 `pInstance`

[in] Bir `IDiaLVarInstance` değerini almak için yerel değişken bir örneğini temsil eden nesne.

 `cbDataMax`

[in] Arabellekteki bayt sayısı tarafından işaret edilen `pbData`. Bu, en fazla 8 bayt olabilir (`sizeof(ULONGLONG)`).

 `pcbData`

[out] Gerçek arabellekteki depolanan bayt sayısını döndürür.

 `pbData`

[out] Veri ile doldurulacak bir arabellek. Bu olamaz `NULL`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaStackFrame](../../debugger/debug-interface-access/idiastackframe.md)