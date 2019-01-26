---
title: Idiasession::findsymbolbyrva | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findSymbolByRVA method
ms.assetid: 14fb2903-b771-44d6-b0a8-44e0097c58ce
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: a9061a4f95e8bc70382185c9996c21524339fcaa
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54919960"
---
# <a name="idiasessionfindsymbolbyrva"></a>IDiaSession::findSymbolByRVA
İçeren veya bir belirtilen göreli sanal adres için (RVA) en yakın bir belirtilen simge türü alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findSymbolByRVA (   
   DWORD        rva,  
   SymTagEnum   symtag,  
   IDiaSymbol** ppSymbol  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `rva`  
 [in] RVA belirtir.  
  
 `symtag`  
 [in] Bulunacak simge türü. Değerleri verilerinden alınır [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) sabit listesi.  
  
 `ppSymbol`  
 [out] Döndürür bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) sembol temsil eden bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
  
```C++  
IDiaSymbol* pFunc;  
pSession->findSymbolByRVA( rva, SymTagFunction, &pFunc );  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)