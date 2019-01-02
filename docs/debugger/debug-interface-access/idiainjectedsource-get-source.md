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
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: a923e323f4ca9dc7f661457add7665f8c136ae92
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53824463"
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