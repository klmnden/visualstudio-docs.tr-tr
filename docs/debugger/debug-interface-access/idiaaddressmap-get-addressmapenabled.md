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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: dc632a0eda039c5f3268d2007f45d7cddd096baa
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53896662"
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
 [Idiaaddressmap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)   
 [IDiaAddressMap::put_addressMapEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-addressmapenabled.md)