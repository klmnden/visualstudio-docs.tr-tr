---
title: Idiasymbol::get_haslongjump | Microsoft Docs
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
- IDiaSymbol::get_hasLongJump method
ms.assetid: 14484cb1-43b0-47a1-a9a8-081b55566886
caps.latest.revision: 11
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 739176b12d9d0eff6c9ada41aa0d49cb851384a6
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49209384"
---
# <a name="idiasymbolgethaslongjump"></a>IDiaSymbol::get_hasLongJump
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

İşlev bir kullanımını içerip içermediğini belirten bir bayrak alır [longjmp](http://msdn.microsoft.com/library/0e13670a-5130-45c1-ad69-6862505b7a2f) komut (ile eşleştirilmiş bir [setjmp](http://msdn.microsoft.com/library/684a8b27-e8eb-455b-b4a8-733ca1cbd7d2) komutu, C stili yöntemi özel durum işleme gelerek).  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
HRESULT get_hasLongJump  
   BOOL *pFlag  
);  
```  
  
#### <a name="parameters"></a>Parametreler  
 `pFlag`  
 [out] Döndürür `TRUE` işlevi içeriyorsa bir `longjmp` komut; Aksi halde döndürür `FALSE`.  
  
## <a name="return-value"></a>Dönüş Değeri  
 Başarılı olursa döndürür `S_OK`; Aksi halde döndürür `S_FALSE` veya bir hata kodu.  
  
> [!NOTE]
>  Dönüş değeri `S_FALSE` özelliği simge için mevcut olmadığı anlamına gelir.  
  
## <a name="requirements"></a>Gereksinimler  
  
|Gereksinim|Açıklama|  
|-----------------|-----------------|  
|Üst bilgi:|dia2.h|  
|Sürüm:|DIA SDK v8.0|  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Idiasymbol](../../debugger/debug-interface-access/idiasymbol.md)   
 [Idiasymbol::get_hassetjump](../../debugger/debug-interface-access/idiasymbol-get-hassetjump.md)   
 [longjmp](http://msdn.microsoft.com/library/0e13670a-5130-45c1-ad69-6862505b7a2f)   
 [setjmp](http://msdn.microsoft.com/library/684a8b27-e8eb-455b-b4a8-733ca1cbd7d2)



