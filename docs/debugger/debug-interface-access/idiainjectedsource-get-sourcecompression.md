---
title: Idiaınjectedsource::get_sourcecompression | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaInjectedSource::get_sourceCompression method
ms.assetid: 854b142f-23a9-466c-bf7f-98e581d5abcd
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: db0cb61d0b2836e5ed3cd3549dbc393b222c58d8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54939975"
---
# <a name="idiainjectedsourcegetsourcecompression"></a>IDiaInjectedSource::get_sourceCompression
Kullanılan kaynak sıkıştırma göstergesi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_sourceCompression (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Kullanılan kaynak sıkıştırma göstergesini döndürür. Sıfır değeri hiçbir kaynak sıkıştırma kullanıldığını gösterir.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem tarafından döndürülen değer, kullanılan derleyici özeldir. Örneğin, bir derleyici Huffman stili çalışma uzunlukta kodlama veya sıkıştırma kullanabilirsiniz.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)