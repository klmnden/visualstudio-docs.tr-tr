---
title: Js_natıve_frame yapısı | Microsoft Docs
ms.custom: ''
ms.date: 01/18/2017
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
apiname:
- JS_NATIVE_FRAME
apilocation:
- jscript9diag.dll
ms.assetid: 5afa2ee1-b3e2-47cb-b304-84f96e6fbb14
caps.latest.revision: 4
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: 9a0777cf42b9ed9412602cb34ed2d521deca1fb9
ms.sourcegitcommit: d3a485d47c6ba01b0fc9878cbbb7fe88755b29af
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2019
ms.locfileid: "58150120"
---
# <a name="jsnativeframe-structure"></a>JS_NATIVE_FRAME Yapısı
Bir yığın çerçevesini temsil eder.  
  
## <a name="syntax"></a>Sözdizimi  
  
```cpp
typedef struct {  
    UINT64 InstructionOffset;    UINT64 ReturnOffset;    UINT64 FrameOffset;    UINT64 StackOffset;  
} JS_NATIVE_FRAME;  
```  
  
## <a name="members"></a>Üyeler  
 `InstructionOffset`  
 Yönerge işaretçisi.  
  
 `ReturnOffset`  
 Dönüş adresi.  
  
 `FrameOffset`  
 Çerçeve işaretçisi.  
  
 `StackOffset`  
 Yığın işaretçisi.  
  
## <a name="remarks"></a>Açıklamalar  
 `JS_NATIVE_FRAME` Yapı tarafından kullanılan `IJsStackFrameEnumerator`.  
  
## <a name="see-also"></a>Ayrıca Bkz.  
 [Etkin Betik Hata Ayıklayıcı Sabitleri, Sabit Listeleri ve Yapıları](../../winscript/reference/active-script-debugger-constants-enumerations-and-structures.md)