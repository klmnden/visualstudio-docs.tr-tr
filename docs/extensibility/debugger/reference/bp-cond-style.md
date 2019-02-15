---
title: BP_COND_STYLE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
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
ms.openlocfilehash: d8ca4f551f4dd6541bad9d73b5e91c671ad80492
ms.sourcegitcommit: 752f03977f45169585e407ef719450dbe219b7fc
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2019
ms.locfileid: "56318309"
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
BP_COND_NONE  
Kesme noktasına, Kesme noktasının konuma ulaşıldığında tetikler. Belirtilen hiçbir kesme noktası koşulu.

BP_COND_WHEN_TRUE  
Veren, koşullu ifade kesme noktasıyla ilişkili yalnızca bir kesme noktası harekete `true`.

BP_COND_WHEN_CHANGED  
Yalnızca koşullu ifadenin değerini kesme noktası ile ilişkili olduğunda kesme noktası, önceki değerlendirmesinden gelen değişti ateşlenir.

## <a name="remarks"></a>Açıklamalar
İçin kullanılan `styleCondition` üyesi [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) yapısı.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)
