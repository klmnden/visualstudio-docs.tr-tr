---
title: BP_PASSCOUNT | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_PASSCOUNT
helpviewer_keywords:
- BP_PASSCOUNT structure
ms.assetid: 791ac175-b897-4c70-873e-240da7e0ac89
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 3fd1ab73a20b319af6c9464062113f4e8f2d64fa
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66353021"
---
# <a name="bppasscount"></a>BP_PASSCOUNT
Bağlı bir koşullu kesme noktası tetiklendiğinde sayısı ve koşullar açıklanmaktadır.

## <a name="syntax"></a>Sözdizimi

```cpp
typedef struct _BP_PASSCOUNT {
    DWORD              dwPassCount;
    BP_PASSCOUNT_STYLE stylePassCount;
} BP_PASSCOUNT;
```

```csharp
public struct BP_PASSCOUNT {
    public uint dwPassCount;
    public uint stylePassCount;
};
```

## <a name="members"></a>Üyeler
`dwPassCount`\
Kaç kez tetiklemeden önce üzerinde bir kesme noktası geçirilecek.

`stylePassCount`\
Bir değer [BP_PASSCOUNT_STYLE](../../../extensibility/debugger/reference/bp-passcount-style.md) kesme noktası stilini belirten sabit listesi sayısı geçirin.

## <a name="remarks"></a>Açıklamalar
Bu yapı üyesidir [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md) yapısı.

Bu yapı ayrıca bir parametre olarak geçirilen[SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md) ve[SetPassCount](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setpasscount.md) yöntemleri.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Yapılar ve Birleşimler](../../../extensibility/debugger/reference/structures-and-unions.md)
- [BP_REQUEST_INFO](../../../extensibility/debugger/reference/bp-request-info.md)
- [SetPassCount](../../../extensibility/debugger/reference/idebugboundbreakpoint2-setpasscount.md)
- [SetPassCount](../../../extensibility/debugger/reference/idebugpendingbreakpoint2-setpasscount.md)
- [BP_PASSCOUNT_STYLE](../../../extensibility/debugger/reference/bp-passcount-style.md)
