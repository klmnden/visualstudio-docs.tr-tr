---
title: Idiaaddressmap::put_addressmapenabled | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::put_addressMapEnabled method
ms.assetid: 0f205337-4e59-4383-8059-7b1d207d6dcd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f36cf93beb6b6c8b66ec25dc8008be7024e398b9
ms.sourcegitcommit: d0425b6b7d4b99e17ca6ac0671282bc718f80910
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/21/2019
ms.locfileid: "56641370"
---
# <a name="idiaaddressmapputaddressmapenabled"></a>IDiaAddressMap::put_addressMapEnabled
Adres Haritası sembol adreslerine çevirmek için kullanılıp kullanılmayacağını belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
HRESULT put_addressMapEnabled ( 
   BOOL NewVal
);
```

#### <a name="parameters"></a>Parametreler
 NewVal

[in] Kümesine `TRUE` sembolleri çevirisini etkinleştirmek için veya `FALSE` devre dışı bırakmak için.

## <a name="return-value"></a>Dönüş Değeri
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.

## <a name="remarks"></a>Açıklamalar
 Yürütülebilir sonrası işlemci bazen yürütülebilir güncelleştirin. DIA mekanizması semboller yeni düzene çevirisi desteği içerir.

 Bir PDB dosyası yüklendiğinde dosyasında depolanan adres Haritası etkinleştirilir. Ne zaman bir istemci uygulaması gerekebilir çağırarak kendi adres Haritası sağlamanız zamanlar [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) yöntemi. Varsa `set_addressMap` yöntemi başarılı olduğu için istemci uygulamasını çağırmanız gerekir `put_addressMapEnabled` yöntemi ile bir `NewVal` parametresinin `TRUE` adresi eşlenen kullanımını etkinleştirmek için.

 Etkinleştirilen adres Haritası geçerli durumunu çağrısıyla alınabilir [Idiaaddressmap::get_addressmapenabled](../../debugger/debug-interface-access/idiaaddressmap-get-addressmapenabled.md) yöntemi.

## <a name="see-also"></a>Ayrıca Bkz.
- [IDiaAddressMap](../../debugger/debug-interface-access/idiaaddressmap.md)
- [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)
- [IDiaAddressMap::get_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-get-addressmapenabled.md)