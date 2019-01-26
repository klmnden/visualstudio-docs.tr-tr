---
title: UdtKind | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- UdtKind enumeration
ms.assetid: 400b59b9-373c-42cb-aae1-570494214328
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eaca67dd56fa34993e46693d6274bc4b7b593006
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/25/2019
ms.locfileid: "54929412"
---
# <a name="udtkind"></a>UdtKind
Kullanıcı tanımlı tür (UDT) çeşitli açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```C++  
enum UdtKind {   
   UdtStruct,  
   UdtClass,  
   UdtUnion,  
   UdtInterface  
};  
```  
  
## <a name="elements"></a>Öğeleri  
 UdtStruct  
 UDT bir yapıdır.  
  
 UdtClass  
 UDT bir sınıftır.  
  
 UdtUnion  
 UDT bir birleşimdir.  
  
 UdtInterface  
 UDT bir arabirimdir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu sabit listesi değerleri tarafından döndürülen [Idiasymbol::get_udtkind](../../debugger/debug-interface-access/idiasymbol-get-udtkind.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: cvconst.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol::get_udtKind](../../debugger/debug-interface-access/idiasymbol-get-udtkind.md)