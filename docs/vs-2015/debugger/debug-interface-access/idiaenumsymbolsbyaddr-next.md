---
title: Idiaenumsymbolsbyaddr::Next | Microsoft Docs
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
- IDiaEnumSymbolsByAddr::Next method
ms.assetid: a1320587-7ce7-401f-9548-2f8bcece5cc3
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 64645ecbe2f1844b7231f9c5eade9e105e934b2f
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49177007"
---
# <a name="idiaenumsymbolsbyaddrnext"></a>IDiaEnumSymbolsByAddr::Next
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Sonraki simgeleri sırayla adresine göre alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT Next (   
   ULONG        celt,   
   IDiaSymbol** rgelt,  
   ULONG*       pceltFetched  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 celt  
 [in] Alınacak Numaralandırıcı sembolleri sayısı.  
  
 http://msdn.microsoft.com/library/default.asp?url=/library/en-us/winui/winui/windowsuserinterface/userinput/rawinput/rawinputreference/rawinputstructures/rawinputdevice.asp  
 [out] İle doldurulacak bir dizi [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md) istenen simgeleri temsil eden nesne.  
  
 pceltFetched  
 [out] Simgelerin sayısını getirilen bir numaralandırıcı döndürür.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`. Döndürür `S_FALSE` daha fazla sembol varsa. Aksi takdirde bir hata kodu döndürür.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu yöntem, numaralandırıcı konumu alınan öğelerin sayısı ile güncelleştirir.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiaenumsymbolsbyaddr](../../debugger/debug-interface-access/idiaenumsymbolsbyaddr.md)   
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



