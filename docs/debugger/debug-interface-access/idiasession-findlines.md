---
title: Idiasession::findlines | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::findLines method
ms.assetid: d6e84916-fd55-457e-b057-57f97b51fe73
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: ae2278835f6de612b61e5fc0a2a1fc2689bad564
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55019482"
---
# <a name="idiasessionfindlines"></a>IDiaSession::findLines
Belirtilen derlenecek ve kaynak dosya tanımlayıcıları içinde satır numaralarını alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
HRESULT findLines (   
   IDiaSymbol*           compiland,  
   IDiaSourceFile*       file,  
   IDiaEnumLineNumbers** ppResult  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `compiland`  
 [in] Bir [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) derlenecek temsil eden nesne. Bu arabirim için satır numaralarını aranacağı bir bağlamda kullanın.  
  
 `file`  
 [in] Bir [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md) için satır numaralarını aranacağı kaynak dosyasını temsil eden nesne.  
  
 `ppResult`  
 [out] Döndürür bir [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md) satır numaralarının listesini içeren bir nesne alındı.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [Idiasourcefile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)