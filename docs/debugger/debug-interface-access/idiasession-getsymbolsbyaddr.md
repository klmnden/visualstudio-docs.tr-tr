---
title: Idiasession::getsymbolsbyaddr | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::getSymbolsByAddr method
ms.assetid: eafcc757-b488-487d-a063-ad3703ff42e8
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 91c8efba79868e3e6fa887bf5babff42adb15c45
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54992769"
---
# <a name="idiasessiongetsymbolsbyaddr"></a>IDiaSession::getSymbolsByAddr
Semboller adreslerini sırasına göre bulur bir numaralandırıcı alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT getSymbolsByAddr(   
   IDiaEnumSymbolsByAddr** ppEnumbyAddr  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `ppEnumbyAddr`  
 [out] Döndürür bir [Idiaenumsymbolsbyaddr](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr.md) nesne. Bu arabirim tarafından bellek konumunda sembol deposu sembolleri aramak için kullanın.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaEnumSymbolsByAddr](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr.md)