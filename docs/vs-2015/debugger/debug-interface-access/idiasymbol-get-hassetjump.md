---
title: Idiasymbol::get_hassetjump | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_hasSetJump method
ms.assetid: 22656206-dccf-40ed-b179-fc016d1b262a
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 3de774fcfa7fcbce48653eb1e6615ae70902cb0d
ms.sourcegitcommit: 75807551ea14c5a37aa07dd93a170b02fc67bc8c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "65703749"
---
# <a name="idiasymbolgethassetjump"></a>IDiaSymbol::get_hasSetJump
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İşlev bir kullanımını içerip içermediğini belirten bir bayrak alır [setjmp](https://msdn.microsoft.com/library/684a8b27-e8eb-455b-b4a8-733ca1cbd7d2) komut (ile eşleştirilmiş [longjmp](https://msdn.microsoft.com/library/0e13670a-5130-45c1-ad69-6862505b7a2f) komutu, C stili yöntemi özel durum işleme gelerek).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
HRESULT get_hasSetJump(  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pFlag`  
 [out] Döndürür `TRUE` işlevi içeriyorsa bir `setjmp` komut; Aksi halde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya hata kodu.  
  
> [!NOTE]
> Dönüş değeri `S_FALSE` özelliği simge için kullanılabilir değil anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasymbol::get_haslongjump](../../debugger/debug-interface-access/idiasymbol-get-haslongjump.md)   
 [longjmp](https://msdn.microsoft.com/library/0e13670a-5130-45c1-ad69-6862505b7a2f)   
 [setjmp](https://msdn.microsoft.com/library/684a8b27-e8eb-455b-b4a8-733ca1cbd7d2)
