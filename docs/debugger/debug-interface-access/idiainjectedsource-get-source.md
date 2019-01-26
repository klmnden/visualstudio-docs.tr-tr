---
title: Idiaınjectedsource::get_source | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaInjectedSource::get_source method
ms.assetid: 3c0b5386-321f-4f8f-85cc-e2ee7b4cc3d2
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 3b5582990ff3db2e03dce9dc0c198a907de978d9
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54971081"
---
# <a name="idiainjectedsourcegetsource"></a>IDiaInjectedSource::get_source
Kaynak kodu bayt alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_source (   
   DWORD  cbData,  
   DWORD* pcbData,  
   BYTE   data[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `cbData`  
 [in] Veri arabellek boyutu temsil eden bayt sayısı.  
  
 `pcbData`  
 [out] Döndürülen bayt sayısını temsil eden bayt sayısı. Varsa `data` olduğu `NULL`, ardından `pcbData` verileri baytlık toplam sayısı kullanılabilir.  
  
 `data[]`  
 [out] Kaynak bayt ile doldurulacak olan bir arabellek.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)