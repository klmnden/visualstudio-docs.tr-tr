---
title: IDiaSymbol::findInlineeLines | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 56ba4bc0-8f96-47c2-8b18-332b4e7c2d91
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 008328536e7fe465594f4fbfec25a52aa2a1ed64
ms.sourcegitcommit: 37fb7075b0a65d2add3b137a5230767aa3266c74
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/02/2019
ms.locfileid: "53927083"
---
# <a name="idiasymbolfindinlineelines"></a>IDiaSymbol::findInlineeLines
Satır numarası bilgisi tüm işlevlerin satır içine alınmış, doğrudan veya dolaylı olarak bu sembol yinelemek bir istemci sağlayan bir sabit listesi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findInlineeLines (   
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppResult`  
 [out] Tutan bir `IDiaEnumLineNumbers` alınan satır numaraları listesi içeren nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md)   
 [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaSession::findInlineeLines](../../debugger/debug-interface-access/idiasession-findinlineelines.md)