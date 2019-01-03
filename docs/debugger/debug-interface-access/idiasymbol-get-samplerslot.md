---
title: IDiaSymbol::get_samplerSlot | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 41c751ba-81be-4bd3-838f-8373fc146157
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: f48731c7c7abdcd0eb36f24b8d49eead0247cbf7
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53985715"
---
# <a name="idiasymbolgetsamplerslot"></a>IDiaSymbol::get_samplerSlot
Örnekleyici yuvası alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_samplerSlot(   
   DWORD* pRetVal);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Bir işaretçi bir `DWORD` örnekleyici yuvası tutan.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)