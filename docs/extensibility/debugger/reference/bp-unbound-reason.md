---
title: BP_UNBOUND_REASON | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- BP_UNBOUND_REASON
helpviewer_keywords:
- BP_UNBOUND_REASON enumeration
ms.assetid: 939b6f9c-113b-471d-9f30-b03871af6285
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 65393f6e162cb15ded7a0e598e360c7ce90bb3cd
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56717669"
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

## <a name="members"></a>Üyeler
BPUR_UNKNOWN nedeni bilinmiyor.

Kesme noktasını içeren kod BPUR_CODE_UNLOADED kaldırıldı.

Farklı bir konuma kesme noktası yansıdı BPUR_BREAKPOINT_REBIND. Bu düzenlemeden sonra gerçekleşir ve kesme noktası hareket ettiğinde veya artık geçerli olmayan bir yola sahip bir dosya kesme noktasına bağlandığında işlemler devam edebilirsiniz.

BPUR_ BREAKPOINT_ERROR Kesme noktasının bağlı olduğu sonra hata olduğu belirlenir. Bu, koşullar artık geçerli olmayan yönetilen kesme noktaları için gerçekleşir.

## <a name="remarks"></a>Açıklamalar
Tarafından döndürülen [GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md) yöntemi.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [GetReason](../../../extensibility/debugger/reference/idebugbreakpointunboundevent2-getreason.md)
