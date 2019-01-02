---
title: IDiaSymbol::get_numberOfColumns | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 64834351-e2c9-4f1c-9dc0-2abb5478bc63
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 24c6078cd1246e5bcb13938e31f65e67f5615e4a
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53953202"
---
# <a name="idiasymbolgetnumberofcolumns"></a>IDiaSymbol::get_numberOfColumns
Matris sütun sayısını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_numberOfColumns(   
   DWORD* pRetVal);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Bir işaretçi bir `DWORD` matriste, sütun sayısını tutar.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)