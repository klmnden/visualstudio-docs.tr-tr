---
title: Idiaaddressmap::get_imagealign | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::get_imageAlign method
ms.assetid: f1ba8071-669c-4cf7-9ac0-02f26d99f366
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f5731c0ec7ba6b7e6e05205e266ecc91efaba194
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54919440"
---
# <a name="idiaaddressmapgetimagealign"></a>IDiaAddressMap::get_imageAlign
Geçerli resim hizalamasını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_imageAlign (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Çalıştırılabilir dosyadan görüntü hizalama değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Görüntüleri görüntünün nasıl yüklenir ve oluşturulan bağlı olarak belirli bellek sınırları hizalanır. Hizalama, genellikle 1, 2, 4, 8, 16, 32 veya 64 baytlık sınırlardaki oluşur. Resmi hizalaması çağrısıyla ayarlanabilir [Idiaaddressmap::put_imagealign](../../debugger/debug-interface-access/idiaaddressmap-put-imagealign.md) yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaaddressmap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [IDiaAddressMap::put_imageAlign](../../debugger/debug-interface-access/idiaaddressmap-put-imagealign.md)