---
title: EVALFLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- EVALFLAGS
helpviewer_keywords:
- EVALFLAGS enumeration
ms.assetid: 7b2cb14a-511a-4fef-9e4f-308139719fba
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 3f780f06188d738deeb7f4b781fba1313e46db6d
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56315774"
---
# <a name="evalflags"></a>EVALFLAGS
İfade değerlendirme denetim bayrakları belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_EVALFLAGS {
    EVAL_RETURNVALUE = 0x0002,
    EVAL_NOSIDEEFFECTS = 0x0004,
    EVAL_ALLOWBPS = 0x0008,
    EVAL_ALLOWERRORREPORT = 0x0010,
    EVAL_FUNCTION_AS_ADDRESS = 0x0040,
    EVAL_NOFUNCEVAL = 0x0080,
    EVAL_NOEVENTS = 0x1000
};
typedef DWORD EVALFLAGS;
```

```csharp
public enum enum_EVALFLAGS {
    EVAL_RETURNVALUE = 0x0002,
    EVAL_NOSIDEEFFECTS = 0x0004,
    EVAL_ALLOWBPS = 0x0008,
    EVAL_ALLOWERRORREPORT = 0x0010,
    EVAL_FUNCTION_AS_ADDRESS = 0x0040,
    EVAL_NOFUNCEVAL = 0x0080,
    EVAL_NOEVENTS = 0x1000
}
```

## <a name="members"></a>Üyeler
EVAL_RETURNVALUE  
Dönüş değeri varsa, değerlendirilecek belirtir.

EVAL_NOSIDEEFFECTS  
Yan etkileri izin verilmeyeceğini belirtir.

EVAL_ALLOWBPS  
Durdurma kesme noktalarında belirtir.

EVAL_ALLOWERRORREPORT  
Hata izin verilmesi için konağa raporlama belirtir. Internet Explorer'da komut ifade değerlendirmesi için kullanılır.

EVAL_FUNCTION_AS_ADDRESS  
İşlev çağırma yerine adresleri olarak değerlendirilecek işlevleri zorlar.

EVAL_NOFUNCEVAL  
İşlevi, değerlendirilen öğesinden engeller. Örneğin, düşünün `int` ifade belirteci `myExpression(int) + 10`. Bu işlev bir adres, ancak bir değer olarak değil doğru değerlendirilebilir.

EVAL_NOEVENTS  
İfade değerlendirme sırasında meydana gelen olayları oturum hata ayıklama Yöneticisi (SDM) veya IDE gönderilmemelidir belirten bayrak.

## <a name="remarks"></a>Açıklamalar
Bu bayraklar bağımsız değişken olarak geçirilen [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) ve [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) yöntemleri.

Bu bayraklar bir bit düzeyinde OR ile birleştirilebilir.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)  
[EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)
