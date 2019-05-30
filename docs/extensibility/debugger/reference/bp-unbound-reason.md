---
title: BP_UNBOUND_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_UNBOUND_REASON
helpviewer_keywords:
- BP_UNBOUND_REASON enumeration
ms.assetid: 939b6f9c-113b-471d-9f30-b03871af6285
author: madskristensen
ms.author: madsk
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 9de6812f3a61feca8ca8e7153fb281369c3312bd
ms.sourcegitcommit: 40d612240dc5bea418cd27fdacdf85ea177e2df3
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2019
ms.locfileid: "66350562"
---
# <a name="bpunboundreason"></a>BP_UNBOUND_REASON
Bir kesme noktası ilişkisiz nedeni sağlar.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BP_UNBOUND_REASON {
    BPUR_UNKNOWN           = 0x0000,
    BPUR_CODE_UNLOADED     = 0x0002,
    BPUR_BREAKPOINT_REBIND = 0x0003,
    BPUR_BREAKPOINT_ERROR  = 0x0004
};
typedef DWORD BP_UNBOUND_REASON;
```

```csharp
public enum enum_BP_UNBOUND_REASON {
    BPUR_UNKNOWN           = 0x0000,
    BPUR_CODE_UNLOADED     = 0x0002,
    BPUR_BREAKPOINT_REBIND = 0x0003,
    BPUR_BREAKPOINT_ERROR  = 0x0004
};
```

## <a name="fields"></a>Alanlar
`BPUR_UNKNOWN`\
Bunun nedeni bilinmiyor.

`BPUR_CODE_UNLOADED`\
Kesme noktasını içeren kod kaldırıldı.

`BPUR_BREAKPOINT_REBIND`\
Farklı bir konuma kesme noktası yansıdı. Bu düzenlemeden sonra gerçekleşir ve kesme noktası hareket ettiğinde veya artık geçerli olmayan bir yola sahip bir dosya kesme noktasına bağlandığında işlemler devam edebilirsiniz.

`BPUR_ BREAKPOINT_ERROR`\
Kesme noktasına bağlı sonra hata olarak değerlendirilir. Bu, koşullar artık geçerli olmayan yönetilen kesme noktaları için gerçekleşir.

## <a name="remarks"></a>Açıklamalar
Tarafından döndürülen [GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md)
