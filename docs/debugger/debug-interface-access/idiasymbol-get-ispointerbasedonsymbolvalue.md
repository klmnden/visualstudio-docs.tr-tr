---
title: IDiaSymbol::get_isPointerBasedOnSymbolValue | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 577c8011-9269-4373-8577-b4822a983724
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: fade6cb19d03587ba277d65295838718d0e331be
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53989509"
---
# <a name="idiasymbolgetispointerbasedonsymbolvalue"></a>IDiaSymbol::get_isPointerBasedOnSymbolValue
Belirtir olup olmadığını `this` işaretçi üzerinde bir sembol değeri temel alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_isPointerBasedOnSymbolValue(   
   BOOL* pRetVal);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Bir işaretçi bir `BOOL` belirtir olup olmadığını `this` işaretçi üzerinde bir sembol değeri temel alır.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)