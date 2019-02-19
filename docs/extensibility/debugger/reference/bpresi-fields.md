---
title: BPRESI_FIELDS | Microsoft Docs
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- BPRESI_FIELDS
helpviewer_keywords:
- BPRESI_FIELDS enumeration
ms.assetid: 99f17b1e-3e67-4f85-89d6-5c6cf45c8008
author: gregvanl
ms.author: gregvanl
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 0784d26f4d5ae6bd8edd9b6565644a6cd513db78
ms.sourcegitcommit: 7153e2fc717d32e0e9c8a9b8c406dc4053c9fd53
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2019
ms.locfileid: "56413065"
---
# <a name="bpresifields"></a>BPRESI_FIELDS
Başarılı bir kesme noktası çözünürlüğü hakkında alınacak bilgileri belirtir.

## <a name="syntax"></a>Sözdizimi

```cpp
enum enum_BPRESI_FIELDS {
    BPRESI_BPRESLOCATION = 0x0001,
    BPRESI_PROGRAM       = 0x0002,
    BPRESI_THREAD        = 0x0004,
    BPRESI_ALLFIELDS     = 0xffffffff
};
typedef DWORD BPRESI_FIELDS;
```

```csharp
public enum enum_BPRESI_FIELDS {
    BPRESI_BPRESLOCATION = 0x0001,
    BPRESI_PROGRAM       = 0x0002,
    BPRESI_THREAD        = 0x0004,
    BPRESI_ALLFIELDS     = 0xffffffff
};
```

## <a name="members"></a>Üyeler
BPRESI_BPRESLOCATION  
Başlat/kullanım `bpResLocation` (kesme noktası çözünürlüğü konumu) alanının [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) yapısı.

BPRESI_PROGRAM  
Başlat/kullanım `pProgram` alanını `BP_RESOLUTION_INFO` yapısı.

BPRESI_THREAD  
Başlat/kullanım `pThread` alanını `BP_RESOLUTION_INFO` yapısı.

BPRESI_ALLFIELDS  
Tüm alanları belirtir.

## <a name="remarks"></a>Açıklamalar
Geçirilen [GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md) hangi alanları göstermek için yöntemi [BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md) yapısı olan başlatılacak.

Bu bayraklar Ayrıca hangi alanları göstermek için kullanılan `BP_RESOLUTION_INFO` yapısı, kullanılan ve geçerli, yapı döndürülür.

Bu değerler, bit düzeyinde ile birleştirilebilir `OR`.

## <a name="requirements"></a>Gereksinimler
Üstbilgi: msdbg.h

Ad alanı: Microsoft.VisualStudio.Debugger.Interop

Derleme: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Ayrıca Bkz.
[Sabit Listeleri](../../../extensibility/debugger/reference/enumerations-visual-studio-debugging.md)  
[BP_RESOLUTION_INFO](../../../extensibility/debugger/reference/bp-resolution-info.md)  
[GetResolutionInfo](../../../extensibility/debugger/reference/idebugbreakpointresolution2-getresolutioninfo.md)
