---
title: Idiasymbol::get_volatiletype | Microsoft Docs
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
- IDiaSymbol::get_volatileType method
ms.assetid: 19782a4d-40a8-467b-ab7d-58bc4d812309
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 4e91ead5fc7f1618afacb1d8fe42a30f6fa3f6bd
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49303153"
---
# <a name="idiasymbolgetvolatiletype"></a>IDiaSymbol::get_volatileType
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Kullanıcı tanımlı veri türü (UDT) geçici olup olmadığını belirten bir bayrak alır.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_volatileType (   
   BOOL* pRetVal  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pRetVal`  
 [out] Döndürür `TRUE` UDT, aksi takdirde geçici döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="remarks"></a>Açıklamalar  
 C++'da bir UDT ile işaretlenebilir `volatile` içeriğinin bir erişimden sonraki bulunması kabul edilemez belirten bir anahtar sözcüğü,.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)



