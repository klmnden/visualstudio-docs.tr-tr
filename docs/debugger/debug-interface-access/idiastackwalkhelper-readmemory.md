---
title: IDiaStackWalkHelper::readMemory | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaStackWalkHelper2::readMemory method
ms.assetid: e1eb90aa-49b7-476c-9e70-7e8f08994cbe
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 7d12d1da983a69f71d96bb06271bd3a971a16cbb
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53825743"
---
# <a name="idiastackwalkhelperreadmemory"></a>IDiaStackWalkHelper::readMemory
Bir veri bloğu bellek yürütülebilir dosyası görüntüden okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT readMemory(   
   enum MemoryTypeEnum type,  
   ULONGLONG           va,  
   DWORD               cbData,  
   DWORD*              pcbData,  
   BYTE*               pbData  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `type`  
 [in] Bir değer [MemoryTypeEnum numaralandırması](../../debugger/debug-interface-access/memorytypeenum.md) okumak için bellek türünü belirten sabit listesi.  
  
 Va  
 [in] Sanal adres okumaya başlayacağı görüntüde.  
  
 `cbData`  
 [in] Veri arabelleğin bayt cinsinden boyutu.  
  
 `pcbData`  
 [out] Aslında okunan bayt sayısını döndürür. Varsa `pbData` olduğu `NULL`, sonra bu verilerin kullanılabilir bayt sayısı.  
  
 `pbData`  
 [out içinde] Okuma bellek ile doldurulmuş bir arabellek.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaStackWalkHelper](../../debugger/debug-interface-access/idiastackwalkhelper.md)   
 [MemoryTypeEnum Numaralandırması](../../debugger/debug-interface-access/memorytypeenum.md)