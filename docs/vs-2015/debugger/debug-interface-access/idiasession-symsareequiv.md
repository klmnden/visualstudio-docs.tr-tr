---
title: Idiasession::symsareequiv | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSession::symsAreEquiv method
ms.assetid: 9941d520-e203-46c0-83c3-b3a967f4fc59
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: ba8c77d7d97da75ce82fcbe732db64acf633b8af
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54794397"
---
# <a name="idiasessionsymsareequiv"></a>IDiaSession::symsAreEquiv
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İki simge eşdeğer olup olmadığını denetler.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT symsAreEquiv (   
   IDiaSymbol* symbolA,  
   IDiaSymbol* symbolB  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `symbolA`  
 [in] İlk [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) Karşılaştırmada kullanılan nesne.  
  
 `symbolB`  
 [in] İkinci `IDiaSymbol` Karşılaştırmada kullanılan nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Simgeleri eşdeğer ise döndürür `S_OK`; Aksi halde döndürür `S_FALSE`, simgeler eşdeğer değildir. Aksi takdirde bir hata kodunu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasession](../../debugger/debug-interface-access/idiasession.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)
