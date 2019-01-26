---
title: Idiaımagedata::get_imagebase | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaImageData::get_imageBase method
ms.assetid: 4ba3d9e4-b205-4ee6-a41d-6996972f1f85
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 238eb138f7e7452e942047d776411d973a689c2a
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54931447"
---
# <a name="idiaimagedatagetimagebase"></a>IDiaImageData::get_imageBase
Görüntü tabanlı burada bellek konumunu alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_imageBase (   
   ULONGLONG* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Önerilen görüntü temel değeri döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Yüklendiğinde görüntü temel çakışmalar nedeniyle görüntü otomatik olarak bir kullanılmayan bellek konumuna ReBase işlemi gerçekleştirildi. Bu yöntem, derleme zamanında modülünde depolanmış temel İpucu (önerilen bellek konumu) döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaImageData](../../debugger/debug-interface-access/idiaimagedata.md)