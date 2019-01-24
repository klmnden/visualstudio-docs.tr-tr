---
title: DataKind | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- DataKind enumeration
ms.assetid: b64be708-22d6-4360-99e7-8f4e6b196de7
caps.latest.revision: 11
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: a6a72d1093bc8acd9aae788ff357aee2efeb9e52
ms.sourcegitcommit: 8b538eea125241e9d6d8b7297b72a66faa9a4a47
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54754923"
---
# <a name="datakind"></a>DataKind
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Veri değeri belirli kapsamını belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
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
