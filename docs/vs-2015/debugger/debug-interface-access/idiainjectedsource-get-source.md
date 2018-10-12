---
title: Idiaınjectedsource::get_source | Microsoft Docs
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
- IDiaInjectedSource::get_source method
ms.assetid: 3c0b5386-321f-4f8f-85cc-e2ee7b4cc3d2
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 03f02815518e6b4d540514bffbc6f93924d003b8
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49211659"
---
# <a name="idiainjectedsourcegetsource"></a>IDiaInjectedSource::get_source
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kaynak kodu bayt alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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



