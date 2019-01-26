---
title: Idiasymbol::get_container | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_container method
ms.assetid: 24e832eb-80b3-484c-a41b-11477ec9de99
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 08019de39c6e579bb0cfa08732f97a748141fb5b
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55039806"
---
# <a name="idiasymbolgetcontainer"></a>IDiaSymbol::get_container
Bu işlev, bu sembol üst/kapsayıcı temsil eden bir sembol için bir işaretçi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_container(  
   IDiaSymbol **pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Bir işaretçi döndüren bir `IDiaSymbol` bu simgenin kapsayıcı hakkında bilgileri içeren.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılıysa S_OK döndürür; Aksi takdirde S_FALSE veya bir hata kodu döndürür.  
  
> [!NOTE]
>  S_FALSE dönüş değeri, özellik simge için kullanılabilir olmadığı anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)