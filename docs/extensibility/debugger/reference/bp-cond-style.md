---
title: BP_COND_STYLE | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_COND_STYLE
helpviewer_keywords:
- BP_COND_STYLE enumeration
ms.assetid: a93b1412-f447-48a1-af9d-38f3dbb3092f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: ded3d31f9be2d0a02a238ead4bc989cc21b4922a
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351820"
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

## <a name="fields"></a>Alanlar
`BP_COND_NONE`\
Kesme noktasına, Kesme noktasının konuma ulaşıldığında tetikler. Belirtilen hiçbir kesme noktası koşulu.

`BP_COND_WHEN_TRUE`\
Veren, koşullu ifade kesme noktasıyla ilişkili yalnızca bir kesme noktası harekete `true`.

`BP_COND_WHEN_CHANGED`\
Yalnızca koşullu ifadenin değerini kesme noktası ile ilişkili olduğunda kesme noktası, önceki değerlendirmesinden gelen değişti ateşlenir.

## <a name="remarks"></a>Açıklamalar
İçin kullanılan `styleCondition` üyesi [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md) yapısı.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [BP_CONDITION](../../../extensibility/debugger/reference/bp-condition.md)
