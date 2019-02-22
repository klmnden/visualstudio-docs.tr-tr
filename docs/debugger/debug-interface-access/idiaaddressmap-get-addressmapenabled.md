---
title: Idiaaddressmap::get_addressmapenabled | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::get_addressMapEnabled method
ms.assetid: 6183dc5e-befa-4e5a-ae5a-f4aa24f3ed9e
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 7391010e409cc25a3151bb2abb806289c81288a1
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641892"
---
# <a name="idiaaddressmapgetaddressmapenabled"></a>IDiaAddressMap::get_addressMapEnabled
Belirli bir oturum için bir adres eşlemesi kurulduktan olup olmadığını gösterir.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT get_addressMapEnabled ( 
   BOOL* pRetVal
);
```

#### <a name="parameters"></a>Parametreler
 pRetVal

[out] Döndürür `TRUE` adres eşlemesi etkinse.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Yürütülebilir sonrası işlemci bazen yürütülebilir güncelleştirin. DIA mekanizması semboller yeni düzene çevirisi desteği içerir.

 İstemci uygulamaları ayarlayabilirsiniz adres eşlemesi için belirli bir oturum alarak [Idiaaddressmap](../../debugger/debug-interface-access/idiaaddressmap.md) alanından arabirim [Idiasession](../../debugger/debug-interface-access/idiasession.md) arabirimi ve arama [IDiaAddressMap::set_ addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) yöntemine bir çağrı tarafından izlenen [Idiaaddressmap::put_addressmapenabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md) yöntemi. `get_addressMapEnabled` Yöntemi çağırma sonuçları döndürür `put_addressMapEnabled` yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)
- [IDiaSession](../../debugger/debug-interface-access/idiasession.md)
- [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)
- [IDiaAddressMap::put_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md)