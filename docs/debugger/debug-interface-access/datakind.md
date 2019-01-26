---
title: DataKind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- DataKind enumeration
ms.assetid: b64be708-22d6-4360-99e7-8f4e6b196de7
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 2a967581a2b5da2354908f6f5d6a2f5a35d7fa1c
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "55040027"
---
# <a name="datakind"></a>DataKind
Veri değeri belirli kapsamını belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
enum DataKind {   
   DataIsUnknown,  
   DataIsLocal,  
   DataIsStaticLocal,  
   DataIsParam,  
   DataIsObjectPtr,  
   DataIsFileStatic,  
   DataIsGlobal,  
   DataIsMember,  
   DataIsStaticMember,  
   DataIsConstant  
};  
```  
  
## <a name="elements"></a>Öğeleri  
 DataIsUnknown  
 Veri sembol belirlenemiyor.  
  
 DataIsLocal  
 Veri öğesi yerel bir değişkendir.  
  
 DataIsStaticLocal  
 Statik bir yerel değişken veri öğesidir.  
  
 DataIsParam  
 Biçimsel parametre veri öğesidir.  
  
 DataIsObjectPtr  
 Veri öğesi olan bir nesne işaretçisi (`this`).  
  
 DataIsFileStatic  
 Veri öğesi dosya kapsamlı bir değişkendir.  
  
 DataIsGlobal  
 Veri öğesi genel bir değişkendir.  
  
 DataIsMember  
 Bir nesne üye değişkeni veri öğesidir.  
  
 DataIsStaticMember  
 Veri öğesi bir sınıfın statik değişkendir.  
  
 DataIsConstant  
 Veri öğesi, bir sabit değerdir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu sabit listesi değerleri tarafından döndürülen [Idiasymbol::get_datakind](../../debugger/debug-interface-access/idiasymbol-get-datakind.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: cvconst.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol::get_dataKind](../../debugger/debug-interface-access/idiasymbol-get-datakind.md)