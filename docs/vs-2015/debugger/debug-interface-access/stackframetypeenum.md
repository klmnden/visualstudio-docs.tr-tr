---
title: StackFrameTypeEnum | Microsoft Docs
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
- StackFrameTypeEnum enumeration
ms.assetid: 61e40163-eee0-4c1f-af47-cef3771bdc41
caps.latest.revision: 10
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: fb233000eb9bc0684858a82bf63ac2d71dbd60e5
ms.sourcegitcommit: 9ceaf69568d61023868ced59108ae4dd46f720ab
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/12/2018
ms.locfileid: "49252273"
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
  
## <a name="elements"></a>Öğeleri  
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



