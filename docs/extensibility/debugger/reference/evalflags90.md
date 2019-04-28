---
title: EVALFLAGS90 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- EVALFLAGS90 enumeration
ms.assetid: 64fb0139-8b04-4726-b52c-db2e04d65498
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 73673d0b0ca7ccb640a3fab2043bc35b26657a9b
ms.sourcegitcommit: 94b3a052fb1229c7e7f8804b09c1d403385c7630
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62924356"
---
# <a name="evalflags90"></a>EVALFLAGS90
İfade değerlendirme denetim bayrakları için geçerli değerleri listeler. Bu numaralandırma genişletir [EVALFLAGS](../../../extensibility/debugger/reference/evalflags.md) sabit listesi.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_EVALFLAGS90
{
    // VS 8.0 values
    EVAL90_RETURNVALUE                 = 0x0002,
    EVAL90_NOSIDEEFFECTS               = 0x0004,
    EVAL90_ALLOWBPS                    = 0x0008,
    EVAL90_ALLOWERRORREPORT            = 0x0010,
    EVAL90_FUNCTION_AS_ADDRESS         = 0x0040,
    EVAL90_NOFUNCEVAL                  = 0x0080,
    EVAL90_NOEVENTS                    = 0x1000,
    EVAL90_DESIGN_TIME_EXPR_EVAL       = 0x2000,
    EVAL90_ALLOW_IMPLICIT_VARS         = 0x4000,

    // Values added in VS 9.0
    EVAL90_FORCE_EVALUATION_NOW        = 0x8000
};
typedef DWORD EVALFLAGS90;
```

```csharp
public enum enum_EVALFLAGS90
{
    // VS 8.0 values
    EVAL90_RETURNVALUE                 = 0x0002,
    EVAL90_NOSIDEEFFECTS               = 0x0004,
    EVAL90_ALLOWBPS                    = 0x0008,
    EVAL90_ALLOWERRORREPORT            = 0x0010,
    EVAL90_FUNCTION_AS_ADDRESS         = 0x0040,
    EVAL90_NOFUNCEVAL                  = 0x0080,
    EVAL90_NOEVENTS                    = 0x1000,
    EVAL90_DESIGN_TIME_EXPR_EVAL       = 0x2000,
    EVAL90_ALLOW_IMPLICIT_VARS         = 0x4000,

    // Values added in VS 9.0
    EVAL90_FORCE_EVALUATION_NOW        = 0x8000
};
```

#### <a name="parameters"></a>Parametreler
Dönüş değeri varsa, değerlendirilecek EVAL90_RETURNVALUE belirtir.

EVAL90_NOSIDEEFFECTS yan etkileri izin verilmeyeceğini belirtir.

Kesme noktalarında durdurma EVAL90_ALLOWBPS belirtir.

EVAL90_ALLOWERRORREPORT izin verilmesi için konağa Raporlama hata belirtir. Internet Explorer'da komut ifade değerlendirmesi için kullanılır.

İşlev çağırma yerine adresleri olarak değerlendirilecek işlevleri EVAL90_FUNCTION_AS_ADDRESS zorlar.

Değerlendirilen gelen işlevi EVAL90_NOFUNCEVAL engeller. Örneğin, düşünün `int` ifade belirteci `myExpression(int) + 10`. Bu işlev bir adres, ancak bir değer olarak değil doğru değerlendirilebilir.

EVAL90_NOEVENTS ifadesi değerlendirmesi sırasında meydana gelen olayları oturum hata ayıklama Yöneticisi (SDM) veya IDE gönderilmemelidir belirten bayrak.

Tasarım zamanı ifade değerlendirmesi EVAL90_DESIGN_TIME_EXPR_EVAL sağlar.

Örtük değişken oluşturma EVAL90_ALLOW_IMPLICIT_VARS sağlar.

Hemen oluşmasını zorlar EVAL90_FORCE_EVALUATION_NOW değerlendirmesi'ni kullanın. Bu, hizmet kullanıcı isteği gibi bir istek olduğunda yararlıdır.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg90.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
