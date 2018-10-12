---
title: Idiastackwalkframe::readmemory | Microsoft Docs
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
- IDiaStackWalkFrame::readMemory method
ms.assetid: 7ab0b525-a5a7-4692-acad-e8c00fa9ab9a
caps.latest.revision: 15
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: c5f6758206ced4d4be19552ada3bb4a8ac62e10f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49300865"
---
# <a name="idiastackwalkframereadmemory"></a>IDiaStackWalkFrame::readMemory
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bellek görüntüden okur.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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



