---
title: Idiaınjectedsource::get_objectfilename | Microsoft Docs
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
- IDiaInjectedSource::get_objectFilename method
ms.assetid: 7c42847a-f0df-443a-a9fe-c495c1271ea8
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: a6c27b631beb0165548087156f2d6c0c9cf7558e
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49176591"
---
# <a name="idiainjectedsourcegetobjectfilename"></a>IDiaInjectedSource::get_objectFilename
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kaynak için derlenen nesne dosyası adını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_objectFilename (   
   BSTR* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Kaynak için derlenen nesne dosyası adını döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaInjectedSource](../../debugger/debug-interface-access/idiainjectedsource.md)



