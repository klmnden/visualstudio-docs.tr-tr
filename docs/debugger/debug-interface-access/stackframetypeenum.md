---
title: StackFrameTypeEnum | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- StackFrameTypeEnum enumeration
ms.assetid: 61e40163-eee0-4c1f-af47-cef3771bdc41
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: dab674576655df3b4a695d97fdfdb42df2ffa449
ms.sourcegitcommit: 22b73c601f88c5c236fe81be7ba4f7f562406d75
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56227270"
---
# <a name="stackframetypeenum"></a>StackFrameTypeEnum
Yığın çerçeve türünü belirtir.

## <a name="syntax"></a>Sözdizimi

```C++
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
[Enumerations and Structures](../../debugger/debug-interface-access/enumerations-and-structures.md)  
[IDiaStackFrame::get_type](../../debugger/debug-interface-access/idiastackframe-get-type.md)
