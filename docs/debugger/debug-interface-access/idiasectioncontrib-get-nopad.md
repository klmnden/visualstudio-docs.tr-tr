---
title: Idiasectioncontrib::get_nopad | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSectionContrib::get_nopad method
ms.assetid: f5c08603-0b3e-4e81-acf1-1b95a6a83bed
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 402cd3840e78785ca9cda755b5e7e33e33d7db36
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54999697"
---
# <a name="idiasectioncontribgetnopad"></a>IDiaSectionContrib::get_nopad
Bölüm sonraki bellek sınırına sıfır değil olup olmadığını belirten bir bayrak alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_nopad(  
   BOOL* pRetVal  
};  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Döndürür `TRUE` bölümü sonraki bellek sınırına; sıfır değil, aksi halde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` varsa bu özelliği desteklenmiyor. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu, genellikle yalnızca eski dosyaları görülen bir özelliktir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSectionContrib](../../debugger/debug-interface-access/idiasectioncontrib.md)