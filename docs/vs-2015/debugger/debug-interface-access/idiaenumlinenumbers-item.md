---
title: Idiaenumlinenumbers::Item | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaEnumLineNumbers::Item method
ms.assetid: 08efbeaf-22f7-49e9-96a8-bb906dfe4fd8
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 630c86e463cdc6ff838fad00d5d02e6f67c729d7
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68190137"
---
# <a name="idiaenumlinenumbersitem"></a>IDiaEnumLineNumbers::Item
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir satır numarası yoluyla dizin alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Item (   
   DWORD            index,  
   IDiaLineNumber** lineNumber  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 dizin  
 [in] Dizin [Idialinenumber](../../debugger/debug-interface-access/idialinenumber.md) alınacak nesne. İçin 0 aralığındaki dizinidir `count`-1, burada `count` tarafından döndürülen [Idiaenumlinenumbers::get_Count](../../debugger/debug-interface-access/idiaenumlinenumbers-get-count.md) yöntemi.  
  
 lineNumber  
 [out] Döndürür bir [Idialinenumber](../../debugger/debug-interface-access/idialinenumber.md) istediğiniz satır numarasını temsil eden nesne.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi takdirde bir hata kodu döndürür.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumlinenumbers](../../debugger/debug-interface-access/idiaenumlinenumbers.md)   
 [IDiaLineNumber](../../debugger/debug-interface-access/idialinenumber.md)
