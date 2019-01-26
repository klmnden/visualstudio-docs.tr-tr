---
title: Idiasymbol::get_targetrelativevirtualaddress | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_targetRelativeVirtualAddress method
ms.assetid: 49a159f3-6943-44d3-90a3-0dba51e8a7ec
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: c6f38b983945b7182f0e0822133f6542922dc1f0
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55016295"
---
# <a name="idiasymbolgettargetrelativevirtualaddress"></a>IDiaSymbol::get_targetRelativeVirtualAddress
Dönüştürücü hedefi göreli sanal adres (RVA) alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT get_targetRelativeVirtualAddress (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Dönüştürücü hedefi RVA döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu özellik geçerli yalnızca simgesi olarak bir [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) değerini `SymTagThunk`.  
  
 Bir "dönüştürücü" dönüştürür (segmentlere ayrılmış adres alanı olarak da bilinir) bir 16 bit adres alanı ile bir 32-bit bellek adres alanı (düz adres alanı olarak da bilinir) arasındaki kod parçasıdır.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)