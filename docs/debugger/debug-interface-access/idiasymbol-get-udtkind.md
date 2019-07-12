---
title: Idiasymbol::get_udtkind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_udtKind method
ms.assetid: 4002f887-aea6-4475-b302-67c57079fe0a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 34faf217f77bd30ba707f5ae17886b05dac8ab4f
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "64796643"
---
# <a name="idiasymbolgetudtkind"></a>IDiaSymbol::get_udtKind
Bir kullanıcı tanımlı tür (UDT) çeşitli alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_udtKind ( 
   DWORD* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 `pRetVal`

[out] Bir değer döndürür [UdtKind numaralandırması](../../debugger/debug-interface-access/udtkind.md) bir UDT türünü belirten sabit listesi: yapısı, sınıf veya birleşim.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya hata kodu.

> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
- [UdtKind Numaralandırması](../../debugger/debug-interface-access/udtkind.md)