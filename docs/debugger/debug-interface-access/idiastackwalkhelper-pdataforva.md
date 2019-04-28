---
title: IDiaStackWalkHelper::pdataForVA | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2::pdataByVA method
ms.assetid: fafc38fe-74dc-4726-9a51-eebf3a673d7f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 6315032a36369eff7a5d43241ae4968a64ad42cc
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62831901"
---
# <a name="idiastackwalkhelperpdataforva"></a>IDiaStackWalkHelper::pdataForVA
Sanal adresle ilişkilendirilen PDATA veri bloğu döndürür.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT pdataForVA( 
   ULONGLONG  va,
   DWORD      cbData,
   DWORD*     pcbData,
   BYTE*      pbData
);
```

#### <a name="parameters"></a>Parametreler
 `va`

[in] Sanal adres edinmek için verilerin belirtir.

 `cbData`

[in] Veri almak için bayt cinsinden boyutu.

 `pcbData`

[out] Gerçek veri boyutunu edinilen bayt cinsinden döndürür.

 `pbData`

[out içinde] İstenen veriler ile doldurulmuş bir arabellek. Olamaz `NULL`.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` hiçbir PDATA belirtilen adresi için varsa. Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 PDATA (".pdata" adlı bölümde) bir derlenecek özel durum işleme için işlevleri hakkında bilgi içerir.

 Çağıran, arayan için ne kadar veri kullanılabilir isteyin gerek yoktur. Bu nedenle döndürülecek ne kadar veri olduğunu bilir. Bu nedenle, bu yöntemin bir hata ise döndürülecek bir uygulama için kabul edilebilir `pbData` parametresi `NULL`.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)