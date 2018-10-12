---
title: Idiaaddressmap::set_imageheaders | Microsoft Docs
ms.custom: ''
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- IDiaAddressMap::set_imageHeaders method
ms.assetid: a46b9d0e-43e6-433f-b2c7-aa203981e4e4
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f8ef978dfe6da37c06574fd2ec72e87ba21b214b
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49294950"
---
# <a name="idiaaddressmapsetimageheaders"></a>IDiaAddressMap::set_imageHeaders
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kümeleri göreli sanal adres çevirisi'ni etkinleştirmek için üst görüntü.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT set_imageHeaders (   
   DWORD cbData,  
   BYTE  data[],  
   BOOL  originalHeaders  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 cbData  
 [in] Üst bilgi veri baytı sayısı. Olmalıdır `n*sizeof(IMAGE_SECTION_HEADER)` burada `n` bölüm başlıkları, yürütülebilir dosya sayısıdır.  
  
 veri]  
 [in] Bir dizi `IMAGE_SECTION_HEADER` yapıları görüntü üst bilgi olarak kullanılacak.  
  
 originalHeaders  
 [in] Ayarlayın `FALSE` görüntü üstbilgileri yeni görüntüden varsa `TRUE` varsa bunlar orijinal görüntünün bir yükseltmeden önce yansıtır. Genellikle, bu ayarlanır `TRUE` çağrıları ile birlikte, yalnızca [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) yöntemi.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 `IMAGE_SECTION_HEADER` Yapısı Winnt.h içinde bildirilmiş ve yürütülebilir görüntü bölümü üstbilgi biçimi temsil eder.  
  
 Göreli sanal adres hesaplamalar bağlı `IMAGE_SECTION_HEADER` değerleri. DIA genellikle, bu program veritabanı (.pdb) dosyası alır. Bu değerleri eksikse DIA göreli sanal adreslerine duyduğunu hesaplayamadığını ve [Idiaaddressmap::get_relativevirtualaddressenabled](../../debugger/debug-interface-access/idiaaddressmap-get-relativevirtualaddressenabled.md) yöntemi döndürür `FALSE`. İstemci ardından çağırmalıdır [Idiaaddressmap::put_relativevirtualaddressenabled](../../debugger/debug-interface-access/idiaaddressmap-put-relativevirtualaddressenabled.md) göreli sanal adres hesaplamalar görüntünün kendisi eksik görüntü üst bilgiler girdikten sonra etkinleştirmek için yöntemi.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaaddressmap](../../debugger/debug-interface-access/idiaaddressmap.md)   
 [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)   
 [Idiaaddressmap::get_relativevirtualaddressenabled](../../debugger/debug-interface-access/idiaaddressmap-get-relativevirtualaddressenabled.md)   
 [IDiaAddressMap::put_relativeVirtualAddressEnabled](../../debugger/debug-interface-access/idiaaddressmap-put-relativevirtualaddressenabled.md)



