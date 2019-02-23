---
title: BP_COND_STYLE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_COND_STYLE
helpviewer_keywords:
- BP_COND_STYLE enumeration
ms.assetid: a93b1412-f447-48a1-af9d-38f3dbb3092f
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 70ab3655d27e810b3c05d0e0e81d81bc15a26950
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56685865"
---
# <a name="bpcondstyle"></a>BP_COND_STYLE
Bekleyen kesme noktası koşulu stili için belirtir ve bağlı kesme noktaları.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BP_COND_STYLE {
    BP_COND_NONE         = 0x0000,
    BP_COND_WHEN_TRUE    = 0x0001,
    BP_COND_WHEN_CHANGED = 0x0002
};
typedef DWORD BP_COND_STYLE;
```

```csharp
public enum enum_BP_COND_STYLE {
    BP_COND_NONE         = 0x0000,
    BP_COND_WHEN_TRUE    = 0x0001,
    BP_COND_WHEN_CHANGED = 0x0002
};
```

## <a name="members"></a>Üyeler
Kesme noktasının konuma ulaşıldığında BP_COND_NONE kesme noktası tetikler. Belirtilen hiçbir kesme noktası koşulu.

BP_COND_WHEN_TRUE değerlendiren, koşullu ifade kesme noktasıyla ilişkili yalnızca bir kesme noktası harekete `true`.

Yalnızca koşullu ifadenin değerini kesme noktası ile ilişkili olduğunda kesme noktası, önceki değerlendirmesinden gelen değişti BP_COND_WHEN_CHANGED ateşlenir.

## <a name="remarks"></a>Açıklamalar
İçin kullanılan `styleCondition` üyesi [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) yapısı.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)
