---
title: Idiaenumınjectedsources::Item | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumInjectedSources::Item method
ms.assetid: 14846955-7270-451d-91d2-9cb34bb65187
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2fd803520a6b6bb58679dd30dbf913450ce6066a
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56636287"
---
# <a name="idiaenuminjectedsourcesitem"></a>IDiaEnumInjectedSources::Item
Eklenen bir kaynak dizin yoluyla alır.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT Item ( 
   DWORD                index,
   IDiaInjectedSource** injectedSource
);
```

#### <a name="parameters"></a>Parametreler
 dizin

[in] Dizin [Idiaınjectedsource](../../debugger/debug-interface-access/idiainjectedsource.md) alınacak nesne. ' % S'aralığı 0 için dizinidir `count`-1, burada `count` tarafından döndürülen [Idiaenumınjectedsources::get_Count](../../debugger/debug-interface-access/idiaenuminjectedsources-get-count.md) yöntemi.

 injectedSource

[out] Döndürür bir [Idiaınjectedsource](../../debugger/debug-interface-access/idiainjectedsource.md) eklenen kaynak temsil eden nesne.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaEnumInjectedSources](../../debugger/debug-interface-access/idiaenuminjectedsources.md)
- [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)