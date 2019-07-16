---
title: StackFrameTypeEnum | Microsoft Docs
ms.date: 11/15/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-debug
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- StackFrameTypeEnum enumeration
ms.assetid: 61e40163-eee0-4c1f-af47-cef3771bdc41
caps.latest.revision: 10
author: MikeJo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 655911bac1efbafe1838e24e2056282f9036479b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "68179195"
---
# <a name="stackframetypeenum"></a>StackFrameTypeEnum
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

Yığın çerçeve türünü belirtir.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp  
enum StackFrameTypeEnum {  
   FrameTypeFPO,  
   FrameTypeTrap,  
   FrameTypeTSS,  
   FrameTypeStandard,  
   FrameTypeFrameData,  
   FrameTypeUnknown = -1  
};  
```  
  
## <a name="elements"></a>Öğeler  
 `FrameTypeFPO`  
 Çerçeve işaretçisini; atlanmış FPO bilgisi yok.  
  
 `FrameTypeTrap`  
 Çekirdek yakalama çerçevesi.  
  
 `FrameTypeTSS`  
 Çekirdek yakalama çerçevesi.  
  
 `FrameTypeStandard`  
 Standart EBP yığın çerçevesi.  
  
 `FrameTypeFrameData`  
 Çerçeve işaretçisini; atlanmış Çerçeve veri bilgileri kullanılabilir.  
  
 `FrameTypeUnknown`  
 Çerçeve herhangi bir hata ayıklama bilgisi yok.  
  
## <a name="remarks"></a>Açıklamalar  
 Bu numaralandırma değerleri için yapılan bir çağrı tarafından döndürülen [Idiastackframe::get_type](../../debugger/debug-interface-access/idiastackframe-get-type.md) yöntemi.  
  
## <a name="requirements"></a>Gereksinimler  
 Üstbilgi: cvconst.h  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Sabit listeleri ve yapıları](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaStackFrame::get_type](../../debugger/debug-interface-access/idiastackframe-get-type.md)
