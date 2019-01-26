---
title: Idiaaddressmap::put_relativevirtualaddressenabled | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::put_relativeVirtualAddressEnabled method
ms.assetid: 767c078e-8ad7-4940-9e00-cae7704aadee
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: f32b83ce4d44a18b3eb50d246a5d5ff4800316c8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54927639"
---
# <a name="idiaaddressmapputrelativevirtualaddressenabled"></a>IDiaAddressMap::put_relativeVirtualAddressEnabled
Etkinleştirmek veya hesaplama ve göreli sanal adreslerine (RVA) kullanımını devre dışı bırakmak istemcinin sağlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT put_relativeVirtualAddressEnabled (   
   BOOL NewVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 NewVal  
 [in] Kümesine `TRUE` etkinleştirmek için veya `FALSE` devre dışı bırakmak için.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 DIA arabirimleri ve temel, yürütülebilir dosyası görüntü göre açıklanan hata ayıklama nesneler için adresleri göreli sanal adreslerine alınabilir.  
  
 Parçaları bir PDB dosyasındaki ilk yüklendiğinde RVA kullanımını etkinleştirilir. RVA kullanımını geçerli durumunu almak için arama [Idiaaddressmap::get_relativevirtualaddressenabled](../../debugger/debug-interface-access/idiaaddressmap-get-relativevirtualaddressenabled.md) yöntemi.  
  
 `put_relativeVirtualAddress` Yöntemi çağrıldığında, başarılı bir çağrı sonra RVA etkinleştirmek için [Idiaaddressmap::set_imageheaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md) yöntemi yeni bir görüntü üstbilgileri kurulan.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaaddressmap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [Idiaaddressmap::get_relativevirtualaddressenabled](../../debugger/debug-interface-access/idiaaddressmap-get-relativevirtualaddressenabled.md)   
 [IDiaAddressMap::set_imageHeaders](../../debugger/debug-interface-access/idiaaddressmap-set-imageheaders.md)