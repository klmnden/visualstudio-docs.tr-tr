---
title: CONTEXT_INFO_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- CONTEXT_INFO_FIELDS
helpviewer_keywords:
- CONTEXT_INFO_FIELDS enumeration
ms.assetid: ef436bd3-738e-47e8-828c-8febce752439
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 13501c86eabd249e0e47137099862cd6db654415
ms.sourcegitcommit: b0d8e61745f67bd1f7ecf7fe080a0fe73ac6a181
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/22/2019
ms.locfileid: "56706099"
---
# <a name="contextinfofields"></a>CONTEXT_INFO_FIELDS
Bir bellek bağlamı hakkında almak için hangi bilgilerin belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_CONTEXT_INFO_FIELDS {
    CIF_MODULEURL =       0x00000001,
    CIF_FUNCTION =        0x00000002,
    CIF_FUNCTIONOFFSET =  0x00000004,
    CIF_ADDRESS =         0x00000008,
    CIF_ADDRESSOFFSET =   0x00000010,
    CIF_ADDRESSABSOLUTE = 0x00000020,
    CIF_ALLFIELDS =       0x0000003f
};
typedef DWORD CONTEXT_INFO_FIELDS;
```

```csharp
public enum enum_CONTEXT_INFO_FIELDS {
    CIF_MODULEURL =       0x00000001,
    CIF_FUNCTION =        0x00000002,
    CIF_FUNCTIONOFFSET =  0x00000004,
    CIF_ADDRESS =         0x00000008,
    CIF_ADDRESSOFFSET =   0x00000010,
    CIF_ADDRESSABSOLUTE = 0x00000020,
    CIF_ALLFIELDS =       0x0000003f
};
```

## <a name="members"></a>Üyeler
CIF_MODULEURL başlatma/kullanım `bstrModuleUrl` alanını [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md) yapısı.

CIF_FUNCTION başlatma/kullanım `bstrFunction` alanını `CONTEXT_INFO` yapısı.

CIF_FUNCTIONOFFSET başlatma/kullanım `posFunctionOffset` alanını `CONTEXT_INFO` yapısı.

CIF_ADDRESS başlatma/kullanım `bstrAddress` alanını `CONTEXT_INFO` yapısı.

CIF_ADDRESSOFFSET başlatma/kullanım `bstrAddressOffset` alanını `CONTEXT_INFO` yapısı.

CIF_ALLFIELDS başlatma/kullanım tüm alanları `CONTEXT_INFO` yapısı.

## <a name="remarks"></a>Açıklamalar
Bu değerleri bir parametresine geçirilir [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md) hangi alanları göstermek için yöntemi [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md) yapısı olan başlatılacak.

Bu bayraklar Ayrıca hangi alanları göstermek için kullanılan `CONTEXT_INFO` yapısı, kullanılan ve geçerli yapısı döndürülür.

Bu değerleri bir bit düzeyinde OR ile birleştirilebilir.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
- [Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)
- [CONTEXT_INFO](../../../extensibility/debugger/reference/context-info.md)
- [GetInfo](../../../extensibility/debugger/reference/idebugmemorycontext2-getinfo.md)
