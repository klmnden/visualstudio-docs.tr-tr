---
title: EVALFLAGS90 | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
helpviewer_keywords:
- EVALFLAGS90 enumeration
ms.assetid: 64fb0139-8b04-4726-b52c-db2e04d65498
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 24afc4456570ff0c3e5dc1eb56789984bf18ac58
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66337825"
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

## <a name="fields"></a>Alanlar
`EVAL90_RETURNVALUE`\
Dönüş değeri varsa, değerlendirilecek belirtir.

`EVAL90_NOSIDEEFFECTS`\
Yan etkileri izin verilmeyeceğini belirtir.

`EVAL90_ALLOWBPS`\
Durdurma kesme noktalarında belirtir.

`EVAL90_ALLOWERRORREPORT`\
Konağa izin verilmesi için Raporlama hata belirtir. Internet Explorer'da komut ifade değerlendirmesi için kullanılır.

`EVAL90_FUNCTION_AS_ADDRESS`\
İşlev çağırma yerine adresleri olarak değerlendirilecek işlevleri zorlar.

`EVAL90_NOFUNCEVAL`\
İşlevi, değerlendirilen öğesinden engeller. Örneğin, düşünün `int` ifade belirteci `myExpression(int) + 10`. Bu işlev bir adres, ancak bir değer olarak değil doğru değerlendirilebilir.

`EVAL90_NOEVENTS`\
İfade değerlendirme sırasında meydana gelen olayları oturum hata ayıklama Yöneticisi (SDM) veya IDE gönderilmemelidir belirten bayrak.

`EVAL90_DESIGN_TIME_EXPR_EVAL`\
Tasarım zamanı ifade değerlendirmesi sağlar.

`EVAL90_ALLOW_IMPLICIT_VARS`\
Örtük değişken oluşturmaya izin verir.

`EVAL90_FORCE_EVALUATION_NOW`\
Hemen oluşmasını zorlar değerlendirmesi'ni kullanın. Bu, hizmet kullanıcı isteği gibi bir istek olduğunda yararlıdır.

## <a name="requirements"></a>Gereksinimler
Üst bilgi: Msdbg90.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
