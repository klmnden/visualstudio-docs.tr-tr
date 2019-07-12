---
title: Idiasymbol::get_isnaked | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_isNaked method
ms.assetid: b16629dc-8e17-476b-9c7b-58e7277c61ed
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 64989ca10416ab2ad9606c94b3f3bc977f60c5ee
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "65702355"
---
# <a name="idiasymbolgetisnaked"></a>IDiaSymbol::get_isNaked
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İşlev olup olmadığını belirten bir bayrak alır [naked](https://msdn.microsoft.com/library/69723241-05e1-439b-868e-20a83a16ab6d) özniteliği (diğer bir deyişle, işlev derleyici tarafından eklenen giriş veya çıkış kodu olmayan).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT get_isNaked(  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pFlag`  
 [out] Döndürür `TRUE` işlevi varsa `naked` özniteliği; Aksi halde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Naked İşlevi Çağrıları](https://msdn.microsoft.com/library/2a66847a-a43f-4541-a7be-c9f5f29b5fdb)
