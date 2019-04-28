---
title: CV_call_e | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- CV_call_e enumeration
ms.assetid: f230560b-4243-432d-8f19-46df112043b9
caps.latest.revision: 13
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: cd1ee4c024894e5752277a5000d37745c88c4ac6
ms.sourcegitcommit: 47eeeeadd84c879636e9d48747b615de69384356
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "63442100"
---
# <a name="cvcalle"></a>CV_call_e
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Bir işlev çağırma kuralını belirtir.  
  
> [!NOTE]
> En yaygın numaralandırma değerlerinden yalnızca aşağıda belirtilmiştir. Tam numaralandırma cvconst.h üstbilgi dosyasında kullanılabilir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp#  
typedef enum CV_call_e {   
   CV_CALL_NEAR_C    = 0x00,  
   CV_CALL_NEAR_FAST = 0x04,  
   CV_CALL_NEAR_STD  = 0x07,  
   CV_CALL_NEAR_SYS  = 0x09,  
   CV_CALL_THISCALL  = 0x0b,  
   CV_CALL_CLRCALL   = 0x16  
} CV_call_e;  
```  
  
## <a name="elements"></a>Öğeleri  
 CV_CALL_NEAR_C  
 Yakın sağdan sola push kullanarak bir işlev çağırma kuralını belirtir. Çağıran işlev, yığını temizler.  
  
 CV_CALL_NEAR_FAST  
 Yazmaçları ile yakın bir soldan sağa anında iletme kullanarak bir işlevi çağırma kuralını belirtir. Çağrılan işlev parametresi baytların toplamından yığın temizlemek için kullanır.  
  
 CV_CALL_NEAR_STD  
 Yakın bir standart çağrı (sağdan sola anında iletme) kullanarak bir işlev çağırma kuralını belirtir.  
  
 CV_CALL_NEAR_SYS  
 Yakın bir sistem çağrısı kullanarak bir işlev çağırma kuralını belirtir.  
  
 CV_CALL_THISCALL  
 Kullanarak bir işlev çağırma kuralını belirtir `this` çağırın (`this` işaretçi geçirildi kayıttaki).  
  
 CV_CALL_CLRCALL  
 Ortak dil çalışma zamanı (CLR tarafından) (çağırma kuralı olarak da bilinen bir yönetilen kod için) kullanılan bir işlevi çağırma kuralını belirtir.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu numaralandırma değerleri için yapılan bir çağrı tarafından döndürülen [Idiasymbol::get_callingconvention](../../debugger/debug-interface-access/idiasymbol-get-callingconvention.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: cvconst.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol::get_callingConvention](../../debugger/debug-interface-access/idiasymbol-get-callingconvention.md)
