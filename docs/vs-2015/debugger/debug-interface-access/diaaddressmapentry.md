---
title: DiaAddressMapEntry | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- DiaAddressMapEntry enumeration
ms.assetid: 5d0ae226-981d-4541-a801-fc4993fe663b
caps.latest.revision: 12
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 67c0a3e297f3eebfbf44724e64c4989d9bb979fb
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68164352"
---
# <a name="diaaddressmapentry"></a>DiaAddressMapEntry
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir adres eşlemesi bir girişe açıklar.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
struct DiaAddressMapEntry {   
   DWORD rva,  
   DWORD rvaTo  
};  
```  
  
## <a name="elements"></a>Öğeler  
 `rva`  
 A. görüntüdeki göreli sanal adres (RVA)  
  
 `rvaTo`  
 Göreli sanal adres `rva` görüntüde b eşlenir  
  
## <a name="remarks"></a>Açıklamalar  
 Bir adres eşlemesi tek bir görüntü düzeninden bir çeviri (A) için başka bir (B) sağlar. Bir dizi `DiaAddressMapEntry` ölçütü yapıları `rva` adres Haritası tanımlar.  
  
 Bir adresi çevrilecek `addrA`, bir adrese bir görüntüdeki `addrB`, görüntü B, aşağıdaki adımları gerçekleştirin:  
  
1. Eşleme girişi için arama `e`, en büyük ile `rva` ya da eşit `addrA`.  
  
2. Ayarlama `delta = addrA – e.rva`.  
  
3. Ayarlama `addrB = e.rvaTo + delta`.  
  
   Bir dizi `DiaAddressMapEntry` yapıları geçirildiğinde [Idiaaddressmap::set_addressmap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: dia2.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaAddressMap::set_addressMap](../../debugger/debug-interface-access/idiaaddressmap-set-addressmap.md)
