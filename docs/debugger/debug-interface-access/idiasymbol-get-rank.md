---
title: Idiasymbol::get_rank | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_rank method
ms.assetid: 14cc9c4b-a5ec-414a-b01f-4a142c17b7cc
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c38962ab5915a4235201e76e1828f84a56af1333
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64830790"
---
# <a name="idiasymbolgetrank"></a>IDiaSymbol::get_rank
' % S'boyut (boyut sayısı) FORTRAN çok boyutlu bir dizi sayısını alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_rank ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Boyutların sayısı FORTRAN çok boyutlu bir dizi döndürür.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="remarks"></a>Açıklamalar
 Burada dizisi olarak bildirilen bir dizideki boyutların sayısı derecesi başvurduğu `myarray[1,2,3]`. Bu örnekte, 3 ila 3 boyutlu bir dereceli. Boyut her boyut için oluşan bir dizi kavramını kullanan C++ için geçerli değildir (diğer bir deyişle, `myarray[1][2][3]`).

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)