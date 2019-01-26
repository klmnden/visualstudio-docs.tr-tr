---
title: Idiastackwalkframe::readmemory | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkFrame::readMemory method
ms.assetid: 7ab0b525-a5a7-4692-acad-e8c00fa9ab9a
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 97b1f58f31484084bff502d9ad6a019089ecfec8
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992532"
---
# <a name="idiastackwalkframereadmemory"></a>IDiaStackWalkFrame::readMemory
Bellek görüntüden okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT readMemory (   
   MemoryTypeEnum type,  
   ULONGLONG va,  
   DWORD     cbData,  
   DWORD*    pcbData,  
   BYTE      data[]  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `type`  
 [in] Aşağıdakilerden birini [MemoryTypeEnum numaralandırması](../../debugger/debug-interface-access/memorytypeenum.md) erişmek için bellek türünü belirten numaralandırma değerlerinden.  
  
 `va`  
 [in] Sanal adres görüntü okumanın başlatılacağı konum.  
  
 `cbData`  
 [in] Veri arabelleğin bayt cinsinden boyutu.  
  
 `pcbData`  
 [out] Döndürülen bayt sayısını döndürür. Varsa `data` olduğu `NULL`, ardından `pcbData` kullanılabilir verileri baytlık toplam sayısını içerir.  
  
 `data`  
 [out] Belirtilen konumdan veri ile doldurulacak olan bir arabellek.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaStackWalkFrame](../../debugger/debug-interface-access/idiastackwalkframe.md)