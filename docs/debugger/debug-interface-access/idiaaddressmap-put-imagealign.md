---
title: Idiaaddressmap::put_imagealign | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::put_imageAlign method
ms.assetid: f9ce875d-c263-43e5-a534-f34c37f9866f
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a78b1d03eddfcedb04966276c889219630c45f83
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54950747"
---
# <a name="idiaaddressmapputimagealign"></a>IDiaAddressMap::put_imageAlign
Resim hizalamasını ayarlar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT put_imageAlign (   
   DWORD NewVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 NewVal  
 [in] Yürütülebilir dosya için yeni görüntü hizalama değeri.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Belirtilen bellek sınırlarını için görüntüleri (yüklenen yürütülebilir dosyalar) hizalanır. Bu hizalama, geçerli sistem mimarisi ve derleme ve bağlama zamanı seçenekleri tarafından etkilenebilir. Resmi hizalaması bayt sınırlarda her zaman olur. Aşağıdaki görüntü hizalama değerler geçerlidir: 1, 2, 4, 8, 16, 32 ve 64 baytlık sınırlar.  
  
 Bir çağrı ile geçerli görüntü hizalama alınabilir [Idiaaddressmap::get_imagealign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md) yöntemi.  
  
> [!NOTE]
>  Bu yöntem zamanında resmi zaten yüklü. `put_imageAlign` Yöntemi genellikle görüntünün taşınmış veya değiştirilmiş ve yeni bir hizalama gerekli olduğunda kullanılır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaaddressmap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [IDiaAddressMap::get_imageAlign](../../debugger/debug-interface-access/idiaaddressmap-get-imagealign.md)