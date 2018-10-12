---
title: Idiasession::findsymbolbytoken | Microsoft Docs
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
- IDiaSession::findSymbolByToken method
ms.assetid: 3c92149c-6eef-454f-86be-66e89557b9e6
caps.latest.revision: 12
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 2ddd34e08dfaaf24a23b2c8b27010e51e41fbc29
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49261774"
---
# <a name="idiasessionfindsymbolbytoken"></a>IDiaSession::findSymbolByToken
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Belirtilen meta veri belirteci içeren simgeyi alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT findSymbolByToken (   
   ULONG        token,  
   SymTagEnum   symtag,  
   IDiaSymbol** ppSymbol  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `token`  
 [in] Belirteç belirtir.  
  
 `symtag`  
 [in] Bulunacak simge türü. Değerleri verilerinden alınır [SymTagEnum numaralandırması](../../debugger/debug-interface-access/symtagenum.md) sabit listesi.  
  
 `ppSymbol`  
 [out] Döndürür bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) sembol temsil eden bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="example"></a>Örnek  
  
```cpp#  
IDiaSymbol* pFunc;  
pSession->findSymbolByToken( token, SymTagFunction, &pFunc );  
```  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [SymTagEnum Numaralandırması](../../debugger/debug-interface-access/symtagenum.md)



