---
title: Idiasymbol::get_typeıds | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_typeIds method
ms.assetid: 5166e647-fde5-4efe-92bf-77f8ae3fbc9b
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 12024a3a024f2c9433e144790c0a513d4e33df12
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56643749"
---
# <a name="idiasymbolgettypeids"></a>IDiaSymbol::get_typeIds
Bu simgenin derleyici özel tür tanımlayıcı değerleri dizisini alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_typeIds ( 
   DWORD  cTypeIds,
   DWORD* pcTypeIds,
   DWORD  typeIds[]
);
```

#### <a name="parameters"></a>Parametreler
 `cTypeIds`

[in] Verileri tutmak için arabellek boyutu.

 `pcTypeIds`

[out] Sayısını döndürür `typeIds` yazılan veya `typeIds` olduğu `NULL`, ardından tip tanımlayıcıları kullanılabilir toplam sayısı.

 `typeIds[]`

[out] Oturum türü tanımlayıcılar doldurulması için bir dizi.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)