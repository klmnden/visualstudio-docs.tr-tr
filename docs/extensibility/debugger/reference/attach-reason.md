---
title: ATTACH_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- ATTACH_REASON
helpviewer_keywords:
- ATTACH_REASON enumeration
ms.assetid: 159fb70b-a344-4ba6-9115-b7eaa16e228f
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 8c132b507d679fd6cec5ce7fff04362159cbc848
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66351843"
---
# <a name="attachreason"></a>ATTACH_REASON
Bir program düğüme iliştirmek için hata ayıklama altyapısı (DE) nedenini belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_ATTACH_REASON {
    ATTACH_REASON_LAUNCH = 0x0001,
    ATTACH_REASON_USER   = 0x0002,
    ATTACH_REASON_AUTO   = 0x0003
};
typedef DWORD ATTACH_REASON;
```

```csharp
public enum enum_ATTACH_REASON {
    ATTACH_REASON_LAUNCH = 0x0001,
    ATTACH_REASON_USER   = 0x0002,
    ATTACH_REASON_AUTO   = 0x0003
};
```

## <a name="fields"></a>Alanlar
`ATTACH_REASON_AUTO`\
İşlem şu anda hata ayıklama modunda olduğundan ekleyin.

`ATTACH_REASON_LAUNCH`\
İşlem başlatıldığından ekleyin.

`ATTACH_REASON_USER`\
Bir kullanıcı isteği nedeniyle ekleyin.

## <a name="remarks"></a>Açıklamalar
Bu değerler için parametre olarak kullanılan [iliştirme](../../../extensibility/debugger/reference/idebugengine2-attach.md) ve [iliştirme](../../../extensibility/debugger/reference/idebugprogramex2-attach.md) yöntemleri.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [Attach](../../../extensibility/debugger/reference/idebugengine2-attach.md)
- [Attach](../../../extensibility/debugger/reference/idebugprogramex2-attach.md)
