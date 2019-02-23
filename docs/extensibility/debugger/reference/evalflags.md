---
title: EVALFLAGS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
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
ms.openlocfilehash: d9d59262349891a5c0483297039578c5de4a7b72
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56696278"
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
Dönüş değeri varsa, değerlendirilecek EVAL_RETURNVALUE belirtir.

EVAL_NOSIDEEFFECTS yan etkileri izin verilmeyeceğini belirtir.

Kesme noktalarında durdurma EVAL_ALLOWBPS belirtir.

Konağa izin verilmesi için raporlama EVAL_ALLOWERRORREPORT belirtir hata oluştu. Internet Explorer'da komut ifade değerlendirmesi için kullanılır.

İşlev çağırma yerine adresleri olarak değerlendirilecek işlevleri EVAL_FUNCTION_AS_ADDRESS zorlar.

Değerlendirilen gelen işlevi EVAL_NOFUNCEVAL engeller. Örneğin, düşünün `int` ifade belirteci `myExpression(int) + 10`. Bu işlev bir adres, ancak bir değer olarak değil doğru değerlendirilebilir.

EVAL_NOEVENTS ifadesi değerlendirmesi sırasında meydana gelen olayları oturum hata ayıklama Yöneticisi (SDM) veya IDE gönderilmemelidir belirten bayrak.

## <a name="remarks"></a>Açıklamalar
Bu bayraklar bağımsız değişken olarak geçirilen [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md) ve [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md) yöntemleri.

Bu bayraklar bir bit düzeyinde OR ile birleştirilebilir.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [EvaluateAsync](../../../extensibility/debugger/reference/idebugexpression2-evaluateasync.md)
- [EvaluateSync](../../../extensibility/debugger/reference/idebugexpression2-evaluatesync.md)
